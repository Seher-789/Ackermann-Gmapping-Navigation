
# Ackermann GMapping Navigation

This project demonstrates autonomous SLAM (Simultaneous Localization and Mapping) using an Ackermann steering vehicle in a ROS Noetic and Gazebo 11 environment. The system utilizes the `gmapping` algorithm for real-time 2D mapping using LiDAR data.

---

## Features

- Ackermann vehicle model with differential drive approximation
- LiDAR-based environment mapping via `gmapping`
- Sensor data processing via `pointcloud_to_laserscan`
- Interactive map saving
- Compatible with ROS Noetic and Gazebo 11

---

## Requirements

- **Ubuntu 20.04**
- **ROS Noetic**
- **Gazebo 11**
- **Velodyne VLP-16**

---

## Installation & Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/Seher-789/Ackermann-Gmapping-Navigation.git
cd Ackermann-Gmapping-Navigation
```
### Step 2: Build the Workspace
```bash
cd ~/Ackermann-Gmapping-Navigation
catkin_make
source devel/setup.bash
```
### Launching the Simulation 
### Step 1: Launch GMapping
```bash
roslaunch robot_description robot_gmapping.launch
```
### Step 2: Convert PointCloud to LaserScan
```bash
roslaunch robot_description pointcloud_to_laserscan.launch
```
### Step 3: Launch Robot Control Interface
```bash
roslaunch robot_description isac.launch
```
### Saving the Map
Once the map is fully built in RViz, run:
```bash
rosrun map_server map_saver -f ~/your_directory/map_name
```
Replace ~/your_directory/map_name with the desired path and filename.

### Project Structure
```bash
Ackermann-Gmapping-Navigation/
├── robot_description/         # Launch files and URDFs for Ackermann robot
├── maps/                      # Saved maps (output)
├── scripts/                   # Control, sensor scripts (if any)
└── README.md
```

# Ackermann-Gmapping-Navigation
