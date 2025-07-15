<img width="1229" height="1228" alt="Screenshot from 2025-07-15 16-27-16" src="https://github.com/user-attachments/assets/655e060f-4ee1-4d7c-b7cb-553608d569aa" />
<img width="1281" height="1281" alt="Screenshot from 2025-07-15 16-23-39" src="https://github.com/user-attachments/assets/e5c3cd06-ef1a-4a9a-9664-00b17792ec7c" />
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

