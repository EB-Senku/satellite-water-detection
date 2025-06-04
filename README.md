# Water Body Detection from Satellite Images

This project is part of my learning journey in computer vision and machine learning. The goal is to detect **water bodies (lakes, rivers, etc.)** from satellite images using various techniques — from classical machine learning with feature compression, to deep learning feature extraction with CNNs.

> ⚠️ This is **not** a production-ready or end-to-end solution, but a step-by-step educational exploration.

---

##  Dataset

I used the **EuroSAT RGB dataset**, which contains labeled satellite images across multiple land use classes. For this project, classes were grouped into:
- **Water**: `River`, `SeaLake`
- **Non-Water**: All other classes

---

##  Methods Explored

### 1.  Feature Compression + Classical ML
- **Grayscale conversion**
- **SVD (Truncated SVD)** to reduce dimensionality
- **Random Forest classifier**
- Use of **SMOTE** and **CLASS WEIGHTING** to address class imbalance

### 2.  CNN Feature Extraction + XGBoost
- Features extracted using **ResNet18** (pretrained on ImageNet)
- Classifier: **XGBoost**
- Achieved significant improvement in **water recall** and overall accuracy

---

##  Results

| Model                   | Water Recall | Accuracy |
|------------------------|--------------|----------|
| Random Forest + SVD    | ~38–64%      | ~88%     |
| CNN Features + XGBoost | **91%**      | **98%**  |




