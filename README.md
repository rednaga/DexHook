# DexHook
DexHook is a [xposed module](https://github.com/rovo89/XposedInstaller) for capturing dynamically loaded dex/jar/apk/zip files. DexHook hooks into `BaseDexClassLoader` and `DexFile`, then copies the file prior to loading to a user define path.

`baseDir` needs to be writable from the app you are hooking, `/sdcard` will work if the app can write to it.

Build and tested on Nexus 5 running Android 4.4.4 with SELinux set permissive, using DalvikVM. At this time, DexHook is untested with ART.

Usage
------
Its one class, less than 100 lines of code. Read it, or don't worry about it.


Revision History
----------------
v1.1
 - Added hook for DexFile, bringing support for DexGuard encrypted classes
 - Fixed path error, causing some dex files not to be written.

v1.0 (Initial release)
 - Hook BaseDexClassLoader, capturing the loaded dex

License
-------
    The MIT License (MIT)
    
    Copyright (c) 2015 Red Naga
    
    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.
