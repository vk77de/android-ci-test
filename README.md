# About

[![GitHub Actions Build](https://github.com/rgl/hello-world-kotlin-android/actions/workflows/build.yml/badge.svg)](https://github.com/rgl/hello-world-kotlin-android/actions/workflows/build.yml)
[![Cirrus CI Build Status](https://api.cirrus-ci.com/github/rgl/hello-world-kotlin-android.svg)](https://cirrus-ci.com/github/rgl/hello-world-kotlin-android)

This is an Hello World application for Android.

# Usage (Windows)

Install [Chocolatey](https://chocolatey.org/install).

In a cmd shell with Administrator privilege, install the dependencies:

```batch
choco install -y msys2
choco install -y androidstudio
choco install -t temurin17
```

Open Android Studio, select the `Tools / SDK Manager` menu, select the `SDK Tools` tab, select the `Android SDK Command-line Tools (latest)` tool, click `OK`.

In a msys2/mingw64 bash shell:

```bash
ANDROID_SDK_HOME="$(cygpath $LOCALAPPDATA)/Android/Sdk"
export PATH="$PATH:$ANDROID_SDK_HOME/platform-tools"
export PATH="$PATH:$ANDROID_SDK_HOME/emulator"
export PATH="$PATH:$ANDROID_SDK_HOME/cmdline-tools/latest/bin"
javac --version
adb --version
sdkmanager.bat --version
avdmanager.bat list avd
```

Build the application:

```bash
make
```
