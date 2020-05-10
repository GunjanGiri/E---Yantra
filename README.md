# E-Yantra
This Repo is Created to submit Details and Works regarding E-Yantra

Open a terminal window and install the dependent packages. Enter the following commands, one right after the other:
cd ~/catkin_ws/src/
git clone https://github.com/GunjanGiri/E-Yantra.git
cd ~/catkin_ws && catkin_make

TurtleBot3 has three models, Burger, Waffle, and Waffle Pi, so you have to set which model you want to use before you launch TurtleBot3. Type this command to open the bashrc file to add this setting:

gedit ~/.bashrc

Add this line at the bottom of the file:
export TURTLEBOT3_MODEL=burger

Save the file and close it.
Now reload .bashrc so that you do not have to log out and log back in.

source ~/.bashrc

cd ~/catkin_ws && catkin_make

Then we need to run the Gazebo and Turtlebot.

Install the SLAM module in a new terminal window.
sudo apt install ros-melodic-slam-gmapping

Start Gazebo in a new terminal window.
roslaunch turtlebot3_gazebo turtlebot3_world.launch

Start SLAM in a new terminal tab.
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping

Start autonomous navigation in a new terminal tab:
roslaunch turtlebot3_gazebo turtlebot3_simulation.launch

Watch the robot create a map of the environment as it autonomously moves from place to place!
