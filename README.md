# Map-My-World
Project 3 of Robotics Software Engineering Nanodegree Program 

## Overview of the Project:
In this project a 2D occupancy grid and 3D octomap was created from a simulated environment a robot with the RTAB-Map package.

RTAB-Map (Real-Time Appearance-Based Mapping) is a popular solution for SLAM to develop robots that can map environments in 3D. RTAB-Map has good speed and memory management, and it provides custom developed tools for information analysis. 

## Task of the Project:
* Develop a package to interface with the rtabmap_ros package.
* Build upon your localization project to make the necessary changes to interface the robot with RTAB-Map. An example of this is the addition of an RGB-D camera.
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
`sudo apt-get install ros-kinetic-rtabmap-ros ` 


## How to run 
* Open Ubuntu bash and execute the command \
`sudo apt-get update && sudo apt-get upgrade -y`
* Install the necessary packages 
* Clone this repository 
* Open the repository and make \
`cd /(your_directory}/catkin_ws/` \
`catkin_make`
* Launch my_robot in Gazebo to load both the world and plugins
`roslaunch my_robot world.launch`
* Launch teleop_twist_keyboard node, open a new terminal, enter
`cd /{your_directory}/catkin_ws/ \
`source devel/setup.bash` \
`rosrun teleop_twist_keyboard teleop_twist_keyboard.py``
* Launch teleop_twist_keyboard node, open a new terminal, enter
`cd /{your_directory}/catkin_ws/
source devel/setup.bash
roslaunch my_robot mapping.launch`
* Testing: \
Send move command via teleop package to control your robot and observe real-time visualization in the environment rtabmapviz.
`rtabmap-databaseViewer ~/.ros/rtabmap.db`

 View database once you are statisfied with your move, press Ctrl + c to exit then view your database with `rtabmap-databaseViewer ~/.ros/rtabmap.db`
 Remember to rename your ~/.ros/rtabmap.db before your next attempt since it will be deleted due to the launch file setting in mapping.launch




# Note:
* For more information on RTAB-Map package refer [RTAB-Map](http://wiki.ros.org/rtabmap_ros).
