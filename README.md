# Medical Image Enhancement (CLAHE & Histogram Equalization)

This is a small project I worked on to explore image enhancement techniques for medical X-rays, specifically focusing on skull fractures. The main goal was to see if I could make fracture details more visible by improving the contrast of the original images.

I experimented with two main techniques:
1.  **Global Histogram Equalization**: A standard approach to increase contrast.
2.  **CLAHE (Contrast Limited Adaptive Histogram Equalization)**: A more advanced method that improves local contrast without amplifying too much noise.

## What's in this repo?

The core of this project is a Jupyter Notebook (`exercise_4.ipynb`) that walks through the processing steps.

It covers:
*   Downloading the sample dataset automatically.
*   Loading a raw X-ray image.
*   Applying the different enhancement filters.
*   Plotting the results side-by-side for comparison.

## Tech Stack

I used **Python** for everything, relying on these libraries:
*   `opencv-python` (cv2) for the actual image processing algorithms.
*   `matplotlib` to display the before/after results.
*   `scikit-image` for simple image loading.
*   `kagglehub` to grab the dataset.

## The Dataset

I used a public Skull Fracture Dataset from Kaggle (`soumyaneelsarkar/skull-fracture-dataset-original`). The notebook is set up to just grab the latest version for you, so you don't need to manually download it.

## How to Run It

If you want to try this out on your own machine:

1.  Clone this repo:
    ```bash
    git clone https://github.com/Wirandy/CLAHE-Image-Processing.git
    cd CLAHE-Image-Processing
    ```

2.  Make sure you have the required libraries installed:
    ```bash
    pip install numpy matplotlib opencv-python scikit-image kagglehub
    ```

3.  Open up `exercise_4.ipynb` in Jupyter or VS Code and run the cells.

## Results Observations

When you run the notebook, you'll see a comparison image. From my testing, **CLAHE** tends to give much better results for medical imaging than standard Histogram Equalization. The standard equalization often blows out the brightness and highlights background noise too much, whereas CLAHE keeps the details recognizable while making the bone structures pop a bit more.

---
Created by [Wirandy](https://github.com/Wirandy)
