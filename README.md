# Run-and-install-the-arm-packag-on-ROS
After installing Ubuntu and installing ROS, follow the instructions below to install packag. <br>
If you have not installed Ubuntu and ROS, go to this repository https://github.com/Aliah110/Download_the_ROS_O

Let's create and build a catkin workspace:
```
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin_make
```
```
cd ~/catkin_ws/src
```
The git clone command is used to create a copy of a specific repository or branch within a repository.
you can read more about this command in https://github.com/git-guides/git-clone
```
git clone https://github.com/smart-methods/arduino_robot_arm.git 
```
```
cd ~/catkin_ws
```
Then you may run the following instruction to make sure that all dependencies referenced in the workspace are installed
```
rosdep install --from-paths src --ignore-src -r -y
```
```
sudo apt-get install ros-kinetic-moveit
```
```
sudo apt-get install ros-kinetic-joint-state-publisher ros-kinetic-joint-state-publisher-gui
```
```
sudo apt-get install ros-kinetic-gazebo-ros-control joint-state-publisher
```
```
sudo apt-get install ros-kinetic-ros-controllers ros-kinetic-ros-control
```
'.bashrc' is a Bash shell script that Bash runs whenever it is started interactively. <br>
It initializes an interactive shell session. You can put any command in that file that you could type at the command prompt.
```
sudo nano ~/.bashrc
```
```
at the end of the (bashrc) file add the follwing line
(source /home/your_name/catkin_ws/devel/setup.bash)
then 
ctrl + o
```
```
source ~/.bashrc
```
```
roslaunch robot_arm_pkg check_motors.launch
```
Screenshot of the robot arm installation steps
![صورة2](https://user-images.githubusercontent.com/108204114/181555431-8193d95b-711d-452c-b718-3ba667fc2889.png)
![صورة3](https://user-images.githubusercontent.com/108204114/181555849-bda31f2b-0bf8-4a21-a153-d4353f74d807.png)


