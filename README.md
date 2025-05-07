<h1 align="center">
    <img src="https://readme-typing-svg.herokuapp.com/?font=Righteous&size=35&color=00BFFF&center=true&vCenter=true&width=700&height=100&duration=7000&lines=Hello+Everyone+👋;I+hope+this+project+is+useful+to+you+❤;" />
</h1>

<p align="center">
  <img src="https://cainvas-static.s3.amazonaws.com/media/user_data/cainvas-admin/Signature.gif" alt="Signature GIF" width="600" />
</p>
<br>

# Signature Forgery Detection 🖊️🔍

This project leverages **machine learning** to detect forged signatures in documents by analyzing signature images. The model classifies signatures into two categories: **Genuine** (Real) ✅ and **Forged** (Fake) ❌.

## 📑 Table of Contents
1. [Project Overview](#project-overview)
2. [Steps Involved](#steps-involved)
3. [Technologies Used](#technologies-used)
4. [Example Workflow](#example-workflow)

## 📌 Project Overview
The goal of this project is to create a robust system capable of distinguishing between authentic signatures and forged signatures using **image processing** and **machine learning** techniques. The model uses **Histogram of Oriented Gradients (HOG)** for feature extraction and a **Support Vector Machine (SVM)** classifier for predicting the authenticity of the signatures.

### Key Features:
- **Genuine Signatures** ✅: Authentic signatures made by the individual.
- **Forged Signatures** ❌: Fake signatures that imitate the original signature.

## ⚙️ Steps Involved

### 1. Data Loading and Preprocessing 🖼️
- **Image Preprocessing**: 
  - Convert images to grayscale for consistent input 🖤.
  - Resize all images to a fixed size of 200x200 pixels 🔲.
  - Apply Gaussian blur to smooth the images and reduce noise 🌫️.
  
### 2. Feature Extraction Using HOG (Histogram of Oriented Gradients) 📊
The **HOG** technique is used to extract features from the signature images:
- HOG captures the gradient and edge orientations in an image, which are crucial for identifying unique characteristics of signatures 📐.
- The images are divided into cells and blocks, and the gradient information is used to generate feature vectors 📉.

### 3. Dimensionality Reduction Using PCA (Principal Component Analysis) 📉
- **PCA** is used to reduce the dimensionality of the feature set, making the data easier to handle and speeding up computation ⚡.
- This step enhances the performance of the model by focusing on the most significant features 🔍.

### 4. Model Training 🤖
- **SVM Classifier**: A **Support Vector Machine (SVM)** with a polynomial kernel is employed to classify signatures as "Real" or "Forge" 🤖.
- **Train-Test Split**: The dataset is split into training and testing sets to evaluate the model's accuracy and generalization capability 🔄.

### 5. Model Evaluation 📊
- **Confusion Matrix**: A confusion matrix is used to assess the performance of the model 💬.
- **Classification Report**: Metrics such as **precision** 📏, **recall** 📞, and **F1 score** 🏆 are computed to evaluate the model’s performance in detail.

### 6. Single Image Prediction 🖼️➡️📊
- The trained model can predict the authenticity of a signature from a single image by analyzing the HOG features and projecting them onto the PCA space 🎯.

## 🛠️ Technologies Used
- **Python** 🐍 for coding and algorithm development.
- **OpenCV** for image processing 🖼️.
- **scikit-image** for HOG feature extraction 🔬.
- **scikit-learn** for machine learning models (SVM, PCA, metrics) ⚙️.
- **Matplotlib** for visualization 📊.
- **NumPy** for numerical computation 🔢.

## ⚙️ Example Workflow:

### 1. Load the Dataset 📂:
The dataset consists of images of genuine and forged signatures, which are loaded and preprocessed.

### 2. Feature Extraction 📝:
Features are extracted from the signature images using HOG.

### 3. Dimensionality Reduction 🧠:
PCA is applied to reduce the dimensionality of the extracted features.

### 4. Model Training 🏋️:
The SVM classifier is trained on the processed data.

### 5. Prediction 🔮:
The trained model is then used to predict whether a given signature is real or forged.

## 🔚 Conclusion
This project showcases a practical application of **machine learning** and **image processing** to detect forged signatures, with high accuracy achieved using HOG feature extraction and SVM classification. It serves as a useful tool for automating signature verification in document security applications 🔒📜.
