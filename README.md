# MNIST Handwritten Digit Classification with Dropout

This project demonstrates how to build, train, and evaluate a neural network on the **MNIST dataset** using **Dropout** as a regularization technique to prevent overfitting.

---

## 📂 Dataset

- **Name:** MNIST Handwritten Digits
- **Samples:** 70,000 grayscale images (60,000 train / 10,000 test)
- **Image Size:** 28×28 pixels
- **Classes:** 10 (digits 0–9)
- **Format:** Grayscale, 8‑bit (0–255), normalized to [0, 1]

---

## 🏗 Model Architecture

- **Input Layer:** Flatten (28×28 → 784)
- **Dense Layer 1:** 512 units, ReLU activation
- **Dropout:** 0.5
- **Dense Layer 2:** 256 units, ReLU activation
- **Dropout:** 0.3
- **Output Layer:** 10 units, Softmax activation

---

## ⚙️ Training Configuration

- **Optimizer:** Adam
- **Loss Function:** Categorical Crossentropy
- **Batch Size:** 128
- **Epochs:** 10
- **Validation Split:** 20%

---

## 📊 Results

| Metric              | Training | Validation | Test Set |
|---------------------|----------|------------|----------|
| **Accuracy**        | 99.2%    | 98.1%      | **98.06%** |
| **Loss**            | 0.025    | 0.065      | 0.07     |

---

## 🔍 Confusion Matrix Insights

- **Strong classes:** `0`, `1`, `7` — very high precision and recall.
- **Common confusions:**
  - `5` ↔ `3` or `8`
  - `9` ↔ `4` or `7`
  - `8` ↔ `3`, `5`, `7`
- **Improvement ideas:** Data augmentation (rotation, shift, zoom), CNN architecture for spatial feature extraction.

---

## 📉 Training Curves

**Loss Curve**
- Train loss steadily decreases.
- Validation loss closely follows train loss → minimal overfitting.

**Accuracy Curve**
- Both training and validation accuracy rise and stabilize above 98%.
- Small gap between curves → good generalization.

---

