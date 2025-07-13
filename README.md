 # 🧠 Skin Cancer Detection Using Hybrid Deep Learning Model (ResNet50 & EfficientNetB0)

This project presents an AI-powered system for **automated skin cancer detection** using a **hybrid deep learning model** that combines **ResNet50** and **EfficientNetB0** architectures. The model is trained and evaluated on the **HAM10000** dataset to classify common types of skin lesions.
The system is trained on the HAM10000 dataset and is capable of identifying 3 types of skin lesions: 

AKIEC (Actinic Keratoses)  
BCC (Basal Cell Carcinoma)  
NV (Melanocytic Nevi) 

## 🧠 Model Architecture

- **ResNet50**: Captures deep residual features.
- **EfficientNetB0**: Optimized for efficiency and accuracy with fewer parameters.
- **Fusion Strategy**: Feature vectors from both networks are concatenated and passed through fully connected layers for final classification.

## 🗂️ Dataset

- **Source**: [HAM10000 Dataset](https://www.kaggle.com/datasets/kmader/skin-cancer-mnist-ham10000)
- **Classes Used**:
  - `nv` – Melanocytic Nevi
  - `bcc` – Basal Cell Carcinoma
  - `akiec` – Actinic Keratoses
- **Preprocessing**:
  - Resized to `224x224`
  - Normalized pixel values to `[0, 1]`
  - Stratified train/val/test split


