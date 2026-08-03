# Launching Nodes
1) source install/setup.bash
2) ros2 launch <package_name> <launch_file_name>

# Current state of project:

```
ros2 launch sctebot2_viz view_model.launch.py
```

# Rebuilding Workspace

```
colcon build --symlink-install
```

# Useful tools
```
ros2 run rqt_topic rqt_topic

ros2 topic echo /<topic name>
``

# TODO:
1) Get robot description to launch in a container.
2) Get RVIZ to launch in a container.
    - Note: current RVIZ launch file also launches the description. This may need to be undone so that two robot_descriptions and joint states aren't published at the same time. Put another way, RVIZ should just launch the GUI and nothing else.
3) Get sensors to launch in a container.
4) Verify sensors show up in RVIZ when running in the container.

5) Get carlikebot ros2 demo running in a container and connected to the model.
6) Verify RC control of simulated vehicle using a gamepad.
7) Start working on converting old ROS1 custom nodes/drivers to ROS2.
8) Verify RC control of real vehicle using a gamepad.
9) Work on getting localization working with the following sensors:
    - IMU
    - GPS
    - COMPASS
    - LIDAR
    - Optical Flow Sensor (drone sensor)
    - Realsense Camera (occupancy)
10) Work on getting getting path planning integrated.