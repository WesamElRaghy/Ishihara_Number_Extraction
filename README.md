# Ishihara_Number_Extraction

## Overview
This repository contains two implementations for extracting numbers from Ishihara color blindness test images using K-means clustering.

## Code 1: Standard K-means Implementation

### Description
A streamlined implementation using binary clustering (k=2) in the LAB color space.

### Key Features
- Uses LAB color space 'a' channel (red-green component)
- Fixed k-means clustering with k=2  
- Automatic cluster selection based on minimum pixel count
- Binary output (green number on black background)

### Characteristics
- Universal parameters across all images
- Dynamic cluster selection
- Efficient processing pipeline 
- Minimal parameter configuration

## Code 2: Optimized K-means Implementation

### Description
A parameter-tuned version with image-specific clustering and morphological refinements.

### Key Features
- Image-specific k values (k=19 or k=25)
- Predetermined target clusters for each image
- Morphological operations for dot enhancement
- Enhanced color saturation

### Technical Parameters
- k=19 for image '6'
- k=25 for images '12', '42', and '74'
- Custom target clusters per image
- MORPH_ELLIPSE kernel (5,5) for dilation

### Characteristics  
- Precise number extraction
- Customized processing per image
- Enhanced visual clarity
- Optimized dot representation

## Dependencies
- NumPy
- OpenCV (cv2)
- Matplotlib 
- Scikit-learn

## Usage
Both implementations process images named:
- '6.jpg'
- '12.jpg'
- '42.jpg'
- '74.jpg'

and display the original and extracted numbers side by side.

---
Note: This implementation is designed for specific Ishihara test images and may require parameter adjustments for different images.
