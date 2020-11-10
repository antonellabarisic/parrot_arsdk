# parrot_arsdk

This is a [catkin](http://wiki.ros.org/catkin) wrapper for the [official Parrot ARSDK3](https://github.com/Parrot-Developers/arsdk_manifests).

## Build status

[![Build Status](https://travis-ci.org/AutonomyLab/parrot_arsdk.svg?branch=indigo-devel)](https://travis-ci.org/AutonomyLab/parrot_arsdk)

## Installation instructions

Parrot_arsdk

```
cd ~/bebop_ws/src
git clone git@github.com:antonellabarisic/parrot_arsdk.git
git checkout noetic_dev
sudo apt-get install libavahi-client-dev
sudo ln -s /usr/bin/python3 /usr/bin/pyhton
cd ..
catkin_make
```

Bebop autonomy
```
cd ~/bebop_ws/src
git clone https://github.com/AutonomyLab/bebop_autonomy.git
```
Modify /bebop_driver/src/bebop_video_decoder.cpp
- line 93: CODEC_AP_TRUNCATED -> AV_CODEC_AP_TRUNCATED
- line 95: CODEC_FLAG_TRUNCATED -> AV_CODEC_FLAG_TRUNCATED
- line 97: CODEC_FLAG2_CHUNKS -> AV_CODECO_FLAG2_CHUNKS
```
cd ..
catkin_make
```
