
---
# Mobile Robotics Final Project
#### Nate Herbst - A02307128
---

This repository contains the implementation of a python code simulation for Introduction to Planning and Control for Mobile Robots - ECE 5340 class. 

## Features Overview

### Basic Simulation Abilities (50 Points)
- (15 points) **Static Analysis Compliance**: Code passes `mypy` and `pylint` static analysis tests.
- (10 points) **Workspace Setup**: `final_project.rosinstall` file provided to recreate the workspace. (see [Setup Instructions](#setup-instructions))
- (10 points) **Single Launch File**: Each section has a single launch file to run all commands necessary for the simulation.
- (10 points) **Interactive Destination Selection**: GUI allows users to click and set a new destination for the robot.
- (5 points) **Adaptable Look-Ahead Horizon**: An explanation in the `FinalProjectWriteup.md` on how it dynamically adjusts while the robot moves.


### Control Capabilities (25 Points)
- (25 Points) **Trajectory Following Control Law**: Ensures the robot follows paths generated by implemented planners.

### Going beyond the classroom (60 Points)
- (30 points) **Visualize 3D Differential Drive Robot in RVIZ**: Visually see the differential drive robot in RVIZ and give it a point to go too.
- (30 points) **Visualize the Differential Drive Robot using Gazebo**: See robot spawn into Gazebo

## Setup Instructions

### Prerequisites
- **OS**: [Ubuntu 24.04 or newer]
- **ROS Distribution**: [ROS Jazzy]
- **Python Version**: [Python 3]
- **Dependencies** as stated int the  `requirements.txt` file:
  - `numpy`
  - `matplotlib`
  - `networkx`
  - `rtree`
  - `black`
  - `control`
  - `isort`
  - `jupyter`
  - `jupyterlab`
  - `mypy`
  - `myst-parser`
  - `pandas`
  - `pylint`
  - `sphinx`

### Installation

#### Assumtions
This installation sections assumes:
- You have the correct `.bashrc` aliases configured from the ECE-5345 ROS class 
- When running path planning algorithms, You have correctly set up the virtual environment with `python3 -m venv --system-site-packages venv && source venv/bin/activate` from the `make_venv` alias.
- And that you have the latest of ROS2 Jazzy, RVIZ, and Gazebo already installed 

1. Navigate to the repository:
   ```bash
   cd FinalProject
   ```
2. Use the provided `.rosinstall` file to set up the workspace:
   ```bash
   vcs import --input finalProject.rosinstall src
   ```
3. Build the workspace:
   ```bash
   build
   ```

---

## Running the Code

There are 3 launch files that can be run to satisfy the requirments for each section described in [Features Overview](#features-overview).

1. (10 points) Ability to click on the GUI to choose a new destination for the robot.
   - To run this launch file run the following command in the workspace directory after building:
   ```bash
   ros2 launch diff_drive_bot 3D_bot_path_follow_pysim.launch.py
   ```

2. (30 points) Visualize a 3D model of the robot from a CAD model in RVIZ.
   - To run this launch file and see the 3D `URDF` CAD model of a differential drive robot, run the following command in the workspace directory:
   ```bash
   ros2 launch diff_drive_bot 3D_RViz_Bot_FP.launch.py
   ```

3. (30 points) Runs using Gazebo without getting stuck.
   - To run this launch file and see the robot spawn in Gazebo, run the following command:
   ```bash
   ros2 launch diff_drive_bot 3D_Gazebo_Bot_FP.launch.py
   ```

---