# Advanced Image Processing for Bone Fracture Detection

![Upcoming Publication](https://img.shields.io/badge/Publication-ICONIC25-blue)

> This repository accompanies a research study on enhancing and detecting bone fractures in medical X‑ray images using advanced preprocessing techniques and machine learning models. Presented at Panimalar Engineering College’s ICONIC25 conference.

---

## 📄 Abstract

Medical X‑ray imaging is essential for diagnosis but often suffers from low contrast, noise, blur, and poor illumination. This study integrates advanced image enhancement methods—smoothing filters (minimum, median), sharpening filters (Laplacian, high‑pass), and CLAHE (Contrast Limited Adaptive Histogram Equalization)—with machine learning classifiers (Decision Trees, KNN, SVM, Random Forest, Linear Regression) to improve automated fracture detection accuracy. CLAHE and minimum smoothing delivered the best balance between clarity and detail preservation, and the Decision Tree classifier emerged as the most effective for clinical application.

---

## 🎯 Objectives

- **Enhance** low‑quality X‑ray images under challenging conditions (low light, high noise, low contrast).
- **Compare** multiple enhancement techniques: minimum & median smoothing, Laplacian & high‑pass sharpening, and CLAHE.
- **Evaluate** the impact of preprocessing on fracture detection performance across various machine learning models.
- **Identify** the optimal enhancement-model pipeline for real‑world clinical use. citeturn0file0

---

## 🗂 Repository Structure
- **Image Processing Techniques/**
  - Jupyter notebooks implementing various enhancement methods:
    - Minimum and median smoothing filters
    - Laplacian and high-pass sharpening filters
    - CLAHE implementation and analysis
  - Image comparison utilities (PSNR, MSE, SSIM metrics)
  <br>- **Dataset/**
    - Training and testing datasets (not included in repository)
    - Results and performance metrics


- **Bone Fracture Detection Using CLAHE/**
  - Implementation of the CLAHE enhancement pipeline
  - Fracture detection analysis notebooks
  - Class-based processor for batch image enhancement
  - Classifier implementations (Decision Tree, KNN, SVM, etc.)
  - Feature extraction and evaluation scripts
  - Model performance comparison tools

---

## 🛠️ Technologies & Libraries

- **Python 3.9+**
- **OpenCV** for image processing
- **NumPy** for array operations
- **scikit-learn** for machine learning models and metrics
- **Matplotlib** for plotting histograms, ROC curves, and SSIM comparisons
- **Jupyter** for interactive analysis

---

## 📊 Dataset Details

- **Total images**: 9,463 (8,863 training, 600 testing). citeturn0file0
  - Training fractured: 4,480
  - Training non‑fractured: 4,383
  - Testing fractured: 360
  - Testing non‑fractured: 240
- **Preprocessing**: resized to 64×64 pixels, grayscale conversion, normalized to [0,1]. citeturn0file0

---

## 🔍 Enhancement Techniques

1. **Minimum & Median Smoothing**
   - Median filter reduces impulse noise with edge preservation (minimal blur).
   - Minimum filter reduces noise but can blur fine details.
2. **Laplacian & High‑Pass Sharpening**
   - Laplacian enhances edges via second‑order derivatives (amplifies noise).
   - High‑pass filtering highlights high‑frequency components.
3. **CLAHE**
   - Local histogram equalization with contrast limit avoids over-amplification of noise. Proven most effective for fracture visibility. citeturn0file0

---

## 🤖 Machine Learning Pipeline

1. **Feature Input**: Flattened pixel intensities and histogram-based features from original and enhanced images.
2. **Classifiers**:
   - Logistic Regression (baseline)
   - K‑Nearest Neighbors (KNN)
   - Support Vector Machine (SVM)
   - Decision Tree (best trade-off of accuracy & interpretability) citeturn0file0
   - Random Forest
3. **Evaluation Metrics**: Accuracy, Precision, Recall, F1-Score, ROC‑AUC. citeturn0file0

---

## 📈 Key Results

- **Image Enhancement**:
  - CLAHE achieved PSNR = 44.59, MSE ≈ 0, SSIM = 0.98, outperforming median (PSNR=24.51, SSIM=0.62) and minimum (PSNR=28.42, SSIM=0.92). citeturn0file0
- **Fracture Detection**:
  - Decision Tree on CLAHE dataset: Accuracy = 0.79, F1 (fractured) = 0.82, F1 (non‑fractured) = 0.75.
  - KNN on original dataset: Accuracy = 0.76 (close runner‑up). citeturn0file0

---

## 🚀 Getting Started
1. **Clone the repository**
   ```bash
   git clone https://github.com/Saisandeepsangeetham/Advanced-Image-Processing-for-Bone-Fracture-Detection.git
   cd Advanced-Image-Processing-for-Bone-Fracture-Detection
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Dataset preparation**
   - Place your X-ray images in the appropriate data directory
   - Make sure they follow the required format (64×64 pixels, grayscale)

4. **Image enhancement**
   - Run the enhancement notebooks in the "Image Processing Techniques" folder
   ```bash
   cd "Image Processing Techniques"
   jupyter notebook "Image Enhancement And Analysis.ipynb"
   ```

5. **Fracture detection**
   - Use the CLAHE-enhanced images with the machine learning pipeline
   ```bash
   cd "../Bone Facture Detection Using CLAHE"
   jupyter notebook "Bone Fractured Detection Analysis.ipynb"
   ```

6. **Model evaluation**
   - Compare different classifiers' performance using the provided metrics
   - Analyze results to determine the most effective enhancement-model pipeline

---

## 📚 References

1. Saisandeep S., Shankari S.R., Shiva K.S.V., Priyadharsini R., "Optimizing Medical X‑ray Image Quality...", Sri Sivasubramaniya Nadar College of Engineering, 2025.  
2. Hage Chehade A. et al., "Classification of Lung Diseases...", SN Comput. Sci., 2024.  
3. Singh A., Sharma M., Bhattacharya M., "Automated Semantic Segmentation...", IEEE IBSSC, 2021.  
4. Zhang Y. et al., "Frequency space mamba...", Proc. SPIE 13242, 2024.  

---


