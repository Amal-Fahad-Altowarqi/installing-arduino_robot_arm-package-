# installing-arduino_robot_arm-package-
this is the steps of how to installing arduino_robot_arm package:

1- download ros melodic system by following the steps in the link :  http://wiki.ros.org/melodic/Installation/Ubuntu
2- creat the work space by following the steps in the link : http://wiki.ros.org/catkin/Tutorials/create_a_workspace
3- Add the “arduino_robot_arm” package to “src” folder by using the commands:
	$ cd ~/catkin_ws/src
	$ sudo apt install git
	$ git clone https://github.com/smart-methods/arduino_robot_arm 
4- Install all the dependencies by using the commands: 
	$ cd ~/catkin_ws
	$ rosdep install --from-paths src --ignore-src -r -y
	$ sudo apt-get install ros-melodic-moveit
	$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui
	$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher
	$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control
5-	Compile the package by using the command:
$ catkin_make
6-launch rviz app by using the command:
$ roslaunch robot_arm_pkg check_motors.launch
7-launch gazebo app by using the command:
$ roslaunch robot_arm_pkg check_motors_gazebo.launch


