cmake_minimum_required(VERSION 2.8.3)
project(force_keyboard_py)

find_package(catkin REQUIRED COMPONENTS
  rospy
  geometry_msgs
)

catkin_package(
  INCLUDE_DIRS src
  CATKIN_DEPENDS rospy geometry_msgs
)

include_directories(${catkin_INCLUDE_DIRS})

add_executable(force_keyboard src/force_keyboard.py)
target_link_libraries(force_keyboard ${catkin_LIBRARIES})

