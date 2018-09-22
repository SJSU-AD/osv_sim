# osv_sim
A simulation repository for the OSV platform.

RUN:   
```roslaunch fusion_ad_sim demo.launch```







Known Possible Error or Missing Package:   
```sudo apt-get ros-kinetic-fake-localization```


INSTALLING GAZEBO 8 on a Machine with ROS installed.
Follow the Steps one by one
```
$ sudo sh -c 'echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable `lsb_release -cs` main" > /etc/apt/sources.list.d/gazebo-stable.list'
$ wget http://packages.osrfoundation.org/gazebo.key -O - | sudo apt-key add -
$ sudo apt-get update
$ wget https://bitbucket.org/osrf/release-tools/raw/default/jenkins-scripts/lib/dependencies_archive.sh -O /tmp/dependencies.sh
ROS_DISTRO=dummy . /tmp/dependencies.sh
$ sudo apt-get install $(sed 's:\\ ::g' <<< $BASE_DEPENDENCIES) $(sed 's:\\ ::g' <<< $GAZEBO_BASE_DEPENDENCIES)
$ sudo apt-get install ros-kinetic-libgazebo8-dev
$ sudo apt-get install ros-kinetic-gazebo8*  
$ sudo apt-get install ros-kinetic-gazebo-worlds-oru  
$ sudo apt-get install ros-kinetic-orunav-mpc  
$ sudo apt-get install ros-kinetic-navigation-oru  
$ source /opt/ros/kinetic/setup.bash  
```  





Credit:  
This is a simulation based off from OSRF's car_demo
