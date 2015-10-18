**Basic Audio Effects**

The JSoundSystem supports various simple effects you can add to your sound. This includes simulated 3D sounds or playback speed or something as basic as volume or panning.
```
	JSound mySound = new JSound( "mysound.ogg" );
	mySound.setVolume( 0.75f );
	mySound.setSpeed( 2.00f );
	mySound.setLoop( true );
	mySound.play();
```
The sound will now play at double speed with 25% less volume in an infinite loop until you call mySound.stop() or mySound.pause().



---


**3D Sound Emulation**

3D sound emulation works is done through the JSound3D object. Note that changing volume or panning for JSound3D objects won't do anything useful because this handled automatically by the JSoundSystem. To use a JSound3D you need first to set positions of the listener, position of the source and the maximum hearing distance. Setting the position of the listener usually only needs to be done once unless you change who is the listener.

```
	//Setup positions of the listener and source
	//Setup positions of the listener and source
	Vector3f listenerPosition = new Vector3f( 400, 300, 0 ); //X, Y, Z positions for the listener
	Vector3f sourcePosition = new Vector3f( 200, 150, 0 );	//X, Y, Z positions for the source

	//Initialize the listener, this only needs to be done once
	JSoundSystem.setMaxDistance( 800 );
	JSoundSystem.setListenerPosition( listenerPosition );
	
	//Now load and play the audio file
	File myAudioFile = new File( "mysound.mp3" );
	JSound3D my3dSound = new JSound3D( myAudioFile );
	my3dSound.setSourcePosition( sourcePosition );
	my3dSound.setLoop(true);
	my3dSound.play();
```

The 3D emulation in the JSoundSystem currently uses Vector3f as the position for the source and listener. For 3D sounds to be automatically updated when either your listener or source moves, you need to make sure that any movement that is done is also done to listenerPosition and sourcePosition variables. You do not need to reset the positions each time you move if you have referenced the Vector3f variable correctly..