# ur5_ROS-Gazebo
Simulation of UR5 on gazebo to pick and place blocks based on the size and shape of each block to sort them.

This is the project for Introduction to Robotics The task of the project is to sort the blocks on a conveyor, pick and place each of the blocks into different place based on the weight of the block. The main goal of the robot is to pick and place task given certain inputs.

#Implementation of the task in Gazebo

Steps to start the simulation
1. Create your catkin_ws/src folder
2. Clone Universal Robots repository in the src folder
3. Cmake the folder
4. Download or clone the repository in your cakin_ws/src directory
5. Extract the ur5_ROS-Gazebo.tar.gz file
6. Once extracting is done, open a new terminal to run the simulation
7. cd ..
8. catkin_ws/source devel/setup.bash
9. catkin_ws/roslaunch ur5_notebook initialize.launch
