Dexed DX7 Software Emulator
===========================

Dexed is a multi platform, multi format plugin synth that is closely modeled on the Yamaha DX7. 
Under the hood, it uses [music-synthesizer-for-android](https://code.google.com/p/music-synthesizer-for-android) 
for the synth engine and [JUCE](http://wwww.juce.com) as a plugin wrapper.

The goal of this project is to be a great tool/companion for the original DX7. Yes, the sound engine 
with 'float' values parameter; different waveform (à la TX81z) would be great but anything that 
goes beyond the DX7 should will be a fork of this project. This is to keep the compatiblity with
the original synth.

Dexed is licensed on the GPL v2. The msfa component (acronym for music synthesizer for android, see msfa 
in the source folder) stays on the Apache 2.0 license to able to collaborate between projects.

Features 
--------
* Multi platform (OS X, Windows, Linux) and multi format (VST, AU and others that I don't use); by using JUCE
* The sound engine [music-synthesizer-for-android](https://code.google.com/p/music-synthesizer-for-android) is closely modeled on the original DX7 characteristics
* All of the 144 DX7 parameters are available from one single panel
* Fully supports DX7 input and output Sysex messages; including controller change. This means that you can use this with a native DX7/TX7 as a patch editor
* Each operator have a realtime VU meter to know wich one is active
* Can load any DX7/TX7 sysex programs

Binary downloads
----------------
It is far from finished but for those who want to try the "music-synthesizer-for-android" project
on a PC/Mac, you can download it [here](http://le-son666.com/software/dexed).

Using as a DX7 editor
---------------------
This plugin can process original DX7 messages. If you change a parameter, it will send the 
corresponding DX7 sysex to midi out. Not all DAW supports sysex; for example
Ableton Live simply discard any sysex data. Reaper does process midi out, but doesn't pass any
midi in sysex input data to the plugin. 

Randomized programs
-------------------
Dexed doesn't check the sysex checksum so you can load any type of files. If the checksum doesn't 
match, it will tell you but load it anyway. This features enable a somekind of randomized DX 
programs.

TODO - Dexed 
------------
* Implement a better DX look and feel (amp, pitch, algo)
* Better implementation of the LPF filter
* Various code cleanup

TODO - msfa
-----------
* LFO Amplitude
* MOD Wheel action
* Algo 4 & 6 feedback