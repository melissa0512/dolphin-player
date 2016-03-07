**List of tasks pending in Dolphin Player**

# Bugs #
  * Hide status bar in ICS when playing audio/video file
  * Changing aspect ratio, clear the screen
  * video lagging problem - Better frame skip algorithm/ optimized playing of videos (for eg., playing compressed videos like mkv)
> (Need to study the following links for improvement:
> http://www.gamedev.net/topic/370896-playing-back-video-with-sdl/
> iffplay.googlecode.com/files/ffplay.c
> https://github.com/frankandrobot/FFvideoLiveWallpaper

# Enhancements #
  * plugin support
  * Change audio streams, subtitle stream of a video file in run time
  * Brightness, Volume and Seek using Gesture control
  * check for mobile model while running, download the relevant ffmpeg from internet or ask user to place the proper so file in the sdcard. Load the same accordingly
  * Integrating libsdl 1.3 - Hardware accelerated video output
  * Portrait view
  * Hardware acceleration decoding videos - stagefright/openmax/inbuilt codec -opencore
  * FileManager - Auto search videos and audios and show in list
  * FileManager - Recently played audios, videos
  * File manager - video thumbnail support
  * Audio enhancement plugins - Fast playing, Slow playing, Audio amplifications, SRS
  * playing HD videos
  * Better, Pleasing look & feel UI
  * Showing current time, dragged by User in Seek bar
  * Exposing the player engine as a Service
  * DLNA support
  * Shoutcast radio support
  * Providing the player as an Android service   external libraries

# Futuristic features #
  * Speech recognition for player controls `[Ongoing`]
  * Create playlist based on current user emotions, interest

# Research #
  * Various GUI Modifications can be tried out (for eg., New User Interfaces like Clutter UI) to present a better file manager
  * Optimization based on the type of the cpu features(v5,v6,v7, v7neon) available on a given device

# Minor #
  * Eliminating unnecessary modules and code to reduce the size of the Player
  * Keyboard support
  * Widget support
  * Notifications ??

# Closed Items #
  * On incoming call, pause the player (audio/video) - fixed
  * Put all types of print(C,Java) in a Debug define. Remove any sort of print in Release code)
  * support for video streams and audio streams - Use .astream, .vstream file having the first line as the URL link
  * audio and video files intent support (support for opening from other file managers and applications)
  * 3gp audio not playing properly
  * support for translations - arabic, indonesian, portugese, spanish, thai, vietnamese
    * Integrating latest FFmpeg with all codecs, gpl(xvid,x264,theora,..) for V5, V6, V6VFP, V7, V7Neon, X86
