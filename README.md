# F1tenthBP
Code to run the F1tenth package.
ls -l /dev/ttyACM*
#Joy node
source install/setup.bash
ros2 run joy joy_node
#VESC node
source install/setup.bash
ros2 launch vesc_driver vesc_driver_node.launch.py
#Arduino node
source install/setup.bash
ros2 run micro_ros_agent micro_ros_agent serial --dev /dev/ttyACM0
#Ackermann node
source install/setup.bash
ros2 launch vesc_ackermann vesc_to_odom_node.launch.xml
ros2 topic list

