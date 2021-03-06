# osv_sim
A simulation repository for the OSV platform.

## Prerequisite 
This simulation has been tested in the following environment.  
* Ubuntu 16.04 LTS  
* ROS Kinetic Kame  


Please note that the current simulation has been set to run w/o the gui.  
Therefore, this simulation will launch without the graphical component.  
Visualization is done through RVIZ, which is launched at initialization by default.  
  
This is done to reduce resource used on host computer, especially those who uses virtual machine or weaker machine.  

RUN:   
```roslaunch fusion_ad_sim demo.launch```




INSTALLING GAZEBO 8 on a Machine with ROS installed.
Follow the Steps one by one
```
$ sudo sh -c 'echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable `lsb_release -cs` main" > /etc/apt/sources.list.d/gazebo-stable.list'
$ wget http://packages.osrfoundation.org/gazebo.key -O - | sudo apt-key add -
$ sudo apt-get update
$ wget https://bitbucket.org/osrf/release-tools/raw/default/jenkins-scripts/lib/dependencies_archive.sh -O /tmp/dependencies.sh ROS_DISTRO=dummy . /tmp/dependencies.sh
$ sudo apt-get install libignition-math3
$ sudo apt-get install $(sed 's:\\ ::g' <<< $BASE_DEPENDENCIES) $(sed 's:\\ ::g' <<< $GAZEBO_BASE_DEPENDENCIES)
$ sudo apt-get install ros-kinetic-gazebo8*  
$ sudo apt-get install ros-kinetic-fake-localization
$ sudo apt-get install ros-kinetic-joy
$ source /opt/ros/kinetic/setup.bash  
```    

Building the simulation  
```
$ catkin_make --pkg osv_msgs
$ catkin_make
```   


Troubleshooting:  
Q: Catkin_make is telling me that Control.h is not found  
A: Try catkin_make again, that's just the custom message not built for the first time you build the simulation  

Q: Some node is failing or some package is missing at build   
A: run this ```rosdep install --from-paths src --ignore-src -r -y```  



Credit:  
This is a simulation based off from OSRF's car_demo
