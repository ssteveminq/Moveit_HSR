# Moveit_HSR
moveit instructions for using HSR

## prerequisite
* The HSR Simulator
* Proper configurations files 
  * hsrb_description
  * hsrb_moveit_config

## Install the HSR simulator
You have to install HSR simulator from https://hsr.io 
(You need an approved account to access this site)
Please follow instructions 5.4.3.2 Installation of the HSR simulator.
If you are going to use multiple computers, you have to edit bashrc ( follow instruction for 5.4.3.3 .bashrc setting)

## Replace old configurations(installed) files to new configurations files (downloaded)
You should replace two above files (hsrb_description and hsrb_moveit_config) into "/opt/tmc/ros/indigo/share/".

I am not sure if the simulation need these configuration files, in order to control actual robot, you need to replace files. 

## Checking rospackage
```
$ rospack find hsrb_moveit_config
$ rospack find hsrb_description
```

## Start simulation
If you installed the simulator, the simulator may be started.

```
$ roslaunch hsrb_gazebo_launch hsrb_megaweb2015_world.launch
```
You should start the simulation for moveit to receive information from Gazebo simulation. 

At the same time, moveit can be launched with following command
```
roslaunch hsrb_moveit_config demo_with_controller.launch
```
Please check the rviz settings (Use base_link as the global frame, use hsrb_description_moveit as the value of RobotPlanning/RobotDescription)


Now, you might be ready to control HSR with moveit.






