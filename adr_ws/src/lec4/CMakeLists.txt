cmake_minimum_required(VERSION 3.0.2)
project(lec4)


find_package(catkin REQUIRED COMPONENTS
  cv_bridge
  image_transport
  nav_msgs
  roscpp
  rospy
  sensor_msgs
)

find_package(OpenCV REQUIRED)

catkin_package(

)

###########
## Build ##
###########

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

add_executable(exp4_feature_detector
  src/exp4_feature_detector.cpp
  src/feature_detector.cpp
)
target_link_libraries(exp4_feature_detector
  ${catkin_LIBRARIES}
  ${OpenCV_LIBRARIES})