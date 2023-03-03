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
### Feature Matching using SIFT and RANSAC
![feature matching](https://user-images.githubusercontent.com/90370308/222005261-3c35443a-a23e-4ad1-9f88-b6f92a126ba5.png)

### Triangulation check for Cheirality Condition
![all_poses](https://user-images.githubusercontent.com/90370308/222008248-e8bec6d5-b87c-45df-89b6-08b1d9ce333b.png)

### Non-Linear Triangulation
![linear_nonlinear](https://user-images.githubusercontent.com/90370308/222008621-e1d88b49-75f6-461e-a8af-4798b1cd9ce9.png)

### Linear Camera Pose Estimation
![PnP56](https://user-images.githubusercontent.com/90370308/222008862-53869898-0084-4b9d-b764-46be92277d4e.png)

### Bundle Adjustment and Sparse Scene Reconstruction
![BundleAdjustment56](https://user-images.githubusercontent.com/90370308/222008894-d65dfeae-db6d-40e4-a173-2f51f451417c.png)
