# Laserfarm

[![Actions Status](https://github.com/eEcoLiDAR/Laserfarm/workflows/build%20and%20test/badge.svg?branch=development)](https://github.com/eEcoLiDAR/Laserfarm/actions)
[![codecov](https://codecov.io/gh/eEcoLiDAR/Laserfarm/branch/development/graph/badge.svg)](http://codecov.io/github/eEcoLiDAR/Laserfarm/branch/development)
[![Documentation Status](https://readthedocs.org/projects/Laserfarm/badge/?version=latest)](https://laserfarm.readthedocs.io/en/latest/?badge=latest)

Laserfarm provides a FOSS wrapper to [Laserchicken](https://github.com/eEcoLiDAR/laserchicken) supporting the use of
massive LiDAR point cloud data sets for macro-ecology, from data preparation to scheduling and execution
of distributed processing across a cluster of compute nodes.

## Installation

The package can be downloaded using `git`:
```shell script
git clone git@github.com:eEcoLiDAR/Laserfarm.git
```
It requires the [PDAL](https://pdal.io) and [GDAL](https://gdal.org) libraries and the PDAL Python 
bindings. These packages are most easily installed through `conda` from the `conda-forge` channel. The 
remaining dependencies can be retrieved and installed using `pip`:
```shell script
conda install pdal python-pdal gdal -c conda-forge
cd Laserfarm && pip install . 
```
Alternatively, a new environment with the package and all its dependencies can be created from the
YAML file provided:
```shell script
conda env create -f environment.yml
```

# Documentation

The project's full documentation can be found [here](https://laserfarm.readthedocs.io/en/latest/).

# Applications and Current Limitations

This package has been tested on data provided in a metric-based 2D-projected Cartesian coordinate system, i.e. the 
*[Actueel Hoogtebestand Nederland](https://www.pdok.nl/introductie/-/article/actueel-hoogtebestand-nederland-ahn3-)*. 
While some of the tools of Laserfarm could be applied to data in an ellipsoidal latitude/longitude coordinate system 
as well, this has not been tested and it is generally expected to fail. 

# Contributing

If you want to contribute to the development of Laserfarm,
have a look at the  [contribution guidelines](CONTRIBUTING.md).

# License

Copyright (c) 2020, Netherlands eScience Center

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.