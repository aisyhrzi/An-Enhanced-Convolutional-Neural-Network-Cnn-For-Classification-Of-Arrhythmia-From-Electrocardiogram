# An-Enhanced-Convolutional-Neural-Network-For-Classification-Of-Arrhythmia-From-Electrocardiogram
Hi there! 👋 This is my final year project for my Bachelor of Computer Science at Universiti Teknologi Malaysia.
I developed an enhanced Convolutional Neural Network (CNN) to classify arrhythmia from scalogram images, transforming biomedical data into actionable healthcare insights.

## 💡 Project Overview 

Cardiovascular disease is a major cause of death worldwide. Early and accurate detection of arrhythmia (abnormal heart rhythms) is very important for patient care.
In this project, I built a deep learning pipeline using CNNs to classify different types of arrhythmia from ECG signals. I used image-based features (scalograms from CWT) and applied data balancing methods to improve model accuracy.

## 🔬 Main Features

Dataset: MIT-BIH Arrhythmia Database from PhysioNet

Signal Preprocessing: Denoising using Daubechies wavelets

Segmentation: ECG signals divided into chunks of 1000 samples

Feature Extraction: Continuous Wavelet Transform (CWT) to generate 2D scalogram images

Data Balancing: SMOTE, Tomek Links + SMOTE, and SMOTEENN

Model: Custom CNN (TensorFlow/Keras)

Evaluation: Compared with AlexNet, using metrics like accuracy, sensitivity, and specificity

## 🛠️ How It Works

Preprocessing: Clean and segment the ECG signals

Feature Extraction: Convert segments to 2D images with CWT

Balancing: Apply techniques for class balance

Training: Train a CNN model to classify types of arrhythmia

Evaluation: Test on unseen data, compare performance with benchmarks

## 🚀 Results

A comparative analysis was conducted to evaluate the overall performance metrics of three models 

M1 (Mohonta et al., 2022), 

M2 (Custom TensorFlow CNN),

M3 (AlexNet architecture)

![Picture1](https://github.com/aisyhrzi/An-Enhanced-Convolutional-Neural-Network-Cnn-For-Classification-Of-Arrhythmia-From-Electrocardiogram/blob/main/Picture1.jpg?raw=true)




## 🏥 Why It Matters

Accurate and automated arrhythmia detection can help doctors diagnose patients faster and more reliably. This project shows how deep learning and bioinformatics can support real healthcare solutions.

## 📚 
Due to large file size, the ECG data is not stored directly in this repository.
Please download the dataset from [PhysioNet MIT-BIH Database](https://physionet.org/content/mitdb/1.0.0/)
