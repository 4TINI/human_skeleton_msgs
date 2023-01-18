cmake_minimum_required(VERSION 3.4)
project(human_skeleton_msgs)

find_package(catkin REQUIRED COMPONENTS 
    rospy
    message_generation 
    geometry_msgs
)

add_message_files(FILES Pixel.msg BodyPart.msg Skeleton.msg SkeletonArray.msg)

generate_messages(DEPENDENCIES geometry_msgs)

catkin_package(CATKIN_DEPENDS 
    rospy
    message_runtime 
    geometry_msgs
)

## Install
catkin_install_python(PROGRAMS 
                      
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION} 
)
