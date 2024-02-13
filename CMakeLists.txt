cmake_minimum_required(VERSION 3.5)
project(example_custom_drone)

set(CATKIN_DEPENDENCIES
  cmake_modules
  mrs_uav_gazebo_simulation 
  gazebo_ros
  )

find_package(catkin REQUIRED COMPONENTS
  ${CATKIN_DEPENDENCIES}
  )

catkin_package(
  CATKIN_DEPENDS ${CATKIN_DEPENDENCIES}
  )

## --------------------------------------------------------------
## |                           Install                          |
## --------------------------------------------------------------

install(DIRECTORY models/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/models
  )
