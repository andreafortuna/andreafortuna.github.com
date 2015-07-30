---
layout: post
title: "Windows 10: missing MIDI wavetable?"
description: "After upgrading to Windows 10, I discovered that the softwares I use to write music (musescore, for example), are no longer able to carry out the reproduction of the music scores using the GS Wavetable Windows virtual midi interface"
thumbnail: "http://www.andreafortuna.org/technology/images/VirtualMIDISynth.png"
keywords: Windows 10, MIDI, Microsoft, VirtualMIDISynth, Musescore
category: Technology
tags: 
- Microsoft
- Windows 10
- Midi
- VirtualMIDISynth

---
{% include JB/setup %}


After upgrading to *Windows 10*, I discovered that the softwares I use to write music (*Musescore*, for example), are no longer able to carry out the reproduction of the music scores using the*GS Wavetable Windows virtual midi interface*, that allows software to  play midi sequences also without a dedicated hardware.

![VirtualMIDISynth](/technology/images/VirtualMIDISynth.png)
<!-- more -->

I have not yet  found references , but it would seem that the wavetable is one the features that have been removed/changed in this latest Windows upgrade.

The solution is quite simple: install a third-party virtual midi driver.
I chose [Coolsoft](http://coolsoft.altervista.org){:target="_blank"}'s [VirtualMIDISynth](http://coolsoft.altervista.org/en/virtualmidisynth){:target="_blank"}.

It's a userspace driver, with the possibility of loading different sound fonts.

*Main features*:

- User mode multimedia driver, no reboots, no BSOD
- Directly accessible as MIDI Out device, no need for virtual MIDI cables (like MIDI Yoke, LoopBe1)
- MIDI mixer to set track mute/volume, accessible through systray icon while playing
- Compact size (setup is ~900 KBytes)
- No DLL cluttering, everything is self contained in System32/SysWOW64 subfolder
- Clean installer, won't affect other MIDI devices
- Efficient RAM usage (allows using large SoundFonts, > 1GByte)
- Virtually unlimited polyphony (limited only by CPU)
- Load up to 30 SoundFonts and chain them
- Load all of your soundfonts into list and enable/disable them at your will
- Configure MIDI Mapper default device
- Multilanguage dialogs.


The installation is very simple and consists of two steps:

1. Downloading and installing the [driver](http://coolsoft.altervista.org/en/virtualmidisynth#download){:target="_blank"}
2. Downloading and configuring into VirtualMIDISynth a SoundFont (the 'musical instruments' that the driver will use for music playback). 

I used the *FluidR3_GM*, downloadable from [HERE](http://www.synthfont.com/soundfonts.html){:target="_blank"}

Once the installation process is completed, you will have to setting your music software to use the new interface VirtualMIDISynth.

That's all!
