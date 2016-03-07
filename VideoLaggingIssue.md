# Possible areas for improvement - video lag issue #

## Tasks finished ##
  * CPU specific optimized compilation (v5, v6,v6vfp, v7, neon, x86) at ndk various libraries
  * Profiling the code for identifying places using most cpu time
  * no debug print statements in release build and during video playtime - consumes time
  * set higher priority process, thread for the application
  * Remove debugging symbols and any profiling related code in release build
  * skip frames algorithm - even after optimization, time taken to decode and show a frame to screen is greater than the time required to put the frame on screen
  * read the file contents and keep in memory as much as possible (queue size)
  * use arm assembly code for yuv 2 rgb -code available
  * set optimized settings in FFmpeg for faster decoding - code available

## Doable ##
  * direct calling of opengl without going through sdl for video, audio
  * use arm assembly code for copying pixels between arrays
  * skip bidrectional frames -code available
  * 16bit or 24bit rendering based on video lag condition
  * multi threaded single frame decoding
  * multi threaded - parallel frames decoding -ffmpeg
  * Time slicing by OS for each thread(Read packets, Decode Video, Audio Thread, Put Frames to Screen thread) needs to be verified.(Whether they are given equal time slices, concurrently)
  * Process specific optimization during compilation
  * Java overhead for layout, display
  * Using surface flinger in native ??
  * Use profiler and convert heavily used methods to assembly arm/x86
  * Look at gstreamer, vlc ->looks like, they are using surface flinger
  * optimized arm compilation using the compiler from arm.com
  * Use libmedia, libsurfaceflinger\_client based output of audio and video
  * H/w decoding (stagefright framework/OMX)

## Details required ##
  * use inbuilt decoder for known file formats (avi)
  * use hardware acceleration - not available
  * using gstreamer framework ??
  * using libstagefright

# Known questions and possible answers #
  * what to do if the decoding of a frame itself is >40ms, for a frame rate of 25FPS ?  skip frames, disable audio, convert the file to a supported native file format with less FPS ??

# Suggestions #
  * Send your suggestions or any possible solutions to aatrala@gmail.com