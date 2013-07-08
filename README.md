ntpclient-android
=================

This is a forked copy of Larry Doolittle's ntpclient program, forked and
hacked in a few ways to work on Android and FirefoxOS devices.

# Requirements

* To build, you'll need a copy of the Android NDK. You can get a copy from:

    http://developer.android.com/sdk/ndk/index.html

* To run, any rooted device running Android or FirefoxOS should work

# Building / Installing

Assuming you have installed the Android NDK, you can configure and build
Orangutan by running:

    ./configure $PATH_TO_ANDROID_NDK
    make

For example, on my machine I downloaded and extracted the NDK to
$HOME/opt/android-ndk-r6. So In my case I would run:

    ./configure $HOME/opt/android-ndk-r6
    make

To install on your device (assuming it's connected via USB and developer mode
is enabled), run:

    make push

# Running

See README.orig for detailed usage information. To simply synchronize your
Android/FirefoxOS device with a central time server (the primary rationale
behind this version of the utility), you can do something like:

    adb shell su -c '/data/local/ntpclient -c 1 -d -h pool.ntp.org -s'
