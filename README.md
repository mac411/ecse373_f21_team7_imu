# ecse373_f21_team7_imu
This README will describe how to use the ```imu``` ROS package. There are three provided launch files to be used for various purposes as described below. You may notice ```navvis.launch``` inside the ```launch``` directory, but this was only included so as to make the submission easier to test and should not be used to launch this package.

## Prerequisites
Please ensure Ubuntu 18.04 and ROS Melodic (or appropriate equivalent) is installed. Create a new catkin workspace and clone this package as well as the ```navvis_description``` package into the ```src``` directory. Then, you may use the following launch commands.

## Launching the standalone robot in RVIZ
Run ```roslaunch imu robot.launch``` at the command line.<br>This will display the navvis robot in RVIZ as done in the previous lab.
### Arguments 
The following arguments may be added to the end of the launch command for their described purposes.<br><br>
```use_sim_time:=<true|false>```. Optional. False by default. Specifies whether or not ROS should use an external clock signal. Should be kept as false unless you specify your own signal.<br>
```use_robot_state_publisher:=<true|false>```. Optional. True by default. Specifies whether the robot_state_publisher should be used or not.

## Launching the robot with laser scans in RVIZ
Run ```roslaunch imu robot_and_bag.launch``` at the command line.<br>This will display the navvis robot in RVIZ as well as the sensor readings from the provided bag file. This launch file requires the ```bag_file``` argument to be specified.
### Arguments 
The following arguments may be added to the end of the launch command for their described purposes.<br><br>
```use_sim_time:=<true|false>```. Optional. True by default. Specifies whether or not ROS should use an external clock signal. Should be kept true unless you intend to specify another clock signal.<br>
```use_robot_state_publisher:=<true|false>```. Optional. True by default. Specifies whether the robot_state_publisher should be used or not. Not really required because the bag file will have all the transform messages regardless.<br>
```bag_file:=<absolute_path>```. Required. Tells the launch file the where the bag file you want to play is located.

## Launching the robot with laser scans and map in RVIZ
Run ```roslaunch imu robot_and_bag_and_map.launch``` at the command line.<br>This will display the navvis robot in RVIZ as well as the sensor readings from the provided bag file and map from the provided map file. This launch file requires the ```bag_file``` and ```map_file``` arguments to be specified.
### Arguments 
The following arguments may be added to the end of the launch command for their described purposes.<br><br>
```use_sim_time:=<true|false>```. Optional. True by default. Specifies whether or not ROS should use an external clock signal. Should be kept true unless you intend to specify another clock signal.<br>
```use_robot_state_publisher:=<true|false>```. Optional. True by default. Specifies whether the robot_state_publisher should be used or not. Not really required because the bag file will have all the transform messages regardless.<br>
```bag_file:=<absolute_path>```. Required. Tells the launch file the where the bag file you want to play is located.<br>
```map_file:=<absolute_path>```. Required. Tells the launch file the where the map file you want to display is located.
