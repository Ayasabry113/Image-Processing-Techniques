# Image Noise Removal: Spatial and Frequency Domain Filtering

An academic team project exploring image denoising techniques in the spatial and frequency domains. The notebook generates Gaussian, Salt-and-Pepper, and periodic noise, applies multiple filtering methods, and compares restored images using visual results and quantitative metrics.

> **Project status:** Initial GitHub release (v1). This is an academic team project. The notebook is being shared as a working version; further validation, parameter tuning, and documentation improvements may be added in future updates.

## Project Overview

The project studies three common image-noise models:

- **Gaussian noise** — additive random noise.
- **Salt-and-Pepper noise** — impulse noise that sets selected pixels to low or high intensity values.
- **Periodic noise** — structured sinusoidal interference.

The notebook implements filtering approaches in two domains.

### Spatial-domain filters

The notebook includes mean, weighted mean, Gaussian, geometric mean, harmonic mean, contra-harmonic mean, median, adaptive median, minimum, maximum, and alpha-trimmed mean filters.

### Frequency-domain filters

The notebook explores Ideal, Butterworth, and Gaussian filter families, including low-pass, band-reject, and notch-reject designs using Fourier-domain processing.

## Evaluation

Restoration results are compared with the original image using:

- **MSE (Mean Squared Error):** lower is better.
- **PSNR (Peak Signal-to-Noise Ratio):** higher is better.
- **SSIM (Structural Similarity Index):** higher is better.

### Selected results from the current notebook run

| Noise type | Best-performing method in the shown results | MSE | PSNR (dB) | SSIM |
|---|---|---:|---:|---:|
| Gaussian | Weighted Mean (lowest MSE / highest PSNR) | 189.460480 | 25.355617 | 0.610478 |
| Salt & Pepper | Adaptive Median | 54.018295 | 30.805395 | 0.946585 |
| Periodic | Gaussian Notch Reject (GNRF) | 9.735321 | 38.247301 | 0.956314 |

For Gaussian noise, the Gaussian filter produced the highest SSIM in the reported run (0.661762), while Weighted Mean produced the lowest MSE and highest PSNR. This illustrates that the metrics capture different aspects of restoration quality.

## Repository Structure

```text
Image-Noise-Removal/
├── Image_Noise_Removal.ipynb
├── README.md
└── requirements.txt
```

## Getting Started

### 1. Clone the repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd Image-Noise-Removal
```

### 2. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 3. Run the notebook

Open `Image_Noise_Removal.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab, then run the cells from top to bottom.

The notebook uses a standard grayscale test image and includes a fallback synthetic image path if the test image is unavailable.

## Team

This project was completed as a team assignment for the Image Processing course (Academic Year 2025/2026).

- Mohamed Ahmed Saleh
- Remon Maged
- Aya Sabry
- Nariman Mahmoud
- Alaa Hassan

## Notes and Future Improvements

This first published version is a working academic implementation. Potential future improvements include further validation of filter parameters, additional experiments for contra-harmonic filtering, broader quantitative evaluation, and runtime/performance comparisons.

## License

No license has been added yet. Unless a license is included, the repository remains under the default copyright terms; others do not automatically receive permission to reuse or redistribute the code. Add a license only after the team agrees on one.
