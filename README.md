# Image-Super-Resolution

## Introduction
This project explores the implementation and optimization of neural network-based approaches to image super-resolution, focusing primarily on the Super Resolution Convolutional Neural Network (SRCNN) and Fast Super Resolution Convolutional Neural Network (FSRCNN) architectures. Through seven model iterations, we experimented with different input sizes, scale factors, and specialized datasets to improve image upscaling quality. Using Peak Signal-to-Noise Ratio (PSNR) and Structural Similarity Index Measure (SSIM) as evaluation metrics. We achieved the best results with a category-restricted dataset that showed significant improvements over traditional bicubic interpolation.

## How to Use

### Setting Up the Environment
1. **Google Colab**: Open the provided notebook in Google Colab. You can place the notebook in any directory within your Colab environment.

2. **Dataset**: 
   - Download the datasets zip files (and all the extensions), extract them and re-zip them individually with the same names (arcDataset.zip, HighResTestSet.zip, ...), and upload them to the root folder of your Google Drive (`myDrive`). The compressed folders had to be divided to avoid GitHub's 100MB maximum file size.
   - Do not rename the dataset's zip files.

3. **Pre-Computed Models and Results**:
   - If you want to use pre-computed models and results (suggested), download the "SRCNN Models" folder and place it in the root folder of your Google Drive (`myDrive`).
   - This folder contains trained models and results that can be directly used for inference or further analysis.

## Demo
- The demo requires the same setup. 
- Images from the "Extra Demo Images" folder (or the HighResTestSet folder) should be drag-and-dropped into colab's runtime while executing the demo, and the name of the imported image at the start of the "Demo with Full Image Reconstruction" should be changed.

## Results Recap

Our best results were achieved with Model 6 (SRCNN) using the architecture dataset:
- PSNR: 35.92 dB (baseline: 33.96 dB)
- SSIM: 0.9477 (baseline: 0.8554)
- 2x scale factor with 256x256 input size

FSRCNN showed comparable results with 2x upscaling:
- PSNR: 34.16 dB
- SSIM: 0.9409
- Slightly faster execution time

For 3x upscaling, the FSRCNN Model performed significantly better:
- SRCNN: PSNR 33.55 dB, SSIM 0.8176
- FSRCNN: PSNR 32.60 dB, SSIM 0.8460