# ur5_ROS-Gazebo
Simulation of UR5 on gazebo to pick and place blocks based on the size and shape of each block to sort them.

This repository demonstrates the project for Introduction to Robotics. The task of the project is to sort the blocks on a conveyor, pick and place each of the blocks into different place based on the weight of the block. The main goal of the robot is to pick and place task given certain inputs. The robot used for the project is UR5 from universal robots. UR5 uses a USB cam to detect the red or blue box on the conveyor using (ur5_vision.py) and it publishes its position. The UR5 then plans its motions using the node ur5_mp.py to follow the box. Once the position of the gripper is close to the box, it will turn on the gripper. The vacuum grippers provided by the gazebo plugin provide only limited force, so we must append multiple grippers in order to lift the blocks.

#Implementation of the task in Gazebo

This code was tested for ROS-kinetic Ubuntu 16.04, so $ROS_DISTRO should be replaced with kinetic

Steps to start the simulation
1. Create your catkin_ws/src folder
2. The catkin_ws folder is attached, so one can download the given file.
3. In the src folder, we should be adding the following files: universal_robot driver and AWS_robotics/aws-robomaker-small-warehouse-world
4. This can be done by using the following two lines of code in the terminal, once you are in the src folder, i.e catkin_ws/src
5. git clone -b $ROS_DISTRO-devel https://github.com/aws-robotics/aws-robomaker-small-warehouse-world.git
6. git clone -b $ROS_DISTRO-devel https://github.com/ros-industrial/universal_robot.git
7. Once you are done cloning the files, we should be making some modifications to the Universal Robot drivers, to make changes in the our UR5_Robot
8. Download the universal_robot_replace and replace it in the universal_robot folder in the src
9. Go back to catkin_ws and catkin_make
10. Once extraction and compilising is done, open a new terminal to run the simulation
15. catkin_ws/source devel/setup.bash
16. catkin_ws$ roslaunch ur_gazebo ur5_initialize.launch


Youtube Simulation Link: https://www.youtube.com/watch?v=bSLL_NA9660
