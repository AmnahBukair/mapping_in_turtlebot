# Mapping_in_turtlebot
SLAM tool will be used to create maps in turtlebot world.   
to do that, follow three simple steps.  

 ## 1- Launch turtlebot world  
 This will be your first terminal, press CTRL+ALT+T  
 ### Change directory  
 go to the workspace where you have installed turtlebot package.  
 $ cd ~/Documents/ turtlebot_ws  
 ### Launch Gazebo  
 $ source devel/setup.bash  
 $ export TURTLEBOT3_MODEL=burger  
 $ roslaunch turtlebot3_gazebo turtlebot3_world.launch  
 
 ## 2- Launch SLAM
 open another terminal and type these lines:
$ cd ~/Documents/ turtlebot_ws  
$ source devel/setup.bash  
$ export TURTLEBOT3_MODEL=burger  
$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping  

## 3- Remotely Control TurtleBot3
Again, open another terminal and type these lines:
$ cd ~/Documents/ turtlebot_ws  
$ source devel/setup.bash  
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

## 4- Save the Map
$ rosrun map_server map_saver -f ~/map
