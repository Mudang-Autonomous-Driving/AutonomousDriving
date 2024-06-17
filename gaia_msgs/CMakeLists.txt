cmake_minimum_required(VERSION 2.8.3)
project(gaia_msgs)

add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  rosgraph_msgs
  geometry_msgs
  std_msgs
)

add_message_files(
  FILES
    DetectedCone.msg
    DetectedConeArray.msg
)

generate_messages(DEPENDENCIES
  rosgraph_msgs
  geometry_msgs
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS
    message_runtime
    rosgraph_msgs
    geometry_msgs
    std_msgs
)
