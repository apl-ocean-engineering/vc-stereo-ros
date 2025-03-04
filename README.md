Minimalist ROS1 camera driver for stereo cameras.

To install:

```
mkdir -p camera_ws/src/
cd camera_ws/src
git clone git@github.com:apl-ocean-engineering/vc-stereo-ros.git
cd ../
catkin build
```

To run

```
source devel/setup.bash
roslaunch vc_stereo_node vc_stereo_node.launch
```
