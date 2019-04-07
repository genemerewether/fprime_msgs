cmake_minimum_required(VERSION 2.8.3)
project(fprime_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs actionlib_msgs
  )

add_action_files(
  DIRECTORY action
  FILES CmdSeq.action
)

generate_messages(
  DEPENDENCIES actionlib_msgs std_msgs
)

catkin_package(
  CATKIN_DEPENDS
  std_msgs actionlib_msgs
)
