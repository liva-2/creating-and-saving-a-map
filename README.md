# creating-and-saving-a-map
### creating and saving a map using Turtlebot3 with SLAM approach
## 1- PC setup
* Install ROS 1 on Remote PC
```
wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_melodic.sh
```
```
chmod 755 ./install_ros_melodic.sh 
```
```
bash ./install_ros_melodic.sh
```
* Install Dependent ROS 1 Packages
```
sudo apt-get install ros-melodic-joy ros-melodic-teleop-twist-joy \
  ros-melodic-teleop-twist-keyboard ros-melodic-laser-proc \
  ros-melodic-rgbd-launch ros-melodic-depthimage-to-laserscan \
  ros-melodic-rosserial-arduino ros-melodic-rosserial-python \
  ros-melodic-rosserial-server ros-melodic-rosserial-client \
  ros-melodic-rosserial-msgs ros-melodic-amcl ros-melodic-map-server \
  ros-melodic-move-base ros-melodic-urdf ros-melodic-xacro \
  ros-melodic-compressed-image-transport ros-melodic-rqt* \
  ros-melodic-gmapping ros-melodic-navigation ros-melodic-interactive-markers
  ```
  * Install TurtleBot3 Packages
```
 sudo apt-get install ros-melodic-dynamixel-sdk
 ```
 ```
 sudo apt-get install ros-melodic-turtlebot3-msgs
 ```
 ```
 sudo apt-get install ros-melodic-turtlebot3
 ```
 * Set TurtleBot3 Model Name
 ```
 echo "export TURTLEBOT3_MODEL=waffle_pi" >> ~/.bashrc
 ```
 ## 2- simulation
 * Install Simulation Package
 ```
 cd ~/catkin_ws/src/
 ```
 ```
 git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
 ```
 ```
 cd ~/catkin_ws && catkin_make
 ```
 * Launch Simulation World
```
export TURTLEBOT3_MODEL=waffle
```
```
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
* Operate TurtleBot3
```
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
* Run SLAM Node
```
export TURTLEBOT3_MODEL=waffle
```
* Run Teleoperation Node
```
export TURTLEBOT3_MODEL=waffle
```
### then we will be able to control the robot and draw the map
* Save Map
```
rosrun map_server map_saver -f ~/map
```
### creating and saving a map using AVG with SLAM approach
* i created and saved the map following this github steps: https://github.com/wh200720041/warehouse_simulation_toolkit - automatic!
[GitHub](http://github.com)
