# Head Pose Estimation

## Overview
This project aims to estimate the head pose (pitch, yaw, and roll) using facial landmarks extracted from images. The methodology involves utilizing the MediaPipe library to extract facial landmarks, followed by training Support Vector Regression (SVR) models using the AFLW2000 dataset to predict the head pose angles.

![Head-Pose](https://github.com/Mahmoud2227/Head-Pose-Estimation/assets/89731900/1f2d2519-5e7e-4be5-87a0-a7a71d3f2b83)

## Demo
https://github.com/Mahmoud2227/Head-Pose-Estimation/assets/89731900/15b00577-1890-49f5-95d2-fce01eed747d

## Dependencies
- MediaPipe
- Scipy
- OpenCV (cv2)
- Matplotlib
- Pandas
- NumPy

## Dataset
The [AFLW2000](http://www.cbsr.ia.ac.cn/users/xiangyuzhu/projects/3DDFA/Database/AFLW2000-3D.zip) dataset was used for training the SVR models. This dataset provides images of faces along with ground truth annotations for head pose angles.

## Approach
1. Facial landmarks are extracted using MediaPipe, resulting in 468 landmarks.
2. The extracted landmarks are normalized to handle variations in face size across the dataset.
3. SVR models are trained using the normalized landmarks to predict the head pose angles.
4. The trained models are then utilized to predict the head pose angles for new images.

## Challenges
- Variation in face sizes across the dataset necessitated normalization of the extracted landmarks.
- Extracting pitch, yaw, and roll angles from the AFLW2000 dataset's annotations required utilizing the SciPy library to handle MAT files.

## Future Improvements
- Fine-tuning the SVR models to improve accuracy.
- Exploring other datasets for training to enhance model generalization.

## Credits
- **MediaPipe**: For providing a robust framework for facial landmark detection.
- **AFLW2000 Dataset**: For providing labeled data for head pose estimation.
- **SciPy, OpenCV, Matplotlib, Pandas, NumPy**: For providing essential tools and libraries used in the project.
