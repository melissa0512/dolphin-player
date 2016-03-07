I'm trying to build dolphin player, and I get this:

jni/jpeg/jidctfst.S: Assembler messages:
jni/jpeg/jidctfst.S:66: Error: missing ')'
jni/jpeg/jidctfst.S:66: Error: garbage following instruction -- `pld ([r2](https://code.google.com/p/dolphin-player/source/detail?r=2),#0)'
jni/jpeg/jidctfst.S:259: Error: missing ')'
jni/jpeg/jidctfst.S:259: Error: garbage following instruction -- `pld (sp,#32)'
jni/jpeg/jidctfst.S:271: Error: missing ')'
jni/jpeg/jidctfst.S:271: Error: garbage following instruction -- `pld (ip,#32)'
make: **[obj/local/armeabi-v7a/objs/jpeg/jidctfst.o] Error 1**


Solution suggested by one of our Developers:

the PLD lines should read

PLD     [[r2](https://code.google.com/p/dolphin-player/source/detail?r=2), #0]

and not

PLD     ([r2](https://code.google.com/p/dolphin-player/source/detail?r=2), #0)