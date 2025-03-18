# actor_collision_plugin

## Description
The `actor_collision_plugin` is a ROS2 package for enabling collision for moving person in Gazebo simulator. This plugin allows the moving person to be detected by sensors like LiDAR by enabling collsion for it. 

## Installation Instructions
1. First, clone this repository inside the `src` folder of your ROS 2 workspace (replace `ros2_ws` with the name of your ROS 2 workspace):
    ```sh
    cd ~/ros2_ws/src
    git clone https://github.com/dhaval-lad/actor_collision_plugin.git
    ```
2. Next, build your ROS 2 workspace to install the package (replace `ros2_ws` with the name of your ROS 2 workspace):
    ```sh
    cd ~/ros2_ws
    colcon build --packages-select actor_collision_plugin
    ```

## Referance Used
- [gazebo_plugin_actor_collision](https://github.com/LCAS/iliad/tree/master/gazebo_plugin_actor_collision)