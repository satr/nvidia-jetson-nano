#ROS on Jetson Nano

## Setup ROS2
### Install CMake version 3.19 or above
Version of CMake, existing by default, can not supportcommand `target_link_directories`, introduced in version 3.13
Check the version: `cmake --version`

Build latest version
```
$ sudo apt install build-essential git
$ cd ~/Download
$ git clone https://github.com/Kitware/CMake/; cd CMake
$ ./bootstrap && make && sudo make install
$ cmake --version
```

### Install ROS2 Foxy

[Build ROS2 Foxy](https://index.ros.org/doc/ros2/Installation/Foxy/Linux-Development-Setup)
