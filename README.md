# 🤖 Emotion Detection with Vision Transformer (ViT)

This project focuses on classifying facial emotions using a fine-tuned **Vision Transformer (ViT)** model.  
We used the **ViT-Base-Patch16-224** pretrained model and adapted its classification head to predict **seven emotions** from grayscale face images.

The work was done as part of a team project. This repository contains my contribution to the **ViT model**, including **data augmentation**, **model training**, and **evaluation**.

---

## 🧠 Dataset

We used the [FER 2013 dataset on Kaggle](https://www.kaggle.com/datasets/ananthu017/emotion-detection-fer/data), which contains **35,685 grayscale images** (48×48 pixels), categorized into seven emotions:

- 😠 angry  
- 🤢 disgusted  
- 😨 fearful  
- 😀 happy  
- 😐 neutral  
- 😢 sad  
- 😲 surprised  

The dataset is split into training and test sets. The *disgusted* class was underrepresented and required augmentation (see below).

---

## 🔍 Challenges

- **Imbalanced Classes**: e.g., `disgusted` was underrepresented  
  → Resolved via targeted augmentation (rotation, flips)  
- **Low Image Quality**: Some images were blurry or contained text artifacts  
- **Similar Emotions**: Even for humans, emotions like *fearful* and *sad* are hard to distinguish

---

## **🔧 Tech Stack & Methoden:**  

- **ViT Model**: [Google ViT-Base-Patch16-224](https://huggingface.co/google/vit-base-patch16-224)

- **Libraries**: PyTorch · Hugging Face Transformers  
- **Training Techniques**:
  - Data Augmentation (flips, rotation)
  - Weight Decay Regularization
  - Early Stopping · Learning Rate Scheduler
  - Cross-Entropy Loss
  - Self-Attention Mechanism

---

## 📈 Confusion Matrix – ViT Model

This matrix shows the model’s performance on the test set (normalized):

<img src="images/matrix.png" alt="Confusion Matrix" width="450"/>

---

## 🧾 Project Poster

The final poster summarizes all three models (CNN, Transfer Learning & ViT), their performance, challenges, and findings:

<img src="images/plakat.png" alt="Project Poster" width="700"/>

---

## 📄 License

This project was created as part of a university project at FHNW and is intended for demonstration and educational purposes only.