# Aurora_urdf_task
This repository contains a basic ROS- workspace for an Autonomous Mobile Robot (AMR) model built using URDF (Unified Robot Description Format). It serves as a foundation for simulation and visualization.


## Objective

The goal of this project is to:

1. Model an autonomous navigation robot model using URDF

2. Visualize and simulate using RViz and Gazebo

## Features
### ROS package structure 

#### 1. autonomous_nav/autonomous_nav_urdf

      -URDF-based robot model folder: includes plugins for interfacing with gazebo
      -rviz template world
      -launch file for visualizing in Rviz

#### 2. autonomous_nav_bringup
      -config folder: gazebo bridge for connecting ros2 to gz(equipped with keyboard teleop compatibility)
      -launch file to visualize in gazebo
      -worlds: store template gazebo world
      
## Requirements

1. ROS 2 : Humble 
2. RViz2 (for visualization)
3. Gazebo (Gazebo Harmonic is compatible version for Humble)

### Visualizing the Robot (RViz)

    ros2 launch autonomous_nav_urdf display.launch.xml

### Simulating in Gazebo

    ros2 launch autonomous_nav_bringup gazebo.launch.xml

### Controlling with Keyboard teleop (while gazebo.launch.xml is running)
 
    ros2 launch  ros2 run teleop_twist_keyboard teleop_twist_keyboard

## Future Improvements
Planned upgrades include:

1. Integrating sensors (LiDAR, IMU, camera)
2. SLAM and navigation stack integration
3. Autonomous path planning
4. Learning Outcomes

Through this project, I gain practical understanding of:

1. Robot modeling using URDF
2. ROS 2 workspace architecture
3. Simulation pipeline setup
4. Modular robotics system design
