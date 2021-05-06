# Description of our NKDV code
Network kernel density visualization (NKDV) is one of the most important point pattern analysis methods, which has been supported by the ArcGIS software, using the SANET plugin [1]. However, NKDV is a computationally expensive operation, which is not scalable to million-scale datasets. As such, geographical users restrict the dataset size to be small-scale for using this operation. Here, we have developed three augmentation methods, which are: (1) aggregate distance augmentation (ADA), (2) interval-based augmentation (IA) and (3) hybrid augmentation (HA). These three methods significantly improve the theoretical efficiency (reduce the time complexity) and practical efficiency (5x to 10x speedup) for computing NKDV. This research work has been accepted in the prestigious conference VLDB [2]. In this Github link, we provide the implementation for our methods.

To compile our code, please use the shell script file (call_NKDV.sh). Unfortunately, since the size of the Github page is small, we do not attach the datasets here. If you would like to run our code, please download the point datasets (cf. references in Table 4) and utilize the software OSMNx [3] to extract the road network from different regions, Seattle, Atlanta, San Francisco and New York.

In the future, we plan to develop the visualization system (like our previous work [4]), based on our NKDV code, to support some meaningful applications, e.g., hotspot detection of traffic accidents, crime events and COVID-19 cases. In addition, we also plan to develop the software, called Fast-SANET, which can be much faster than the SANET plugin [1] for supporting different point pattern analysis methods in network. Furthermore, we will integrate this Fast-SANET plugin into the commonly-used GIS software, including QGIS and ArcGIS.

[1] SANET. http://sanet.csis.u-tokyo.ac.jp/ (last accessed: 2020-10-15).

[2] Tsz Nam Chan, Zhe Li, Leong Hou U, Jianliang Xu, Reynold Cheng. "Fast Augmentation Algorithms for Network Kernel Density Visualization" Proceedings of International Conference on Very Large Data Bases (PVLDB), 2021.

[3] Geoff Boeing, "Osmnx: New methods for acquiring, constructing, analyzing, and visualizing complex street networks" Computers, Environment and Urban Systems, 65:126 - 139, 2017.

[4] Tsz Nam Chan, Pak Lon Ip, Leong Hou U, Weng Hou Tong, Shivansh Mittal, Ye Li and Reynold Cheng. "KDV-Explorer: A near real-time kernel density visualization system for spatial analysis" (Webpage link: https://www.comp.hkbu.edu.hk/~edisonchan/system/KDV-Explorer.html)
