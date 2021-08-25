# The AirMuseum Dataset
## A stereo-inertial multi-robots dataset
**Paper**: [[MFI2020]](https://hal.archives-ouvertes.fr/hal-02943634/document)   
**Dataset**: [[IEEEdataport]](https://ieee-dataport.org/open-access/airmuseum-heterogeneous-multi-robot-dataset-stereo-visual-and-inertial-simultaneous)   
The AirMuseum dataset is intended for multi-robot stereo-visual and inertial Simultaneous 
Localization And Mapping (SLAM). It consists in five indoor multi-robot scenarios acquired with 
ground and aerial robots in a former Air Museum at ONERA Meudon, France. Those scenarios were 
designed to exhibit some specific opportunities and challenges associated to collaborative SLAM. 
Each scenario includes synchronized sequences between multiple robots with stereo images and 
inertial measurements. They also exhibit explicit direct interactions between robots through the 
detection of mounted AprilTag markers. Ground-truth trajectories for each robot were computed using 
Structure-from-Motion algorithms and constrained with the detection of fixed AprilTag markers 
placed as beacons on the experimental area. 

It is available for downloading at the following link : 
https://ieee-dataport.org/open-access/airmuseum-heterogeneous-multi-robot-dataset-stereo-visual-and-inertial-simultaneous.

## Preview of scenario
### Scenario 1 
This scenario, makes the three ground robots explore the full experimental
area. They share the same starting point in the North zone
and the same arrival point in the South area. 
They follow very long and ample trajectories without closing any loop
along them, what makes them prone to drift accumulation.
However, there exist multiple inter-robot correspondences
regularly dispatched between their trajectories, and which
allow to close large inter-robot loops. 
The beginning of those sequences may be challenging for odometry algorithms
because the North zone provides few features, most of them belonging to distant structures and exhibiting low parallax.
Furthermore, the reflexivity of the ground results into difficult lighting conditions for robot C at the very beginning
of the sequence. For each robot, the goal of this scenario is to rely on the large inter-robot loop closures induced by the
inter-robot correspondences to mitigate their drift.   
[<img src="https://img.youtube.com/vi/8zpBHcIyOi4/mqdefault.jpg" width=320 >](https://youtube.com/watch?v=8zpBHcIyOi4&list=PLsTICVK4763uqu5JZEJriHjsgEPBdl9RI)
<img src="airmuseum_traj1.gif" width = 320 height = 251 />   

### Scenario 2
This scenario is similar to the scenario 1, with the difference that it only
covers the South part and makes robots start from distinct locations and come back to their starting point.
That aside, each robot covers a significant portion of the South area
without closing any loop. Though they mostly navigate close
to well-textured surfaces, they occasionally cross empty areas
with fewer features and prone to drift accumulation. This is especially the case of robot A near the middle of its trajectory. Multiple inter-robot direct and indirect correspondences are dispatched along the trajectories. For each robot, the
objective is similar to the first scenario.   
[![robots video preview](https://img.youtube.com/vi/otypib5KwGE/mqdefault.jpg)](https://youtube.com/watch?v=otypib5KwGE&list=PLsTICVK4763uqu5JZEJriHjsgEPBdl9RI)
<img src="airmuseum_traj2.gif" width = 320 height = 251 />

### Scenario 3
This scenario involves the three ground robots and the drone.
The first two scenarios were designed in such a way that there were no glaring disparities between
the properties of the trajectories and that the inter-robot correspondences are evenly distributed among the robots.
On the contrary, the third scenario builds on asymmetries. First, robots A and C explore distinct non-overlapping areas and
never meet, nor do they share inter-robot correspondences.
Robot C also closes more loops than robot A, from which ones it may benefit to estimate its trajectory more accurately.
As for robot B, it covers the whole area and meets both other robots.
Finally, the drone successively meets all the ground robots. While robot C is not expected to gain much
estimation accuracy from its interactions with the other robots, it may bring valuable information to robot B, which
may then act as a torchbearer to robot A.   
[![robots video preview](https://img.youtube.com/vi/PhicanV4Tdk/mqdefault.jpg)](https://youtube.com/watch?v=PhicanV4Tdk&list=PLsTICVK4763uqu5JZEJriHjsgEPBdl9RI)
<img src="airmuseum_traj3.gif" width = 320 height = 251 />

### Scenario 4
Similarly to scenario 3, this scenario, explores how to handle and take advantage on information disparity between the robots.
Robot A continuously explores the very same restricted zone. Hence, it closes several loops and may achieve high estimation accuracy.
Reversely, robots B and C browse the full South area and periodically meet each other.
The drone alternately meets robots B and C, which may result in additional indirect constraints between their trajectories.
Furthermore, and overall, robots B and C regularly cross the zone of robot A and accumulate several inter-robot correspondences with
it, which then induce informative inter-robot loop closures and constraint large portions of their trajectories. The goal
of this scenario for robots B and C is to take advantage on the reliable trajectory estimates of robot A to enhance the
accuracy of their own trajectory estimates.   
[![robots video preview](https://img.youtube.com/vi/kDYtvIuryk8/mqdefault.jpg)](https://youtube.com/watch?v=kDYtvIuryk8&list=PLsTICVK4763uqu5JZEJriHjsgEPBdl9RI)
<img src="airmuseum_traj4.gif" width = 320 height = 251 />

### Scenario 5
In this last scenario,all the robots explore the whole South area of the hangar.
However, as opposed to all previous scenarios, they never meet each other, nor do they close loops along their own
trajectory. Hence, their only means to fuse information is to rely on delayed or indirect inter-robot correspondences. Many of them
are dispatched since all robots mostly follow each other to visit the same areas in a delayed fashion. This scenario thus
aims at assessing how successfully the robots can merge information without any direct inter-robot correspondences.   
[![robots video preview](https://img.youtube.com/vi/4Q-1OFxm2PA/mqdefault.jpg)](https://youtube.com/watch?v=4Q-1OFxm2PA&list=PLsTICVK4763uqu5JZEJriHjsgEPBdl9RI)
<img src="airmuseum_traj5.gif" width = 320 height = 251 />

## Related Paper:

If you use AirMuseum dataset in your work, please cite it as:


```
@inproceedings{dubois2020airmuseum,
  title={AirMuseum: a heterogeneous multi-robot dataset for stereo-visual and inertial Simultaneous Localization And Mapping},
  author={Dubois, Rodolphe and Eudes, Alexandre and Fr{\'e}mont, Vincent},
  booktitle={2020 IEEE International Conference on Multisensor Fusion and Integration for Intelligent Systems (MFI)},
  pages={166--172},
  year={2020},
  organization={IEEE}
}
```
