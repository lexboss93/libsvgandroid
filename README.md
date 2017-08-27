# libsvgandroid
SVG render library for Android by Anton Persson. Based on libsvg by Carl D. Worth.

# license
libsvgandroid is released under the GNU Lesser General Public License, version 3 or later.

Please note that libsvgandroid depends on additional third party libraries that has
their own licenses. If you distribute software including or using libsvgandroid make
sure you follow lgpl v3+, and also the additional licensing requirements specified in
the third party libraries.

# requirements

 * A development host running some form of GNU/Linux (tested on Ubuntu 16.04)
 * the Android SDK
 * the Android NDK

# configure

Quick:

```
./configure --ndk-path ~/Source/Android/android-ndk --sdk-path ~/Source/Android/android-sdk-linux --target-platform android-10 --bootstrap
```

--bootstrap will download required third party libraries and cross compile them for Android.

# compiling

either:

```
make debug
```

or:

```
make release
```

# usage

Include libsvgandroid.so as a prebuilt shared library in your Android.mk file. Please refer to the
Android NDK documentation for information about specifics.

Include libsvgandroid.jar in your libs directory. Please refer to the Android SDK documentation for
information about specifics.

# Preparing environment
Tested on Ubuntu 16.04 TLS 64-bit

1. Install Android Studio<br/>
I installed version ide-162.4069837.

2. Then, as described in installation guide https://developer.android.com/studio/install.html<br/>
run command:<br/>
sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386<br/>

3. Install Android NDK<br/>
I installed version r10e from <br/>
https://dl.google.com/android/repository/android-ndk-r10e-linux-x86_64.zip<br/>
because had problems with the latest one.

4. Install Java<br/>
sudo apt-get install openjdk-8-jdk

5. Downgrade android tools to version 25.2.3<br/>
https://dl.google.com/android/repository/tools_r25.2.3-linux.zip<br/>
Remove original tools folder or rename to "tools-backup"<br/>
Extract to $(Android-Sdk)

6. Install Apache Ant<br/>
sudo apt install ant
