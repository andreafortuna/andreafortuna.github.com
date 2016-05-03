---
layout: post
title: "OpenSSL Security Advisory, 3rd May 2016: Patch, Patch ASAP!"
thumbnail: "http://www.andreafortuna.org/seurity/images/openssl/openssl.png"
description: "Memory corruption in the ASN.1 encoder (CVE-2016-2108) and Padding oracle in AES-NI CBC MAC check (CVE-2016-2107)"
keywords: Security, Threat, OpenSSL, CVE-2016-2108, CVE-2016-2107
category: Security
tags: 
- Security
- Threats
- Vulnerability
- OpenSSL

---

[Security Advisory for OpenSSL](https://www.openssl.org/news/secadv/20160503.txt): fixed two high severity vulnerability.

![OpenSSL](http://www.andreafortuna.org/seurity/images/openssl/openssl.png)

Memory corruption in the ASN.1 encoder (CVE-2016-2108)
---

This issue affected versions of OpenSSL prior to April 2015. The bug
causing the vulnerability was fixed on April 18th 2015, and released
as part of the June 11th 2015 security releases. The security impact
of the bug was not known at the time.

In previous versions of OpenSSL, ASN.1 encoding the value zero
represented as a negative integer can cause a buffer underflow
with an out-of-bounds write in i2c_ASN1_INTEGER. The ASN.1 parser does
not normally create "negative zeroes" when parsing ASN.1 input, and
therefore, an attacker cannot trigger this bug.

<hr/>

Padding oracle in AES-NI CBC MAC check (CVE-2016-2107)
---

A MITM attacker can use a padding oracle attack to decrypt traffic
when the connection uses an AES CBC cipher and the server support
AES-NI.

This issue was introduced as part of the fix for Lucky 13 padding
attack (CVE-2013-0169). The padding check was rewritten to be in
constant time by making sure that always the same bytes are read and
compared against either the MAC or padding bytes. But it no longer
checked that there was enough data to have both the MAC and padding
bytes.

OpenSSL 1.0.2 users should upgrade to 1.0.2h
OpenSSL 1.0.1 users should upgrade to 1.0.1t

This issue was reported to OpenSSL on 13th of April 2016 by Juraj
Somorovsky using TLS-Attacker. The fix was developed by Kurt Roeckx
of the OpenSSL development team.


Patch! Patch! Patch! :-)
---