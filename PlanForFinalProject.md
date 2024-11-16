# Plan for Final Project
### Mobile Robotics - ECE 5340 - December 7th 2024

Nate Herbst - A02307138

Devon Higgs - A02312014

## Basic sim abilities - TOTAL POINTS: 50
- (15 points) Python code passes mypy and pylint static analysis tests
- (10 points) Turn in a .rosinstall file which can be used with wstool to make a workspace that runs the code
- (10 points) A single launch file can be called to run the entire sim
- (10 points) Ability to click on the GUI to choose a new destination for the robot. Describe how to do so in the writeup.
- (5 points) Adaptable look ahead horizon. Describe how it is used in the planning architecture in the writeup and how it is adjusted while the robot it moving.

## Planning capability - TOTAL POINTS: 125
- (25 points) Create an alternative Dijkstra-based planner - (i.e., D-star or some other variant - this is not something that you make up, but an existing algorithm that you implement). Explain how to configure the sim to run the planner.
- (50 points) Create an FB-RRT planner that can be used to plan for the robot. Explain how to configure the sim to run the planner.
- (50 points) Create an FB-RRT* planner that can be used to plan for the robot. Explain how to configure the sim to run the planner. 

## Control capability - TOTAL POINTS: 25
- (25 points) Have a trajectory following control law used to follow the path that you find with one of your implemented planners

## TOTAL PROJECT POINTS: 200

---

# Plan if we have time

## Planning capability
- (75 points) Create a BIT* planner that can be used to plan for the robot. Explain how to configure the sim to run the planner.
- (100 points) Create an FB-BIT* planner that can be used to plan for the robot. Explain how to configure the sim to run the planner.
- (25 points) Implement an alternative (pre-approved) planner that can be used to plan for the robot. Explain how to configure the sim to run the alternative planner. Explain the planner in detail. Get written approval (e.g., via email) from Dr. Droge prior to implementing the planner.


## Control capability
- (25 points) Implement a trajectory following control law for a smooth model. Demonstrate convergence.
- (20 points) Implement vector field techniques to aid in the following of the plan (must be more than a simple go-to-goal vector field)

## Going beyond the classroom
- (30 points) Visualize a 3D model of the robot from a [CAD model](https://www.youtube.com/watch?v=Eie-KoMQtxs) in RVIZ 
- (50 points) Implement the Dynamic Window Approach (DWA) to navigation for a smooth unicycle model