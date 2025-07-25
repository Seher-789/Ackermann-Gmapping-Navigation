


# Ackermann GMapping Navigation
This project demonstrates autonomous SLAM (Simultaneous Localization and Mapping) using an Ackermann steering vehicle in a ROS Noetic and Gazebo 11 environment. The system utilizes the `gmapping` algorithm for real-time 2D mapping using LiDAR data.


https://github.com/user-attachments/assets/1688e08f-f25c-45df-8324-80fcce0e69d5


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
├── alogrithm/          # (Typo: Should be "algorithm"?)
├── launch/             # ROS launch files
├── urdf/               # URDF files for robot description
├── worlds/            # Gazebo simulation worlds
├── meshes/            # 3D meshes for the robot
├── config/            # Configuration files (e.g., YAML for navigation)
├── scripts/           # Python/bash scripts
├── robot_description/ # (Possibly redundant with urdf/?)
├── velodyne/          # Velodyne LiDAR related files
├── velodyne_simulator/ # Simulated Velodyne sensor
├── CMakeLists.txt     # ROS/Catkin build file
├── package.xml        # ROS package metadata
└── README.md          # Project documentation
```

# Ackermann-Gmapping-Navigation


<img width="1044" height="1168" alt="Screenshot from 2025-07-16 14-30-11" src="https://github.com/user-attachments/assets/3818ca16-b646-4c94-912d-9044e08795c9" />

![Robot_acker](https://github.com/user-attachments/assets/e8013b8a-6db0-46a3-9dfb-d8f5fe030f1d)





