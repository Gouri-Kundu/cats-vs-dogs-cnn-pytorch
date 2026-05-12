# Cats vs Dogs Image Classification using CNN

This project implements a Convolutional Neural Network (CNN) using PyTorch to classify images of cats and dogs.

The model was trained on the popular Cats vs Dogs dataset downloaded from Kaggle, containing nearly 25,000 images equally distributed between both classes.

---

# Project Overview

The project demonstrates an end-to-end deep learning workflow including:

- Data preprocessing
- Data augmentation
- CNN model building
- Model training and validation
- Early stopping
- Model checkpoint saving/loading
- Model evaluation
- Performance visualization

---

# Problem Statement

Develop a CNN-based image classification model that can distinguish between cat and dog images with high accuracy.

---

# Dataset

**Source:** [Kaggle Dataset](https://www.kaggle.com/datasets/bhavikjikadara/dog-and-cat-classification-dataset)

**Details:**
- Total Images: 24,998
- Classes:
  - Cat: 12,499
  - Dog: 12,499
- Balanced dataset with equal number of images in both classes

**Structure:**

```text
PetImages/
│
├── Cat/
├── Dog/

---

**# Technologies Used**

- Python
- PyTorch
- Torchvision
- Scikit-learn
- NumPy
- Matplotlib

---

**# Data Preprocessing & Augmentation**

**Training Transformations**
- Resize images to 150×150
- Random Horizontal Flip
- Random Rotation (±10°)
- Convert images to tensors
- Normalize pixel values

**Validation/Test Transformations**
- Resize images to 150×150
- Convert images to tensors
- Normalize pixel values

Data augmentation was applied to improve model generalization and reduce overfitting.

---

**# CNN Architecture**

**The custom CNN architecture consists of:**

- 3 Convolutional Blocks
- Batch Normalization
- ReLU Activation
- Max Pooling
- Adaptive Average Pooling
- Fully Connected Layers
- Dropout Regularization

**Architecture Flow:**

Input Image
   ↓
Conv2D → BatchNorm → ReLU → MaxPool
   ↓
Conv2D → BatchNorm → ReLU → MaxPool
   ↓
Conv2D → BatchNorm → ReLU → MaxPool
   ↓
AdaptiveAvgPool2D
   ↓
Fully Connected Layer
   ↓
Dropout
   ↓
Output Layer (Cat / Dog)

---

**# Training Details**

- Loss Function: CrossEntropyLoss
- Optimizer: Adam
- Learning Rate: 0.001
- Batch Size: 64
- Epochs: 30
- Early Stopping Patience: 5

The best-performing model was saved using model checkpointing.

---

**# Model Performance**

**Best Validation Accuracy**
90.58%

**Final Test Accuracy**
90.66%

---

**# Classification Report**

              precision    recall    f1-score    support

Cat              0.91       0.91       0.91       2506
Dog              0.91       0.91       0.91       2495

accuracy                                0.91       5001
macro avg         0.91       0.91       0.91       5001
weighted avg      0.91       0.91       0.91       5001

---

**# Training Visualization**

The training and validation loss curves were plotted to monitor learning behavior and detect overfitting during training.

<img width="872" height="612" alt="image" src="https://github.com/user-attachments/assets/aaa7b243-ea62-467d-971e-c2d81831cafc" />

---

**# Key Highlights**

- Built a custom CNN architecture from scratch
- Applied data augmentation techniques
- Implemented early stopping for regularization
- Achieved over 90% test accuracy
- Evaluated model using multiple performance metrics
- Saved and reloaded best-performing model checkpoints

---

**# Conclusion**

This project demonstrates a complete deep learning pipeline for binary image classification using CNNs in PyTorch.

The model achieved strong and balanced performance on unseen test data while maintaining good generalization ability.

---

**# Contact**

Feel free to connect for discussions, suggestions, or collaboration.

Email: gourikundu1808@gmail.com LinkedIn: www.linkedin.com/in/gouri-kundu
