Simply add JSoundSystem-1.1.0.jar (or any later version) to your project, right click it and add it to build path. Now you can use JSound objects to play sounds.
```
	JSound mySound = new JSound( "mysound.wav" );
	mySound.play();
```

That's it!

**MP3 Support**
If you want support for MP3 sounds you will also need to copy mp3spi1.9.5.jar and add it to your build path. This is because the MP3 decoder is not under a free license and you might not want to include it with your project