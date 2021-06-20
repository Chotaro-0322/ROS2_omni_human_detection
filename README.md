# ROS2_omni_human_detection
# Explain
Human detection for omnidirectional camera that PIXPRO360 4k with ROS2(ROS1 bridge)
# Install
・kodak<br>
https://github.com/uts-magic-lab/kodak_pixpro_sp360_ros<br>
・Panorama convertion<br>
https://github.com/Chotaro-0322/ROS1_panorama_convert<br>
# Usage
terminal 1
```
source /opt/ros/melodic/setup.bash
roslaunch {kodak_root}/kodak.launch
```
terminal 2
```
source /opt/ros/melodic/setup.bash
source ~/ROS1_panorama_convert/devel/setup.bash
rosrun panoram panorama
```
terminal 3
```
source /opt/ros/dashing/setup.bash
ros2 run ros1_bridge dynamic_bridge --bridge-all-topics
```
terminal 4
```
source /opt/ros/dashing/setup.bash
python ros2_img_detection.py
```
![gif](https://github.com/Chotaro-0322/ROS2_omni_human_detection/wiki/image/panorama_detection05.gif)
