# Map-My-World
Project 3 of Robotics Software Engineering Nanodegree Program 

## Overview of the Project 
In this project you will create a 2D occupancy grid and 3D octomap from a simulated environment using your own robot with the RTAB-Map package.
RTAB-Map (Real-Time Appearance-Based Mapping) is a popular solution for SLAM to develop robots that can map environments in 3D. RTAB-Map has good speed and memory management, and it provides custom developed tools for information analysis. Most importantly, the quality of the documentation on ROS Wiki (http://wiki.ros.org/rtabmap_ros) is very high. Being able to leverage RTAB-Map with your own robots will lead to a solid foundation for mapping and localization well beyond this Nanodegree program.
For this project we will be using the rtabmap_ros package, which is a ROS wrapper (API) for interacting with RTAB-Map. Keep this in mind when looking at the relative documentation.

* You will develop your own package to interface with the rtabmap_ros package.
* You will build upon your localization project to make the necessary changes to interface the robot with RTAB-Map. An example of this is the addition of an RGB-D camera.
* You will ensure that all files are in the appropriate places, all links are properly connected, naming is properly setup and topics are correctly mapped. Furthermore you    will need to generate the appropriate launch files to launch the robot and map its surrounding environment.
* When your robot is launched you will teleop around the room to generate a proper map of the environment.

## What you will need to run 
* Gazebo >= 7.0
* ROS Kinetic
* ROS navigation package \
`sudo apt-get install ros-kinetic-navigation`
* ROS map_server package \
`sudo apt-get install ros-kinetic-map-server`
* ROS move_base package \
`sudo apt-get install ros-kinetic-move-base`
* ROS amcl package \
`sudo apt-get install ros-kinetic-amcl`
* ROS rtabmap-ros package
`sudo apt-get install ros-kinetic-rtabmap-ros`


## How to run 
* Open Ubuntu bash and execute the command `sudo apt-get update && sudo apt-get upgrade -y`
* Install the necessary packages 
* Clone this repository 
* Open the repository and make \
`cd /home/workspace/P3-Where-Am-I/catkin_ws/` \
`catkin_make`
* Launch my_robot in Gazebo to load both the world and plugins
`roslaunch my_robot world.launch`
* Launch teleop_twist_keyboard node, open a new terminal, enter
`cd /home/workspace/RoboND-Term1-P4-Map-My-World/catkin_ws/
source devel/setup.bash
rosrun teleop_twist_keyboard teleop_twist_keyboard.py`
* Launch teleop_twist_keyboard node, open a new terminal, enter
`cd /home/workspace/RoboND-Term1-P4-Map-My-World/catkin_ws/
source devel/setup.bash
roslaunch my_robot mapping.launch`
* Testing
Send move command via teleop package to control your robot and observe real-time visualization in the environment rtabmapviz.
`rtabmap-databaseViewer ~/.ros/rtabmap.db`

View database Once you statisfied with your move, press Ctrl + c to exit then view your database with

`rtabmap-databaseViewer ~/.ros/rtabmap.db`
Remember to rename your ~/.ros/rtabmap.db before your next attempt since it will be deleted due to the launch file setting in mapping.launch





