 # 🧠 Skin Cancer Detection Using Hybrid Deep Learning Model (ResNet50 & EfficientNetB0)

This project presents an AI-powered system for **automated skin cancer detection** using a **hybrid deep learning model** that combines **ResNet50** and **EfficientNetB0** architectures. The model is trained and evaluated on the **HAM10000** dataset to classify common types of skin lesions.
The system is trained on the HAM10000 dataset and is capable of identifying 3 types of skin lesions: 

AKIEC (Actinic Keratoses)  
BCC (Basal Cell Carcinoma)  
NV (Melanocytic Nevi) 

## 📄 Abstract

Skin cancer is one of the most common and potentially life-threatening cancers worldwide. Early and accurate detection is critical. This project proposes a **hybrid deep learning model** combining **ResNet50** and **EfficientNetB0**, trained on the HAM10000 dataset to classify skin lesions. Techniques like **data augmentation**, **transfer learning**, and **feature fusion** significantly enhance classification accuracy.

## 📂 Dataset

- **Name:** HAM10000 (Human Against Machine with 10000 training images)
- **Source:** ISIC Archive
- **Classes Used:**
  - Actinic Keratoses (AKIEC)
  - Basal Cell Carcinoma (BCC)
  - Melanocytic Nevi (NV)
- **Preprocessing:**
  - Resized to `224x224` pixels
  - Normalized pixel values to [0, 1]
  - Label extraction via `dx` column
  - Stratified split into training, validation, and test sets

## 🧠 Model Architecture

- **Backbones:**
  - ResNet50
  - EfficientNetB0
- **Fusion Strategy:**
  - Feature extraction from both networks
  - Concatenation of feature vectors
  - Dense layers with dropout and ReLU activation
- **Output Layer:** Softmax (3-class classification)

## 🚀 Training & Evaluation

- **Loss Function:** Categorical Cross-Entropy
- **Optimizer:** Adam
- **Metrics Used:**
  - Accuracy
  - Precision, Recall, F1-Score
  - ROC & PR Curves

## 📊 Performance

- **Classification Accuracy (on test set):** High performance across all three classes
- **Visualization:**
  - Training & Validation Accuracy/Loss
  - ROC and PR Curves
  - Image-wise prediction results
- **Model Interpretation:** (Explainability tools like Grad-CAM are part of future work)
  
## ✅ Advantages

- Combines the best features of ResNet50 and EfficientNetB0
- Outperforms individual models in classification accuracy
- Supports real-time prediction in clinical setups
- Scalable for mobile and embedded platforms

## ⚠️ Limitations

- Requires high-performance hardware (GPU) for training
- Currently limited to 3 lesion classes
- Grad-CAM and explainability not yet integrated
- Performance may drop with low-quality or unbalanced datasets

## 🔮 Future Scope

- Expand to all 7 classes of HAM10000
- Integrate Grad-CAM for explainability
- Deploy model on mobile/edge devices
- Use federated learning for privacy-focused clinical deployment
- Include clinical metadata (age, sex) to improve prediction

