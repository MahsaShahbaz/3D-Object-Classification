# 3D Object Classification Using Voxel Grid Structure

This repository contains the implementation of a deep learning framework for classifying three-dimensional objects using voxel grid structures. The project integrates ideas from VoxNet and ORION, leveraging Convolutional Neural Networks (CNNs) for feature extraction and classification.

## Overview

3D object classification is a critical task in applications involving computer vision and spatial data analysis. This project uses voxel grid neural networks to process volumetric data, allowing for effective 3D shape recognition and categorization. The method is tested on the ModelNet10 dataset.

**Key Features:**
- Voxelization of 3D CAD models.
- CNN-based feature extraction and classification.
- Integration of batch normalization, dropout, and pooling for improved training stability and performance.
- Data augmentation for increased dataset diversity.

## Architecture

The extended architecture includes:
- Four Convolutional Neural Network (CNN) layers.
- Two fully connected layers.
- Batch normalization after each CNN layer.
- Dropout for regularization.
- Average pooling for faster training and better accuracy.

### Key Hyperparameters
| Layer  | Filters | Kernel Size | Stride | Padding | Dropout Ratio | Batch Normalization |
|--------|---------|-------------|--------|---------|---------------|---------------------|
| Conv1  | 32      | 3           | 2      | 1       | 0.2           | Yes                 |
| Conv2  | 64      | 3           | 1      | 1       | 0.3           | Yes                 |
| Conv3  | 128     | 3           | 1      | 1       | 0.4           | Yes                 |
| Conv4  | 256     | 3           | 1      | 1       | 0.6           | Yes                 |
| FC1    | 128     | -           | -      | -       | 0.4           | No                  |
| FC2    | 10      | -           | -      | -       | -             | No                  |

## Results

The proposed method outperforms the standard VoxNet in terms of speed and accuracy:
- **Achieved validation accuracy:** 90.86%
- **Average training time per epoch:** 40.10 seconds

**Comparative Analysis:**
- Batch normalization and dropout significantly reduced overfitting.
- Average pooling improved training speed without compromising accuracy.
- Data augmentation increased model robustness, especially for smaller batch sizes.

## Dataset

The ModelNet10 dataset is used for training and testing. The dataset includes 10 categories of CAD models, voxelized to a grid size of 32x32x32. Data augmentation techniques like flipping and tensor conversion were applied.

## Acknowledgments

This project was developed as part of the **Neural Networks and Deep Learning** course at the **University of Padova**, during the **Master's program in ICT for Internet and Multimedia**.

Team Members:
- Mohammadmostafa Talebi
- Mahsa Shahbazi
- Seyedali Hosseinishamoushaki

Project Date: July 5, 2023
