# ROS Workspace
This is the ROS workspace which contains all of the projects needed for the
robo_guide object tracking.

The repository uses submodules to pull in all of the projects so this command
for cloning:

`git clone --recursive https://github.com/Tuebel/robo_guide_ws`

# Dependencies
The projects build on top of each and can be built in one source tree since they
are catkin and cmake packages. There are quite a few dependencies which have to
be installed most can be installed via the usual cmake process:
```
mkdir build
cd build
cmake ..
sudo make install
```

# ROS
- [ROS-Desktop](http://wiki.ros.org/melodic) Install (for catkin, messages, nodes, ...)
- [tf2_geometry_msgs](http://wiki.ros.org/tf2_geometry_msgs) for conversion of tf2 messages. Install via apt.

## Math
- Eigen3 linear algebra (installed with [ROS-Desktop](http://wiki.ros.org/melodic))
- tf2_ros for transformation pub/sub and calculatiion (installed with [ROS-Desktop](http://wiki.ros.org/melodic))

## Images
- cv_bridge for image conversion (installed with [ROS-Desktop](http://wiki.ros.org/melodic))
- image_transport for image pub/sub (installed with [ROS-Desktop](http://wiki.ros.org/melodic))
- OpenCV for image storage and manipulation (installed with [ROS-Desktop](http://wiki.ros.org/melodic))
- aruco for marker detection
- cv_camera simple camera publisher (for ROS Melodic install the camera_info_manager package first and then build cv_camera from source)

## Rendering
- OpenGL (at least 4.2) for rendering on GPU
- [gl3w](https://github.com/skaslev/gl3w) loading the OpenGL core functions
- [glfw3](https://www.glfw.org/) platform independent OpenGL context creation
- [glm](https://glm.g-truc.net/) linear algebra for OpenGL shaders
- [assimp](http://www.assimp.org/) 3D model loading

## Unit testing
- [googletest](https://github.com/google/googletest)

# Build
In the past Ubuntu 16.04 and ROS Kinetic were used, which should still work.
Right now Ubuntu 18.04 an ROS Melodic are in use and tested.

Since this is a mixed catkin & cmake workspace, the easiest and fastest way is
to use the [catkin tools](https://catkin-tools.readthedocs.io/en/latest/) or the
newer [colcon build](https://colcon.readthedocs.io/en/latest/user/quick-start.html).

I use some recent CMake commands in the cmake projects so make sure you have a recent
version (**CMake >= 3.12**, also see [this](https://answers.ros.org/question/293119/how-can-i-updateremove-cmake-without-partially-deleting-my-ros-distribution/)).
