Very minimal ROS1 driver for dual V4L cameras.

The node itself is fairly generic (it uses gstreamer to access data the cameras from `/dev/video0` and `video1`), but I've hard-coded constants and configuration specific to our configuration with dual [Vision Components](https://www.mipi-modules.com/en/mipi-camera-modules/) IMX296 sensors attached to a Jetson Orin Nano dev kit.

To install:

```
mkdir -p camera_ws/src/
cd camera_ws/src
git clone https://github.com/apl-ocean-engineering/vc-stereo-ros.git
cd ../
catkin build
```

To run

```
source devel/setup.bash
roslaunch vc_stereo_node vc_stereo_node.launch
```

# LICENSE

The module is released under the [BSD 3-Clause license.](LICENSE)
