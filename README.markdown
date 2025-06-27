# Computer Vision and Image Processing - Assignment 2

## Overview
This repository contains the implementation of two image processing techniques as part of the **EC7212 - Computer Vision and Image Processing** take-home assignment by **JATHUSAN U. (EG/2020/3977)**. The project includes:

1. **Otsu's Thresholding Algorithm**: Applied to a synthetic image with Gaussian noise to segment objects.
2. **Region-Growing Technique**: Used for image segmentation starting from seed points.

## GitHub Repository
- [Project Link](https://github.com/Jathusan19//Computer_Vision2)

## Requirements
- Python 3.x
- Libraries:
  - `numpy`
  - `opencv-python`
  - `matplotlib`

Install the required libraries using:
```bash
pip install opencv-python scikit-image
```

## Files
- `EG-2020-3977.pdf`: Assignment document with problem statements and code snippets.
- `ComputerVision_2.ipynb`: Jupyter Notebook containing the complete implementation and visualizations.

## Implementation Details

### 1. Otsu's Thresholding
- **Description**: Implements Otsu's method to automatically determine an optimal threshold for segmenting a noisy image with two objects (a circle and a rectangle) and a background.
- **Steps**:
  - Creates a synthetic image with pixel values (0 for background, 100 for circle, 200 for rectangle).
  - Adds Gaussian noise to the image.
  - Computes the histogram and applies Otsu's algorithm to find the threshold.
  - Visualizes the original, noisy, and thresholded images.
- **Code Location**: `ComputerVision_2.ipynb` (Cell 2)

### 2. Region-Growing Technique
- **Description**: Implements a region-growing algorithm to segment an image starting from seed points within the object of interest.
- **Steps**:
  - Loads a grayscale image (e.g., `chairImage.jpg`).
  - Defines seed points to initiate the growth process.
  - Recursively adds neighboring pixels within a specified intensity threshold.
  - Visualizes the original and segmented images.
- **Code Location**: `EG-2020-3977.pdf` (Page 5) and `ComputerVision_2.ipynb` (additional implementation possible).

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/Jathusan19/ComputerVision2.git
   cd ComputerVision2
   ```
2. Open `ComputerVision_2.ipynb` in Jupyter Notebook or any compatible environment.
3. Run the cells to generate and visualize the results.
4. For the region-growing technique, ensure the input image (`chairImage.jpg`) is in the working directory or update the path in the code.

## Results
- **Otsu's Thresholding**: The output shows the original image, the noisy image, and the binary image after applying Otsu's thresholding with the computed threshold value.
- **Region-Growing**: The output displays the original image and the segmented image based on the seed points and threshold.

## Visualization
- The Jupyter Notebook includes plots for both techniques:
  - Otsu's: 3-in-1 plot (Original, Noisy, Thresholded).
  - Region-Growing: Side-by-side comparison (Original, Segmented).

## Notes
- Ensure all dependencies are installed before running the code.
- Adjust seed points and threshold values in the region-growing code as needed for different images.
- The synthetic image for Otsu's thresholding is generated programmatically; no external image file is required.

## License
This project is for educational purposes only. Feel free to use and modify the code, but please credit the original author.
