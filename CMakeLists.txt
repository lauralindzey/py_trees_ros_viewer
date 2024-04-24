cmake_minimum_required(VERSION 3.0.2)

project(py_trees_ros_viewer)
set(CMAKE_CXX_FLAGS "-g ${CMAKE_CXX_FLAGS}")
# Load catkin and all dependencies required for this package
find_package(catkin REQUIRED py_trees_ros_interfaces )
catkin_package()
catkin_python_setup()

#install(FILES plugin.xml
  #DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
#)

install(PROGRAMS scripts/py-trees-devel-viewer
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
