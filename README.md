# Task 2: MNIST Digit Classification

## 📌 Project Overview
This project builds a **Convolutional Neural Network (CNN)** using PyTorch to classify handwritten digits (0-9) from the MNIST dataset. The model achieves **98.96% accuracy** on the test set.

---

## 🎯 Problem Statement
Handwritten digit recognition is a classic computer vision problem. The goal is to correctly classify 28x28 grayscale images of handwritten digits into 10 classes (0-9).

---

## 📊 Dataset
| Attribute | Details |
|-----------|---------|
| **Name** | MNIST Dataset |
| **Training Images** | 60,000 |
| **Test Images** | 10,000 |
| **Image Size** | 28x28 pixels (Grayscale) |
| **Classes** | 10 (digits 0-9) |

---

## 🏗️ Model Architecture
```
Input: 28x28x1 (Grayscale)
    ↓
Conv2D(32) + ReLU + MaxPool2D
    ↓
Conv2D(64) + ReLU + MaxPool2D
    ↓
Flatten
    ↓
Dense(128) + ReLU + Dropout(0.3)
    ↓
Dense(10) + Softmax
    ↓
Output: Digit (0-9)
```

---

## 📈 Results

### Overall Performance
| Metric | Score |
|--------|-------|
| **Test Accuracy** | **98.96%** |
| Precision (Avg) | 0.99 |
| Recall (Avg) | 0.99 |
| F1-Score (Avg) | 0.99 |

### Per-Digit Performance
| Digit | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| 0 | 0.99 | 1.00 | 0.99 |
| 1 | 0.99 | 1.00 | 1.00 |
| 2 | 0.99 | 0.99 | 0.99 |
| 3 | 0.99 | 0.99 | 0.99 |
| 4 | 0.99 | 0.98 | 0.99 |
| 5 | 0.99 | 0.99 | 0.99 |
| 6 | 0.99 | 0.99 | 0.99 |
| 7 | 0.98 | 0.99 | 0.99 |
| 8 | 0.99 | 0.99 | 0.99 |
| 9 | 0.99 | 0.99 | 0.99 |

### Training Progress
| Epoch | Train Accuracy | Test Accuracy |
|-------|---------------|---------------|
| 1 | 93.69% | 98.66% |
| 2 | 98.08% | 98.76% |
| 3 | 98.61% | 99.04% |
| 4 | 98.88% | 98.96% |
| 5 | 99.04% | 98.96% |

---

## 🛠️ Technologies Used
- **Python 3.x**
- **PyTorch** - Deep Learning framework
- **Torchvision** - Dataset handling
- **Matplotlib, Seaborn** - Visualization
- **Google Colab** - GPU acceleration (T4)

---

## 🚀 How to Run

### Prerequisites
```bash
pip install torch torchvision matplotlib seaborn scikit-learn
```

### Run the Code
```bash
python "deep learning"
```

### Load Saved Model for Inference
```python
import torch
from deep learning import SimpleCNN

# Load model
model = SimpleCNN()
model.load_state_dict(torch.load('mnist_cnn.pth'))
model.eval()

# Predict digit
def predict_digit(image):
    with torch.no_grad():
        output = model(image.unsqueeze(0))
        _, pred = torch.max(output, 1)
    return pred.item()
```

---

## 📁 Repository Structure
```
Task2_DeepLearning/
├── mnist_cnn.pth        # Trained model weights
├── Deep_learning        # Python code file
└── README.md            # Project documentation
```

---

## 👩‍💻 Author
**SADHANA A**

---

## 📅 Date
June 2026

**✅ Task 2 Complete!**
```

---

## 🎯 **Now Do This:**

1. Go to: https://github.com/SadhanaArul/Task2_DeepLearning
2. Click **README.md**
3. Click **✏️ (pencil icon)** to edit
4. **Delete everything** (Ctrl+A → Delete)
5. **Paste** the content above (Ctrl+V)
6. Click **"Commit changes"**

---
