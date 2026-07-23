# 3D Scene Reconstruction from a Single 2D Image

## Project Overview

Modern techniques for reconstructing a 3D scene from a single 2D image aim to recover the spatial characteristics of objects as accurately and efficiently as possible. This project focuses on building a system that is robust to noise and artifacts in the input images, while also being versatile enough to work with a wide variety of data sources.

## Goals and Objectives

The goal of this work is to develop a system that provides:

* High accuracy in recovering depth and structural characteristics.
* Robustness to noise and artifacts in the input images.
* Versatility for working with different data sources.
* Speed and scalability.

Project objectives:

1. Analyze existing methods for extracting features from 2D images.
2. Investigate algorithms for generating 3D objects and their robustness.
3. Preprocess and augment images to improve feature quality.
4. Build a 3D scene generation pipeline, including the stages of depth reconstruction, point cloud formation, and 3D scene representation.
5. Integrate the individual solutions into a single architecture.

## Key Features

* Use of the DenseDepth model for depth estimation.
* Semantic enhancement of the input image to improve spatial relationships.
* Post-processing of several depth maps produced under different parameter settings of the image analysis methods, followed by their aggregation.
* Conversion of the depth map into a point cloud and subsequent 3D model reconstruction.
* Application of post-processing methods such as smoothing and outlier removal to improve the quality of the final model.
* Export of the results to popular formats (.obj, .ply).

## Algorithms and Methods

1. **Gradient-based methods**:

   * Chain Approximation for detecting object boundaries.
   * Watershed and K-Means for image segmentation.
2. **Depth map prediction**:

   * The DenseDepth model with post-processing (aggregation of several depth maps obtained from images with different parameters of the image analysis methods).
3. **Point cloud reconstruction**:

   * Use of camera parameters to generate coordinates in 3D space.
   * Statistical outlier removal.
4. **3D scene construction**:

   * Poisson Surface Reconstruction algorithm to build a continuous 3D mesh.

## Results

* Existing methods for predicting features for 3D scene generation were studied and investigated.
* An intermediate stage of semantic enhancement of the input image was introduced.
* Aggregation of depth maps to correct errors in local regions and to improve the accuracy of depth recognition for objects that were not previously present in the neural network's training set.
* High-quality point clouds with outlier removal.
* Generation of the final 3D scene.

## Examples

### Input image and depth map

 ![image](https://github.com/user-attachments/assets/1bb27d84-6b33-40b0-a3de-e054d3e92c59)

 ![image](https://github.com/user-attachments/assets/cbc3f0b0-5c04-414d-8826-38c27546c228)

### Depth map post-processing

![image](https://github.com/user-attachments/assets/81b25728-e3f4-462e-83b5-6f5d2a3ec818)


### Point cloud

![image](https://github.com/user-attachments/assets/d36eae97-6fb0-4626-850c-bb5e4f37f1c4)

![points](https://github.com/user-attachments/assets/24617ce4-3b07-4725-a355-51acdc3cc82c)

### Final 3D model

![image](https://github.com/user-attachments/assets/0a48e54b-e2e1-47c3-9a88-bc879581ea42)

![3dscene](https://github.com/user-attachments/assets/4e3a08a3-7717-4f38-b77c-b955250f9a5a)


## Authors

Developed as part of a master's thesis.
