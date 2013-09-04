cmake_minimum_required(VERSION 2.8.3)
project(pick_and_place_msgs)
find_package(catkin REQUIRED COMPONENTS actionlib_msgs
                                        geometry_msgs
                                        message_generation
                                        std_msgs)

#add_message_files(DIRECTORY msg
#                  Files     ...)

add_action_files(DIRECTORY action
                 FILES     FindObject.action
                           MoveArm.action
                           MoveGripper.action
                           PickObject.action
                           PlaceObject.action)

generate_messages(DEPENDENCIES actionlib_msgs
                               geometry_msgs
                               std_msgs)

catkin_package(CATKIN_DEPENDS actionlib_msgs
                              geometry_msgs
                              message_runtime
                              std_msgs)
                              

