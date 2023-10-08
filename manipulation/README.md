To get a simple robot model visualisationm, follow the following steps:

1. Run the following command to start the `robot_state_publisher` which will publish the URDF description of the robot to the `/robot_description` topic.

```bash
ros2 launch manipulation robot_state_publisher.launch.py
```
2. Open a new terminal and to get a simple GUI to move the robot joints using the `joint_state_publisher_gui`  ROS package, run the following command:

```bash
ros2 run joint_state_publisher_gui joint_state_publisher_gui
```

3. Open rviz2 in a new terminal

```bash
rviz2 
```
In the `rviz2` gui, set the `Fixed frame` under `Global Options` to the `world` frame.

Add a `TF`, check the ` Show Names` checkbox to see the names of the frames

To visualise a simple 3D model of the robot and the camera described by the `urdf.xacro` file, add a `Robot Model` and set `Description Topic` to `/robot_description`

Move the joints of the robot using the `Joint State Publisher` GUI.
