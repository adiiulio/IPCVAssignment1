# Product Recognition of Food Products  
**Image Processing and Computer Vision – Assignment Module #1**  
University of Bologna  

## Overview

This project explores the development of a computer vision-based object detection system aimed at recognizing products on supermarket shelves using reference images of individual products. The system is designed to simulate real-world applications such as assisting visually impaired customers or enabling automated shelf management (e.g., detecting low-stock or misplaced items).

The task is divided into two main tracks:
- **Track A – Single Instance Detection**: Identify a single instance of each product in a shelf image.
- **Track B – Multiple Instance Detection**: Extend detection to multiple instances of the same product within the same image.

  ### Preprocessing
- Image denoising pipeline:
  - Median blur
  - Gaussian blur
  - Fast Non-local Means Denoising
  - Laplacian sharpening filter
- Reference and scene image paths are organized and indexed

### Detection Techniques

#### Track A – Single Instance Detection
- Keypoint matching using **SIFT**
- Matching refinement via **FLANN-based matcher**
- Homography estimation via **RANSAC**
- Output bounding boxes and object center positions

#### Track B – Multiple Instance Detection
- Iterative SIFT-based matching with keypoint filtering
- Histogram similarity (color-based) for false positive reduction
- Support for detecting repeated products in the same scene image

### Enhancements
- Added **color histogram comparison** to enhance robustness
- Custom visualization for bounding boxes and matched product overlays

---

## Tools & Libraries

- Python
- OpenCV
- NumPy
- Matplotlib
- scikit-image
- Google Colab
