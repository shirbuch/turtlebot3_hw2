# pick_balls_turtlebot3 - Assignment 2 in Robotics Lab

### Info:
Services:
1. Navigate(x, y, theta)->none		: Navigate to a point
2. SensePose()->(x, y, header)		: Sense current robot pose
3. SenseObjects()->[Object]	: Return name and location of each object within the map
4. PickObject(Object)->none	: Pick nearby object (delete and spawn in the knapsack (outside the map))
5. PlaceObject(Object)->none	: Place the object (delete from knapsack and spawn it at the location)

Messages:
1. Object(name, x, y)

### Change Speed (not working):
by https://github.com/ROBOTIS-GIT/turtlebot3/issues/897
\catkin_ws\src\turtlebot3_simulations\turtlebot3_gazebo\include\turtlebot3_gazebo\turtlebot3_drive.h
 define LINEAR_VELOCITY  0.44 //0.3
 define ANGULAR_VELOCITY 2.2  //1.5

\catkin_ws\src\turtlebot3\turtlebot3_navigation\param\dwa_local_planner_params_burger.yaml
  max_vel_x: 9 # 0.22
  min_vel_x: -0.22

  max_vel_y: 0.0
  min_vel_y: 0.0

  max_vel_trans:  9 # 0.22
  min_vel_trans:  0.11

  max_vel_theta: 9 # 2.75
  min_vel_theta: 1.37

\catkin_ws\src\turtlebot3\turtlebot3_navigation\param\base_local_planner_params.yaml
  max_vel_x: 9 # 0.18
  min_vel_x: 0.08

  max_vel_theta:  3 # 1.0

### Build:
1. Unzip pick_balls_turtlebot3.zip into ~/catkin_ws/src
2. open terminal and cd into (unzipped) pick_balls_turtlebot3
3. chmod +x install.sh
4. ./install.sh (this is to compile and source the pick_balls_turtlebot3 package and chmod +x to all script files)

### Run:
1. roslaunch pick_balls_turtlebot3 control.launch
