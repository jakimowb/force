.. _comp_overview:

Overview
========

FORCE is a software framework and consists of several modules and executables. Following table summarizes all modules and programs with a short description. Click on the links for a more detailed description. 

All FORCE programs display a brief usage message when executing the program without arguments. 

A number of auxiliary files are needed (or are optional) and must be prepared as specified in section VII.

**Table 1.** :ref:`lower-level`.

+--------+------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Module | Program                | Level | Short description                                                                                                                                                                                                           |
+========+========================+=======+=============================================================================================================================================================================================================================+
| L1AS   | The FORCE Level 1 Archiving Suite is intended to assist in organizing and maintaining a clean and consistent Level 1 data pool, downloading of Sentinel-2 data, and maintaining file queues                                                                  |
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-level1-landsat   | 1     | Maintenance of Level-1 data pool, Landsat                                                                                                                                                                                   |
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-level1-sentinel2 | 1     | Download of data and maintenance of Level-1 data pool, Sentinel-2                                                                                                                                                           |
+--------+------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| L2PS   | The FORCE Level 2 Processing System is intended to generate Analysis Ready Data (ARD), i.e. harmonized, standardized and radiometrically consistent Level 2 products. This includes cloud and cloud shadow detection, radiometric correction and data cubing | 
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-level2           | 2     | Level 2 processing of image archives                                                                                                                                                                                        |
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-l2ps             | 2     | Level 2 processing of single image                                                                                                                                                                                          |
+--------+------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| WVDB   | The FORCE Water Vapor Database component can be used to generate and maintain a water vapor database used for atmospheric correction of Landsat data                                                                                                         | 
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-lut-modis        | /     | Generation and maintenance of water vapor database using MODIS products                                                                                                                                                     |
+--------+------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+



**Table 2.** :ref:`higher-level`.

+--------+------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Module | Program                | Level | Short description                                                                                                                                                                                                           |
+========+========================+=======+=============================================================================================================================================================================================================================+
| HLPS   | The FORCE Higher Level Processing System ...                                                                                                                                                                                                                 |
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-higher-level     | 3     | LEVEL3: Generate temporal aggregations of Level 2 ARD, i.e. pixel-based composites                                                                                                                                          |
+        +                        +-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        |                        | 3     | CSO: Clear Sky Observations statistics for Level 2-3 ARD data availability mining                                                                                                                                           |
+        +                        +-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        |                        | 3-4   | TSA: Time Series Analysis and Processing based on Level 2-3 ARD                                                                                                                                                             |
+        +                        +-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        |                        | 4     | ML: Machine Learning predictions based on any cubed features                                                                                                                                                                |
+        +                        +-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        |                        | 4     | TXT: Texture metrics based on any cubed features                                                                                                                                                                            |
+        +                        +-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        |                        | 4     | LSM: Landscape metrics based on any cubed features                                                                                                                                                                          |
+        +                        +-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        |                        | /     | SMP: Sampling of features for training/validation purposes                                                                                                                                                                  |
+        +                        +-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        |                        | 4     | FORCE CFIMP: Increase the spatial resolution of coarse continuous fields (like Land Surface Phenology) to Level 2 ARD resolution using the ImproPhe code                                                                    |
+        +                        +-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        |                        | 2     | FORCE L2IMP: Increase the spatial resolution of lower resolution Level 2 ARD using higher resolution Level 2 ARD using the ImproPhe code                                                                                    |
+--------+------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+



**Table 3.** :ref:`aux-level`.

+--------+------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Module | Program                | Level | Short description                                                                                                                                                                                                           |
+========+========================+=======+=============================================================================================================================================================================================================================+
| AUX    | force                  | /     | Print version, short disclaimer, available modules etc.                                                                                                                                                                     |
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-parameter        | /     | Generation of parameter files                                                                                                                                                                                               |
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-train            | /     | Training (and validation) of Machine Learning models                                                                                                                                                                        |
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-qai-inflate      | /     | Inflate QAI bit layers                                                                                                                                                                                                      |
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-tile-finder      | /     | Find the tile, pixel, and chunk of a given coordinate                                                                                                                                                                       |
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-tabulate-grid    | /     | Extract the processing grid as shapefile                                                                                                                                                                                    |
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-cube             | /     | ngestion of auxiliary data into datacube format                                                                                                                                                                             |
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-pyramid          | /     | Generation of image pyramids                                                                                                                                                                                                |
+        +------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|        | force-mosaic           | /     | Mosaicking of image chips                                                                                                                                                                                                   |
+--------+------------------------+-------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

