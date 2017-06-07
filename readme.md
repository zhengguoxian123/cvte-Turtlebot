### Source Installation

#### rocon
```
mkdir ~/rocon
cd ~/rocon
wstool init -j5 src https://raw.github.com/robotics-in-concert/rocon/release/indigo/rocon.rosinstall
source /opt/ros/indigo/setup.bash
rosdep install --from-paths src -i -y
catkin_make
```
#### kobuki
```
mkdir ~/kobuki
cd ~/kobuki
wstool init src -j5 https://raw.github.com/yujinrobot/yujin_tools/master/rosinstalls/indigo/kobuki.rosinstall
source ~/rocon/devel/setup.bash
rosdep install --from-paths src -i -y
catkin_make
```

#### turtlebot
```
mkdir ~/turtlebot
cd ~/turtlebot
wstool init src -j5 https://github.com/rongbohou/cvte-Turtlebot/turtlebot.rosinstall
source ~/kobuki/devel/setup.bash
rosdep install --from-paths src -i -y
catkin_make
```
