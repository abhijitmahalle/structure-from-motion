[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# Structure from Motion (SFM)
This repository contains code to reconstruct a 3D scene and simultaneoulsy obtain the camera poses of a monocular camera with respect to the scene using the set of 6 images from the camera and their feature-point correspondence. 

Following steps are involved:
* Feature Matching and Outlier rejection using RANSAC
* Estimating Fundamental Matrix
* Estimating Essential Matrix from Fundamental Matrix
* Estimate Camera Pose from Essential Matrix
* Check for Cheirality Condition using Triangulation
* Perspective-n-Point
* Bundle Adjustment

## Instruction to run the code:
```
python Wrapper.py --Path PATH_TO_DATA --Filtered False
```
## Result
Bundle Adjustment

<img src ="Data/Results/BundleAdjustment56.png" width=400/>
