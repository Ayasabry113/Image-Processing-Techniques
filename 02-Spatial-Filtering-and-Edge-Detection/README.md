# Spatial Filtering and Edge Detection

This project demonstrates classical image-processing techniques in the spatial domain.

## Topics covered

### Noise reduction
- Gaussian noise generation
- Mean filtering (`3×3`, `5×5`)
- Median filtering (`3×3`, `5×5`)
- Quantitative comparison using MSE, PSNR, and SSIM

### Edge detection
- Sobel X and Sobel Y gradients
- Gradient magnitude
- Laplacian edge response

## Dataset

The notebook uses built-in grayscale sample images from `scikit-image`:
- `data.camera()` for the noise-removal experiment
- `data.moon()` for edge detection

No external image files are required.

## Run the notebook

1. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Open `Spatial_Filtering_and_Edge_Detection.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
3. Run all cells from top to bottom.

## Notes

This is an educational implementation for comparing classical filtering and edge-detection methods. Results depend on the noise parameters and filter kernel sizes. The notebook reports metrics for the Gaussian-noise restoration experiment and uses visual inspection for edge-detection outputs.

## Future improvements

- Add Salt-and-Pepper noise experiments.
- Compare additional spatial filters.
- Apply Gaussian smoothing before Laplacian edge detection.
- Add threshold-based binary edge maps and parameter tuning.
