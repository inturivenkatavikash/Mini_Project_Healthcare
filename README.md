# HealthCare_AI_Project
# 🫁 Lung Cancer Detection Using Deep Learning

## 📌 Project Overview

This project is an **AI-powered Lung Cancer Detection system** that uses **Deep Learning and Transfer Learning** to classify lung CT scan images into four different diagnostic categories.

The system uses the **Xception pre-trained deep-learning model** as a feature extractor and a custom classification layer to predict the category of a given CT scan. The project also provides a complete web-based interface using **React** and **FastAPI**, allowing users to upload CT images and receive predictions through an interactive application.

> ⚠️ This project is developed as a prototype and decision-support system for educational and research purposes. It is not intended to replace professional medical diagnosis.

## 🎯 Objectives

* 🫁 Detect and classify lung CT scan images using Deep Learning.
* 🧠 Apply **Transfer Learning with Xception**.
* 🖼️ Preprocess CT images before model prediction.
* 🤖 Classify images into four diagnostic categories.
* ⚡ Develop a FastAPI backend for model inference.
* 💻 Build an interactive React frontend.
* 📊 Display prediction confidence and class probabilities.
* 🔍 Explore future explainability using techniques such as Grad-CAM.

## 🏷️ Diagnostic Classes

The model classifies CT images into the following four categories:

1. 🔴 **Adenocarcinoma**
2. 🔴 **Large Cell Carcinoma**
3. 🟢 **Normal**
4. 🔴 **Squamous Cell Carcinoma**

## 🗂️ Dataset

The project uses a CT image dataset containing:

* 📚 **613 training images**
* 🧪 **315 validation images**
* 🏷️ **4 diagnostic classes**

Because the dataset is relatively small for training a deep-learning model from scratch, **transfer learning** is used with the Xception architecture.

## 🧠 Model Architecture

The system uses:

**Xception Backbone**
⬇️
**Global Average Pooling**
⬇️
**Dense Layer**
⬇️
**Softmax Classification**
⬇️
**Four Diagnostic Classes**

The Xception backbone is kept frozen, while the final Dense classification layer is trained for the four-class prediction task.

### Model Configuration

* 🧠 Model: **Xception**
* 📐 Input Size: **350 × 350 × 3**
* 🔢 Output Classes: **4**
* ⚙️ Optimizer: **Adam**
* 📉 Loss Function: **Categorical Crossentropy**
* 📦 Batch Size: **8**
* 🔄 Maximum Epochs: **50**
* 🛑 Early Stopping: Enabled
* 🔄 Data Augmentation: Horizontal Flip

## 🔄 Image Preprocessing

The input CT image follows this pipeline:

**Load Image**
→ **Resize to 350×350**
→ **Convert to RGB Array**
→ **Add Batch Dimension**
→ **Normalize Pixel Values by 255**
→ **Xception Model**

The same preprocessing approach is maintained during inference to ensure consistency with model training.

## 🏗️ System Architecture

The complete application follows this workflow:

```text
👤 User
   ↓
💻 React Frontend
   ↓
📤 Upload CT Image
   ↓
⚡ FastAPI Backend
   ↓
🖼️ Image Preprocessing
   ↓
🧠 Xception Model
   ↓
📊 Softmax Prediction
   ↓
📦 JSON Response
   ↓
💻 React Results Page
```

The application returns:

* 🎯 Predicted class
* 📈 Confidence score
* 📊 Per-class probabilities

## 💻 Technology Stack

### Machine Learning

* 🐍 Python
* 🧠 TensorFlow
* 🤖 Keras
* 🧮 NumPy
* 🖼️ Pillow

### Backend

* ⚡ FastAPI
* 🚀 Uvicorn
* 🔗 REST API

### Frontend

* ⚛️ React
* ⚡ Vite
* 🎨 Lucide React

## 📊 Results

The model achieved approximately:

* 📚 **Training Accuracy:** 93.0%
* 🧪 **Validation Accuracy:** 65.6%

The difference between training and validation accuracy indicates **overfitting**. Therefore, the current system should be considered a prototype rather than a clinically validated diagnostic system.

## ⚠️ Limitations

* 📉 Relatively small dataset.
* 📊 Significant training-validation accuracy gap.
* 🧠 Only the final Dense layer is currently trained.
* 🔄 Limited data augmentation.
* 🏥 Not clinically validated for real-world diagnosis.
* 💾 The model uses a weights-only checkpoint and requires the corresponding architecture for loading.

## 🚀 Future Scope

Future improvements can include:

* 📚 Increasing the size and diversity of the dataset.
* 🧠 Fine-tuning the upper layers of Xception.
* 🔄 Applying stronger data augmentation techniques.
* 🔍 Adding **Grad-CAM** for model explainability.
* 📊 Performing more detailed evaluation using precision, recall, F1-score, and confusion matrices.
* 🐳 Containerizing the application using Docker.
* ☁️ Deploying the complete system with monitoring.
* 🏥 Further validation using appropriate clinical datasets.

## 🎯 Conclusion

This project demonstrates an **end-to-end deep-learning prototype for lung CT image classification**. By combining **Xception Transfer Learning, FastAPI, and React**, the project converts a trained machine-learning model into an interactive web-based application.

The project also highlights the importance of evaluating model generalization, as the difference between training and validation performance shows that additional improvements are needed before considering real-world clinical applications.

---

### 👨‍💻 Technologies Used

`Python` `TensorFlow` `Keras` `Xception` `Deep Learning` `Transfer Learning` `FastAPI` `React` `Vite` `NumPy` `Pillow`

### ⭐ Project Focus

**Artificial Intelligence • Deep Learning • Medical Image Classification • Computer Vision • Transfer Learning • Healthcare AI**
