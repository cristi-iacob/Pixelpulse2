## Pixelpulse2

[![Windows Status](https://ci.appveyor.com/api/projects/status/32r7s2skrgm9ubva?svg=true)](https://ci.appveyor.com/project/analogdevicesinc/pixelpulse2/branch/master)
[![OSX Status](https://api.travis-ci.org/analogdevicesinc/Pixelpulse2.svg?branch=master&label=OSX)](https://travis-ci.org/analogdevicesinc/Pixelpulse2)
[![License](https://img.shields.io/badge/license-MPL-blue.svg)](https://github.com/analogdevicesinc/Pixelpulse2/blob/master/LICENSE)

Pixelpulse is a powerful user interface for visualizing and manipulating signals while exploring systems attached to affordable analog interface devices, such as Analog Devices' ADALM1000.

Fully cross-platform using the Qt5 graphics toolkit and OpenGL accelerated density-gradiated rendering, it provides a powerful and accessible tool for initial interactive explorations.

Intuitive click-and-drag interfaces make exploring system behaviors across a wide range of signal amplitudes, frequencies, or phases a trivial exercise. Just click once to source a constant voltage or current and see what happens. Choose a function (sawtooth, triangle, sinusoidal, square) - adjust parameters, and make waves.

Zoom in and out  with your scroll wheel or multitouch gestures (on supported platforms). Hold "Shift" to for Y-axis zooming.

Click and drag the X axis to pan in time.

### Screenshot

![Screenshot of PP2 on Windows 7](https://analogdevicesinc.github.io/Pixelpulse2/pp2screenshot.png "Pixelpulse on Windows 7")

### Getting Pixelpulse2

#### Easy

* OSX - Navigate to the [releases](https://github.com/analogdevicesinc/pixelpulse2/releases) and collect the latest `pixelpulse2-bundled.dmg.zip` package. The latest testing build is available from [Travis-CI](http://pixelpulse2nightly.s3-website-us-east-1.amazonaws.com/pixelpulse2.dmg).
* Windows - For a testing build, download the dependency package and the latest binary build from [appveyor](https://ci.appveyor.com/project/analogdevicesinc/pixelpulse2/build/artifacts). For an official release build, navigate to releases and collect the latest pixelpulse2-setup.exe.
* Linux - Build from source (below) 

#### Installation for Linux

1. Dependencies installation.

The following command should install all the needed dependencies. Note that the packages' names may vary on different platforms. However, the following packages are tested and functional on Ubuntu 16, 18 and 20.

```shell
analog@analog:~$ sudo apt-get update
analog@analog:~$ sudo apt-get install -y git cmake g++ qt5-default qttools5-dev qtdeclarative5-dev libqt5svg5-dev libqt5opengl5-dev libqt5qml5 libqt5quick5 libqt5network5 qml-module-qtgraphicaleffects qml-module-qt-quick-layouts qml-module-qtquick-controls qml-module-qtquick-dialogs qml-module-qt-labs-settings qml-module-qt-labs-folderlistmodel qml-module-qtqml-models2
```

2. Install libsmu. More information [here](https://github.com/analogdevicesinc/libsmu). You can directly install the corresponding .deb packages.

3. Build and install Pixelpulse2.

```shell
analog@analog:~$ git clone https://github.com/analogdevicesinc/Pixelpulse2
analog@analog:~$ cd pixelpulse2
analog@analog:~$ mkdir build
analog@analog:~$ cd build
analog@analog:~$ cmake ..
analog@analog:~$ make
analog@analog:~$ sudo make install
```
