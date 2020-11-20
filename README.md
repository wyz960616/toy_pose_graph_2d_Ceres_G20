# pose_graph_demo_Ceres_G2O

Sample codes to conduct 2D pose graph optimization with Ceres Solver or G2O.

## Dependences

* Eigen 3.3 or later
* Ceres Solver 1.12.0 or later
* g2o 
* Python with matplotlib

## Build

```bash
$ git clone https://github.com/wyz960616/toy_pose_graph_2d_Ceres_G20.git
$ cd  toy_pose_graph_2d_Ceres_G20
$ mkdir build
$ cd build
$ cmake ..
$ make -j4
```

## Optimize

```bash
$ cd  toy_pose_graph_2d_Ceres_G20/bin
$ ./PoseGraphDemoG2O ../datas/manhattan.g2o 
$ ./PoseGraphDemoCeres ../data/manhattan.g2o
```

## Visualize

```bash
$ cd toy_pose_graph_2d_Ceres_G20/script
$ python plot_results.py poses_original_ceres.txt poses_optimized_ceres.txt 
$ python plot_results.py poses_original_g2o.txt poses_optimized_g2o.txt 

```

Or using g2o_viewer:

```bash
$ cd toy_pose_graph_2d_Ceres_G20/datas
$ g2o_viewer manhattan.g2o
$ g2o_viewer manhattan_result.g2o

```

### This project used  https://github.com/shinsumicco/pose-graph-optimization.git for reference.
