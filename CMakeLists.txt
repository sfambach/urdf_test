cmake_minimum_required(VERSION 3.0.2)
project(urdf_test)
find_package(catkin REQUIRED)
catkin_package()

#install(DIRECTORY images meshes launch rviz urdf
install(DIRECTORY launch urdf rviz
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

#############
## Testing ##
#############

if(CATKIN_ENABLE_TESTING)
  find_package(roslaunch REQUIRED)
  roslaunch_add_file_check(launch)
endif()

