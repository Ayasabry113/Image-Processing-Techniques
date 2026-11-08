# Fourier Transform and Frequency-Domain Filtering

An image-processing exercise demonstrating the 2D Discrete Fourier Transform (DFT) and circular Ideal Low-Pass and High-Pass filters.

## Contents
- Grayscale image loading with a portable fallback image
- 2D DFT and centered magnitude-spectrum visualization
- Ideal LPF and HPF mask construction
- Inverse DFT reconstruction
- Experiments with different cutoff radii

## Concepts
- **DFT:** Converts an image from the spatial domain to the frequency domain.
- **LPF:** Keeps low frequencies and suppresses high frequencies, producing smoothing.
- **HPF:** Suppresses low frequencies and keeps high frequencies, emphasizing edges and fine details.
- **Cutoff radius:** Controls the range of frequencies retained by the circular mask.

## Run
1. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Open `Fourier_Transform_and_Frequency_Domain_Filtering.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
3. Optionally place `Camerama.png` in the notebook's working directory. If it is unavailable, the notebook uses the built-in camera image from scikit-image.

## Tools
Python, OpenCV, NumPy, Matplotlib, and scikit-image.
