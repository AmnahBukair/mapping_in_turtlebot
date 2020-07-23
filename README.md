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
 
 ![image](https://user-images.githubusercontent.com/66624381/88346557-4a406280-cd51-11ea-8a27-60f9598ad8d4.png)

 
 ## 2- Launch SLAM
 open another terminal and type these lines:
$ cd ~/Documents/ turtlebot_ws  
$ source devel/setup.bash  
$ export TURTLEBOT3_MODEL=burger  
$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping  

![image](https://user-images.githubusercontent.com/66624381/88346595-63e1aa00-cd51-11ea-8da6-758f23c75980.png)


## 3- Remotely Control TurtleBot3
Again, open another terminal and type these lines:
$ cd ~/Documents/ turtlebot_ws  
$ source devel/setup.bash  
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

![image](https://user-images.githubusercontent.com/66624381/88346681-955a7580-cd51-11ea-8e42-994f642bbf37.png)

Note: you have to press this respiratory to be able to control the movement

## 4- Save the Map
$ rosrun map_server map_saver -f ~/map

* Final map  
![image](https://user-images.githubusercontent.com/66624381/88346841-000bb100-cd52-11ea-8664-bbb1103327ce.png)
