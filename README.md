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
3. Add the plugin to GAZEBO_PLUGIN_PATH by adding following line at the end of the `.bashrc`file. (replace `ros2_ws` with the name of your ROS 2 workspace):
    ```
    export GAZEBO_PLUGIN_PATH=$GAZEBO_PLUGIN_PATH:~/ros2_ws/build/actor_collision_plugin
    ```
4. Source your `.bashrc` file:
    ```
    source ~/.bashrc
    ```

## Referance Used
- [gazebo_plugin_actor_collision](https://github.com/LCAS/iliad/tree/master/gazebo_plugin_actor_collision)