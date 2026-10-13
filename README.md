# 🩺 Chest X-ray Pneumonia Detection

## 📌 Project Overview
This project uses the **Chest X-ray (Pneumonia) dataset from Kaggle** to classify chest X-ray images into two categories:
- **NORMAL** → Healthy lungs
- **PNEUMONIA** → Lungs showing infection (cloudy patches, fluid build-up)

The goal is to build a **Convolutional Neural Network (CNN)** that can automatically detect pneumonia from X-ray scans, supporting faster and more accurate diagnosis.

---

## 📂 Dataset Description
- Source: Kaggle Chest X-ray dataset (Guangzhou Women and Children’s Medical Center)
- Patients: Pediatric (ages 1–5 years)
- Approximate distribution:
- Training: ~5,000 images
- Validation: ~16 images
- Test: ~600 images

---

## ⚙️ Methodology
1. **Data Loading & Preprocessing**
 - Images resized to 128×128
 - Normalized pixel values (0–255 → 0–1)
 - Train/Val/Test split maintained

2. **Data Augmentation**
 - Random flips, rotations, zooms, and contrast adjustments
 - Purpose: Increase dataset diversity and prevent overfitting

3. **Model Architecture**
 - CNN with 3 convolutional layers + pooling
 - Dense layers with dropout for regularization
 - Sigmoid output for binary classification

4. **Training**
 - Optimizer: Adam
 - Loss: Binary Crossentropy
 - Metric: Accuracy
 - Epochs: 15

5. **Evaluation**
 - Tested on unseen data
 - Accuracy achieved: ~65% (baseline CNN)

---

## 📊 Results
- Training and validation curves plotted for accuracy and loss
- Data augmentation improved robustness
- Test accuracy ~65% (can be improved with transfer learning)

---

## 🧪 Future Improvements
- Apply **transfer learning** (ResNet50, VGG16, MobileNetV2) for higher accuracy
- Increase image size to 224×224 for more detail
- Handle class imbalance with class weights
- Deploy as a web app (Flask/Streamlit) for real-world use

---

## 🩺 Medical Suggestions
- **Clinical diagnosis must remain primary**: X-rays are only one part of pneumonia detection; doctors also rely on patient history and lab tests.
- **Early detection saves lives**: Pneumonia is a leading cause of death in children under 5; AI can assist in faster screening.
- **Limitations**: AI may misclassify due to poor image quality or overlapping conditions (e.g., tuberculosis, COVID-19).
- **Ethical use**: AI should support radiologists, not replace them. Patient privacy and data security must always be maintained.

---

## 🚀 How to Run
1. Clone the repository:
 ```bash
 git clone https://github.com/your-username/chest-xray-pneumonia.git

