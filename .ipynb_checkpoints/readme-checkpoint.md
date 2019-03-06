# A* Pathfinding on a point cloud using Delaunay triangulation
Author: Gabi Abrahams

## Notes
* There is no guarantee that Delaunay produces a fully connected graph, so some nodes will be unreachable. This is a major issue!
* Delaunay is O(n^2)
* The final notebook takes both distance and steepness into account to find the least steep path
* Perhaps rover pose could also be taken into acount - by using the nodes around a given node to figure out where all the wheels will be.
* There is no object avoidance. This may be part of the solution: [GROUND FILTERING LiDAR DATA BASED ON MULTI-SCALE ANALYSIS OF HEIGHT DIFFERENCE THRESHOLD](https://www.researchgate.net/publication/320072506_GROUND_FILTERING_LiDAR_DATA_BASED_ON_MULTI-SCALE_ANALYSIS_OF_HEIGHT_DIFFERENCE_THRESHOLD/fulltext/59cc779ba6fdcc451d5cf58f/320072506_GROUND_FILTERING_LiDAR_DATA_BASED_ON_MULTI-SCALE_ANALYSIS_OF_HEIGHT_DIFFERENCE_THRESHOLD.pdf)

## Dependencies
* scipy `pip install scipy`
* matplotlib `pip install matplotlib`
* jupyter lab `pip install jupyterlab`

For interactive widgets:
1. `pip install ipympl`
2. `pip install ipywidgets`
3. Install [node.js](https://nodejs.org/en/)
4. `jupyter labextension install @jupyter-widgets/jupyterlab-manager`
5. `jupyter labextension install jupyter-matplotlib`
Then uncomment '%matplotlib widget' in the first cell of each file.

## To run jupyter lab:
Open up a terminal in this folder and run `jupyter lab`