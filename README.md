# ROS Workspace
This is the ROS workspace which contains all of the projects needed for the
robo_guide object tracking.

The repository uses submodules to pull in all of the projects so this command
for cloning:

`git clone --recursive https://github.com/Tuebel/robo_guide_ws`

# Dependencies
The projects build on top of each and can be built in one source tree since they
are catkin and cmake packages. Additional dependencies are:

# ROS
- ROS Desktop Install (for catkin, messages, nodes, ...)

## Math
- Eigen3 linear algebra
- tf2_ros for transformation pub/sub and calculatiion

## Images
- cv_bridge for image conversion
- image_transport for image pub/sub
- OpenCV for image storage and manipulation
- aruco for marker detection
- cv_camera simple camera publisher

## Rendering
- OpenGL (at least 4.2) for rendering on GPU
- gl3w loading the OpenGL core functions
- glfw3 platform independent OpenGL context creation
- glm linear algebra for OpenGL shaders
- assimp 3D model loading

# Build
Since this is a mixed catkin & cmake workspace, the easiest and fastest way is
to use the [catkin tools](https://catkin-tools.readthedocs.io/en/latest/) or the
newer [colcon build](https://colcon.readthedocs.io/en/latest/user/quick-start.html).
