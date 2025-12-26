# CLAHE Image Processing & Skull Fracture Enhancement

This project performs forensic image enhancement on X-ray/CT images of skull fractures. It utilizes **Global Histogram Equalization** and **CLAHE (Contrast Limited Adaptive Histogram Equalization)** to improve image contrast and visual quality, which is critical for medical diagnosis and forensic analysis.

## 📋 Table of Contents
- [About the Project](#about-the-project)
- [Techniques Used](#techniques-used)
- [Dataset](#dataset)
- [Prerequisites](#prerequisites)
- [Installation & Usage](#installation--usage)
- [Results](#results)

## 📖 About the Project
Medical imaging (like X-rays and CT scans) often suffers from poor contrast, making it difficult to identify fractures or specific details. This notebook demonstrates how to enhance these images using standard computer vision techniques. 

It compares three states:
1.  **Original Image**
2.  **Global Histogram Equalization** (Increases global contrast)
3.  **CLAHE** (Enhances local contrast while limiting noise amplification)

## 🛠 Techniques Used
*   **OpenCV (`cv2`)**: For image processing algorithms (Equalization, CLAHE).
*   **Matplotlib**: For visualization and comparing results side-by-side.
*   **Scikit-Image**: For reading image data.
*   **KaggleHub**: For downloading the dataset directly.

## 📊 Dataset
The project uses the **Skull Fracture Dataset** from Kaggle:
*   **Dataset ID**: `soumyaneelsarkar/skull-fracture-dataset-original`
*   The code automatically downloads the latest version of this dataset using `kagglehub`.

## ⚙️ Prerequisites
Ensure you have Python installed. You will need the following libraries:

*   `numpy`
*   `matplotlib`
*   `opencv-python`
*   `scikit-image`
*   `kagglehub`

## 🚀 Installation & Usage

1.  **Clone the repository**
    ```bash
    git clone https://github.com/Wirandy/CLAHE-Image-Processing.git
    cd CLAHE-Image-Processing
    ```

2.  **Install dependencies**
    ```bash
    pip install numpy matplotlib opencv-python scikit-image kagglehub
    ```

3.  **Run the Notebook**
    Open `exercise_4.ipynb` in Jupyter Notebook or VS Code to see the implementation and results.
    The notebook will:
    *   Download the dataset.
    *   Load a sample X-ray image (`597_0_3517.png`).
    *   Apply Global Histogram Equalization.
    *   Apply CLAHE with Clip Limit 2.0.
    *   Apply CLAHE with Clip Limit 3.0.
    *   Display the comparison plot.

## 🖼️ Results
The output is a visualization entitled **"Forensic Imaging Enhancement (X-ray/CT)"** showing:
1.  **Original**: The raw input image.
2.  **Global Histogram Equalization**: Often over-enhances background noise.
3.  **CLAHE (Clip=2, Tile=8x8)**: Balanced enhancement.
4.  **CLAHE (Clip=3, Tile=8x8)**: Stronger local contrast.

---
**Author**: [Wirandy](https://github.com/Wirandy)
