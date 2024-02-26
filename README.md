# turtlebot3
Commands for parking the robot in particular location / specific coordinates.

$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_autorace_detect my_launch_file.launch

export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/office_small.yaml

roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml

rosrun tf tf_echo /office_small /base_link
rosrun tf tf_echo /map /base_link


set parking 
cd ~/home/robot/catkin_ws/turtlebot
emacs -nw parking_position.py

modify line 83
position = {'x': 1.22, 'y' : 2.56}

Crtl + x
Crtl + s

#launch Parking
cd ~/catkin_ws/turtlebot
export TURTLEBOT3_MODEL=burger
python3 parking_position.py
