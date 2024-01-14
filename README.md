## Table of Contents
- [Introduction](#0)
- [File Tree](#1)
- [Start](#2)
- [UI Design](#3)
- [Examples](#4)
  - [Path Planning](#path-planning)
  - [Curve Generation](#curve-generation)
- [More](#5)


## <span id="0">0. Introduction

### Notice: This project is still under development. Please wait for our official release.

This repository provides a ROS-based visualization Rviz plugins for path planning and curve generation algorithms.

In scientific research, this repository allows researchers to observe, study, understand and analyze the working mechanisms of different algorithms, making it easier to identify strengths and weaknesses. This helps in the development of more efficient and optimized algorithms for various applications, such as robotics, transportation, and computer graphics.

This plugin is also one of tool chains of [ROS Motion Planning](https://github.com/ai-winter/ros_motion_planning) project.

## 1. <span id="1"> Start
We provide a script to quickly start the world.
```sh
cd ./scripts
./main.sh
```
## 2. <span id="2"> UI Design
`include/rmpv/ui_rmpv.h` is automatically generated by `uic`. To modify it, please modify `ui/rmpv.ui` with Qt Designer and run the following commands in your terminal.
```sh
cd ./src/rviz_plugins/rmpv
uic -o ./include/rmpv/ui_rmpv.h ./ui/rmpv.ui
```
## 3. <span id="3"> Documentation
Generating doxygen documentation helps you understand the code better.

First install doxygen and graphviz.
```sh
sudo apt-get install doxygen
sudo apt-get install graphviz
```
Then run the following commands in your terminal to generate doxygen documentation.
```sh
cd ./
doxygen
```
Then you can find the documentation in `./docs/html/index.html`. You can configure the doxygen settings in `./Doxyfile`.
## 4. <span id="4"> Examples
### 4.1 Path Planning
|     Planner      |                                                                                             Version                                                                                              |                         Demo                          |
|:----------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------:|
|     **GBFS**     |      [![Status](https://img.shields.io/badge/done-v1.0-brightgreen)](https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/graph_planner/src/a_star.cpp)       |            ![gbfs_ros.png](assets/gbfs_ros.png)            |
|   **Dijkstra**   |      [![Status](https://img.shields.io/badge/done-v1.0-brightgreen)](https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/graph_planner/src/a_star.cpp)       |        ![dijkstra_ros.png](assets/dijkstra_ros.png)        |
|     **A\***      |      [![Status](https://img.shields.io/badge/done-v1.1-brightgreen)](https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/graph_planner/src/a_star.cpp)       |          ![a_star_ros.png](assets/a_star_ros.png)          |
|     **JPS**      | [![Status](https://img.shields.io/badge/done-v1.0-brightgreen)](https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/graph_planner/src/jump_point_search.cpp) |             ![jps_ros.png](assets/jps_ros.png)             |
|     **D\***      |     [![Status](https://img.shields.io/badge/done-v1.0-brightgreen)]((https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/graph_planner/src/d_star.cpp))      |          ![d_star_ros.png](assets/d_star_ros.png)          |
|    **LPA\***     |    [![Status](https://img.shields.io/badge/done-v1.0-brightgreen)]((https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/graph_planner/src/lpa_star.cpp))     |        ![lpa_star_ros.png](assets/lpa_star_ros.png)        |
|   **D\* Lite**   |   [![Status](https://img.shields.io/badge/done-v1.0-brightgreen)]((https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/graph_planner/src/d_star_lite.cpp))   |     ![d_star_lite_ros.png](assets/d_star_lite_ros.png)     |
|   **Voronoi**    |     [![Status](https://img.shields.io/badge/done-v1.0-brightgreen)]((https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/graph_planner/src/voronoi.cpp))     |         ![voronoi_ros.png](assets/voronoi_ros.png)         |
|   **Theta\***    |   [![Status](https://img.shields.io/badge/done-v1.0-brightgreen)]((https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/graph_planner/src/theta_star.cpp))    |      ![theta_star_ros.png](assets/theta_star_ros.png)      |
| **Lazy Theta\*** | [![Status](https://img.shields.io/badge/done-v1.0-brightgreen)]((https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/graph_planner/src/lazy_theta_star.cpp)) | ![lazy_theta_star_ros.png](assets/lazy_theta_star_ros.png) |
|     **RRT**      |       [![Status](https://img.shields.io/badge/done-v1.1-brightgreen)](https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/sample_planner/src/rrt.cpp)        |             ![rrt_ros.png](assets/rrt_ros.png)             |
|    **RRT\***     |     [![Status](https://img.shields.io/badge/done-v1.0-brightgreen)](https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/sample_planner/src/rrt_star.cpp)     |        ![rrt_star_ros.png](assets/rrt_star_ros.png)        |
| **Informed RRT** |   [![Status](https://img.shields.io/badge/done-v1.0-brightgreen)](https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/sample_planner/src/informed_rrt.cpp)   |    ![informed_rrt_ros.png](assets/informed_rrt_ros.png)    |
| **RRT-Connect**  |   [![Status](https://img.shields.io/badge/done-v1.0-brightgreen)](https://github.com/ai-winter/path_visualization_plugins/blob/master/src/planner/global_planner/sample_planner/src/rrt_connect.cpp)    |     ![rrt_connect_ros.png](assets/rrt_connect_ros.png)     |

### 4.2 Curve Generation

## 5. <span id="5"> More

Our motion planning R&D toolkit:
* [ROS Motion Planning](https://github.com/ai-winter/ros_motion_planning)
  * [ROS Pedestrians Simulation](https://github.com/ai-winter/ros_pedestrians_simulation)
  * [ROS Motion Planning Visualizer](https://github.com/ai-winter/ros_motion_planning_visualizer)
* [Python Motion Planning](https://github.com/ai-winter/python_motion_planning)
* [Matlab Motion Planning](https://github.com/ai-winter/matlab_motion_planning)

Your stars, forks and PRs are welcome! Wishing you all the best in your research!
