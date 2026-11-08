# Contrast Stretching — Image Enhancement

A compact image-processing exercise demonstrating **min–max contrast stretching** on a grayscale image. The notebook compares the original and enhanced image, plots both intensity histograms, and reports basic intensity statistics.

## Method

The input intensity range `[I_min, I_max]` is linearly mapped to `[0, 255]`:

`I_out = ((I_in - I_min) / (I_max - I_min)) * 255`

The implementation handles invalid inputs and constant-intensity images to avoid division by zero.

## Run the notebook

1. Open `Contrast_Stretching.ipynb` in Google Colab or Jupyter Notebook.
2. Install the dependencies listed in `requirements.txt`.
3. In Colab, upload an image when prompted. For local execution, set `IMAGE_PATH` to an image file path.
4. Run all cells.

## Technologies

- Python
- OpenCV
- NumPy
- Matplotlib

## Scope and limitations

This notebook applies global min–max contrast stretching. It can amplify noise and does not perform local/adaptive contrast enhancement.

## Source

Consolidated and improved from the two original Image Processing coursework notebooks (`IP.task-1.ipynb` and `IP.task-1.1.ipynb`).
