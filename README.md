# parrot_arsdk

This is a [catkin](http://wiki.ros.org/catkin) wrapper for the [official Parrot ARSDK3](https://github.com/Parrot-Developers/arsdk_manifests).

## Build status

[![Build Status](https://travis-ci.org/AutonomyLab/parrot_arsdk.svg?branch=indigo-devel)](https://travis-ci.org/AutonomyLab/parrot_arsdk)

## Installation instructions

Parrot_arsdk

```
cd <path_to_your_catkin_ws>/src
git clone https://github.com/antonellabarisic/parrot_arsdk.git
cd parrot_arsdk
git checkout noetic_dev
sudo apt-get install libavahi-client-dev
sudo ln -s /usr/bin/python3 /usr/bin/python
cd <path_to_your_catkin_ws>
catkin_make
```

Bebop autonomy
```
cd <path_to_your_catkin_ws>/src
git clone https://github.com/AutonomyLab/bebop_autonomy.git
```
Modify /bebop_driver/src/bebop_video_decoder.cpp
- line 93: CODEC_AP_TRUNCATED -> AV_CODEC_CAP_TRUNCATED
- line 95: CODEC_FLAG_TRUNCATED -> AV_CODEC_FLAG_TRUNCATED
- line 97: CODEC_FLAG2_CHUNKS -> AV_CODEC_FLAG2_CHUNKS


Add this line in your ~/.bashrc :
```
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:<path_to_your_catkin_ws>/devel/lib/parrot_arsdk
```
Install the following:
```
sudo apt install ros-noetic-joy ros-noetic-joy-teleop ros-noetic-teleop-twist-joy
```
Build:
```
cd ..
catkin_make
```
