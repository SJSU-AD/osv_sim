# osv_sim
A simulation repository for the OSV platform.

RUN:   
```roslaunch fusion_ad_sim demo.launch```







Known Possible Error or Missing Package:   
```sudo apt-get ros-kinetic-fake-localization```


INSTALLING GAZEBO 8 on a Machine with ROS installed.
Follow the Steps one by one
```
sudo apt-get remove ros-kinetic-gazebo*
sudo apt-get upgrade
sudo apt-get install ros-kinetic-libgazebo8-dev
sudo apt-get install ros-kinetic-gazebo8*  
sudo apt-get install ros-kinetic-gazebo-worlds-oru  
sudo apt-get install ros-kinetic-orunav-mpc  
sudo apt-get install ros-kinetic-navigation-oru  
source /opt/ros/kinetic/setup.bash  
```  





Credit:  
This is a simulation based off from OSRF's car_demo
