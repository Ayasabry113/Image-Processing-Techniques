# Edge Detection Techniques

This notebook demonstrates four classical edge detection methods on a grayscale image:

- Sobel operator
- Prewitt operator
- Laplacian operator
- Laplacian of Gaussian (LoG)

## Notebook workflow
1. Load a grayscale image and add Gaussian noise.
2. Implement a custom 2D convolution function.
3. Calculate Sobel and Prewitt gradient magnitudes and binary edge maps.
4. Apply the Laplacian and detect zero crossings.
5. Smooth with a Gaussian kernel, apply the Laplacian, and detect LoG zero crossings.
6. Compare the resulting edge maps.

## Improvements
The custom convolution uses floating-point output and reflected border padding to preserve negative derivative responses and avoid unsigned-integer overflow. Zero-crossing detection also uses a local contrast threshold.

## Run
```bash
pip install -r requirements.txt
```
Open `Edge_Detection_Techniques.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.

## Tools
Python, NumPy, Matplotlib, and scikit-image.
