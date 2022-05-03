cmake_minimum_required(VERSION 3.1 FATAL_ERROR)
project(mission_srvs)

# Catkin dependencies
find_package(catkin REQUIRED COMPONENTS roscpp sensor_msgs geometry_msgs nav_msgs std_msgs message_generation)

# Generate services in the 'srv' folder
add_service_files(
  FILES
  StartSweep.srv
  StartVerticalInspection.srv
  GoToPoint.srv
  SavePoint.srv
)

# Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs  # Or other packages containing msgs
)

# Defining the package
catkin_package(
    INCLUDE_DIRS 
    LIBRARIES 
    CATKIN_DEPENDS roscpp sensor_msgs geometry_msgs nav_msgs message_runtime
    DEPENDS
)
