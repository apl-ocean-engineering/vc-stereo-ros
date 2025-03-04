cmake_minimum_required(VERSION 3.0.2)
project(vc_stereo_ros)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
              cv_bridge
              rospy )

## System dependencies are found with CMake's conventions
# find_package(Boost REQUIRED COMPONENTS system)

catkin_python_setup()

## Generate dynamic reconfigure parameters in the 'cfg' folder
# generate_dynamic_reconfigure_options(
#   cfg/DynReconf1.cfg
#   cfg/DynReconf2.cfg
# )

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES vc_stereo_ros
#  CATKIN_DEPENDS other_catkin_pkg
#  DEPENDS system_lib
)


## Mark executable scripts (Python etc.) for installation
## in contrast to setup.py, you can choose the destination
catkin_install_python(PROGRAMS
   nodes/vc_stereo_node
   DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)


## Mark other files for installation (e.g. launch and bag files, etc.)
# install(FILES
#   # myfile1
#   # myfile2
#   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
# )
