# DexHook
DexHook is a xposed module for capturing dynamically loaded dex/jar/apk/zip files. DexHook hooks into BaseDexClassLoader and DexFile, then copies the file prior to loading to a user define path.

baseDir needs to be writable from the app you are hooking, /sdcard will work if the app can write to it.

Build and tested on Nexus 5 running Android 4.4.4 with SELinux set permissive, using dalvikvm. At this time, DexHook is untested with ART.

Usage:
Its one class, less than 100 lines of code. Read it, or don't worry about it.

v1.1
Added hook for DexFile, bringing support for DexGuard encrypted classes
Fixed path error, causing some dex files not to be written.

v1.0 - Initial release
Hook BaseDexClassLoader, capturing the loaded dex
