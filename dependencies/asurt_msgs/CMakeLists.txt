cmake_minimum_required(VERSION 3.0.2)
project(asurt_msgs)

find_package(catkin REQUIRED COMPONENTS message_generation roscpp rospy
                                        std_msgs geometry_msgs sensor_msgs)

# Generate messages in the 'msg' folder
add_message_files(FILES Landmark.msg LandmarkArray.msg NodeStatus.msg)

# Generate added messages and services with any dependencies listed here
generate_messages(DEPENDENCIES std_msgs geometry_msgs asurt_msgs sensor_msgs)

# ##############################################################################
# catkin specific configuration ##
# ##############################################################################
# The catkin_package macro generates cmake config files for your package Declare
# things to be passed to dependent projects INCLUDE_DIRS: uncomment this if your
# package contains header files LIBRARIES: libraries you create in this project
# that dependent projects also need CATKIN_DEPENDS: catkin_packages dependent
# projects also need DEPENDS: system dependencies of this project that dependent
# projects also need
catkin_package(CATKIN_DEPENDS message_generation roscpp rospy std_msgs)

# ##############################################################################
# Build ##
# ##############################################################################

# Specify additional locations of header files Your package locations should be
# listed before other locations
include_directories(# include
                    ${catkin_INCLUDE_DIRS})
