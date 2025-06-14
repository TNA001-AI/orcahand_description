cmake_minimum_required(VERSION 3.10)
project(orcahand_description)

message(STATUS "Detected ROS 2")

find_package(ament_cmake REQUIRED)
find_package(urdf REQUIRED)
find_package(xacro REQUIRED)

install(DIRECTORY urdf/
  DESTINATION share/${PROJECT_NAME}/urdf
)

install(DIRECTORY assets/
  DESTINATION share/${PROJECT_NAME}/assets
)

install(DIRECTORY launch
  DESTINATION share/${PROJECT_NAME}/launch
)

install(DIRECTORY rviz/
  DESTINATION share/${PROJECT_NAME}/rviz
)

ament_package()
