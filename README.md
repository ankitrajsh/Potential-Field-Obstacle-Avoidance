# Potential Field Obstacle Avoidance

This project implements a simple potential field-based obstacle avoidance algorithm in Python. The robot navigates towards a goal while avoiding obstacles by calculating attractive and repulsive forces.

## Table of Contents
- [Introduction](#introduction)
- [How It Works](#how-it-works)
- [Requirements](#requirements)
- [Usage](#usage)
- [Example](#example)
- [Code Explanation](#code-explanation)
- [License](#license)

## Introduction
Potential Field Obstacle Avoidance (PFOA) is commonly used in robotics for real-time navigation. The algorithm treats obstacles as repelling forces and the target as an attracting force, allowing the robot to avoid obstacles while moving towards a goal.

## How It Works
1. **Attractive Force**: Pulls the robot toward the goal.
2. **Repulsive Force**: Pushes the robot away from obstacles within a specified threshold.
3. **Total Force**: The robot follows the combined attractive and repulsive forces to reach the goal while avoiding obstacles.



## Requirements
- Python 3.x
- NumPy

Install the required packages:
```bash
pip install numpy
```

## Usage
1. Clone this repository.
2. Open the `potential_field_obstacle_avoidance.py` file.
3. Update the `robot_pos`, `goal_pos`, and `obstacles` with the coordinates of the robot, goal, and obstacles.
4. Run the script to calculate the total force acting on the robot.

```bash
python potential_field_obstacle_avoidance.py
```


## Example
Given the following positions:

- **Robot**: `[1.0, 2.0]`
- **Goal**: `[10.0, 10.0]`
- **Obstacles**: `[[4.0, 5.0], [7.0, 8.0]]`

The output will show the resultant force vector acting on the robot, guiding it toward the goal while avoiding obstacles.

## Code Explanation
- **`attractive_force(robot_pos, goal_pos)`**: Calculates the attractive force that pulls the robot towards the goal.
- **`repulsive_force(robot_pos, obstacle_pos, d_robot_obstacle)`**: Calculates the repulsive force from each obstacle.
- **`total_force(robot_pos, goal_pos, obstacles)`**: Computes the net force acting on the robot by summing up all attractive and repulsive forces.

## License
This project is licensed under the MIT License.

