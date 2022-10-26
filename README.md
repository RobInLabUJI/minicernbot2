# minicernbot2

Server for MiniCERNBot2 that subscribes to `cmd_vel` and sends the velocities through the serial port.

## Usage

Clone this repository into your ROS2 workspace
```
cd ~/ros2_ws/src
git clone https://github.com/RobInLabUJI/minicernbot2.git
```

Compile
```
cd ~/ros2_ws
colcon build --packages-select minicernbot2
```

Run the server
```
source /opt/ros/foxy/setup.bash
cd ~/ros2_ws
. install/setup.bash
ros2 run minicernbot2 listener --ros-args -p uart_target:=/dev/ACM0
```

Send motion commands with the keyboard
```
source /opt/ros/foxy/setup.bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```
