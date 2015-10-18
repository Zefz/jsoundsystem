Simply add JSoundSystem-1.2.0.jar to your project, right click it and add it to build path.
Now you can use JSound objects to play sounds.
```
	JSound mySound = new JSound( "mysound.wav" );
	mySound.play();
```
That's it!


JSoundSystem currently supports the following audio formats:
  * WAV
  * MP3 (note you have to copy mp3spi1.9.5.jar for MP3 support)
  * OGG
  * FLAC
  * AIFF
  * AU
  * AIFC
  * SND

JSoundSystem is licensed under the New BSD and implements some SPI libraries from JavaZoom to decode OGG and MP3 sound files.


---

**License Update (28.07.14)**

The JSoundSystem is now released under the New BSD License. This license is less restrictive and allows you to release your project without making it open source. It is therefore applicable for commercial projects as well! It is still considered common courtesy to link or credit back to the JSoundSystem if you use it in your project.

**Latest Release: 1.2.0 (07.12.10):**
  * NEW FEATURE: Added new JMusic object that streams audio instead of loading them into memory. This is useful for large sound files like music that take time to load into memory.
  * NEW FEATURE: Added new clone() and getAudioFormat() methods for JSound objects. The clone() method can be used to duplicate and play the same sound in different threads while only loading the sound into memory once.
  * UPDATE: JSoundSystem now properly uses actual 3d vectors for positions instead of 2d.
  * UPDATE: Renamed the package to accommodate with the Java standard convention.
  * UPDATE: Large optimizations by loading whole sounds into memory instead of keeping open data streams.
  * UPDATE: Various other optimizations.
  * BUGFIX: Fixed possible null pointer exception when using JSound3D