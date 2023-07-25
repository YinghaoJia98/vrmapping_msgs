cmake_minimum_required(VERSION 3.5.1)
project(vrmapping_msgs)

# # Find catkin macros and libraries
find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  geometry_msgs
  message_generation
)

# ######################################
# # Declare ROS messages and services ##
# ######################################

# # Generate messages in the 'msg' folder
add_message_files(
  FILES
  VarmappingMap.msg
)

add_service_files(
  FILES
  VarmappingPubTarget.srv
)

# # Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

# ##################################
# # catkin specific configuration ##
# ##################################
# # The catkin_package macro generates cmake config files for your package
# # Declare things to be passed to dependent projects
# # INCLUDE_DIRS: uncomment this if you package contains header files
# # LIBRARIES: libraries you create in this project that dependent projects also need
# # CATKIN_DEPENDS: catkin_packages dependent projects also need
# # DEPENDS: system dependencies of this project that dependent projects also need
catkin_package(

  # INCLUDE_DIRS include
  # LIBRARIES
  CATKIN_DEPENDS
  geometry_msgs
  message_runtime
  std_msgs

  # DEPENDS
)
