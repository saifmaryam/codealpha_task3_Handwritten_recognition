# ✍️ Handwritten Character Recognition

> **CodeAlpha Machine Learning Internship — Task 3**

Identify handwritten **alphabets (A–Z)** and digits from 28×28 grayscale images using a Deep Convolutional Neural Network.

---

## 📌 Objective
Build a CNN-based image classifier that reads handwritten characters with high accuracy, extendable to full word recognition.

## 📊 Dataset
- **Primary:** EMNIST Letters — 26 classes (A–Z) | ~145,600 samples | Auto-downloaded ✅
- **Fallback:** MNIST Digits — 10 classes (0–9) | 70,000 samples | Auto-downloaded ✅

## 🤖 Model — Deep CNN Architecture
```
Input (28 × 28 × 1 grayscale)
│
├─ Block 1: Conv2D(32) → BN → Conv2D(32) → BN → MaxPool → Dropout(0.25)
├─ Block 2: Conv2D(64) → BN → Conv2D(64) → BN → MaxPool → Dropout(0.30)
├─ Block 3: Conv2D(128)→ BN → Conv2D(128)→ BN → GlobalAvgPool → Dropout(0.40)
│
└─ Dense(256) → BN → Dropout → Dense(n_classes, softmax)
```

## 📈 Results
| Dataset | Test Accuracy |
|---------|:------------:|
| MNIST Digits (0–9) | ~99.3% |
| EMNIST Letters (A–Z) | ~88–92% |

## ✨ Key Features
- ✅ Auto dataset download — no manual setup
- ✅ Data Augmentation (rotation, shift, zoom)
- ✅ Early Stopping + LR Scheduler
- ✅ Per-class accuracy visualization
- ✅ Confusion Matrix heatmap
- ✅ Live inference demo on test samples
- ✅ Model saved as `.keras` file

## 🚀 Run on Google Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

1. Upload `handwritten_recognition.ipynb` to Colab
2. `Runtime → Change runtime type → GPU` ⚡
3. `Runtime → Run All`
4. Dataset downloads automatically!

## 🛠️ Tech Stack
`Python` · `TensorFlow/Keras` · `TensorFlow Datasets` · `NumPy` · `Matplotlib` · `Seaborn` · `Scikit-learn`

## 📁 Output Files
| File | Description |
|------|-------------|
| `task3_samples.png` | Dataset sample grid |
| `task3_results.png` | Full results dashboard |
| `task3_best_model.keras` | Best trained model |

---

*Built with ❤️ during CodeAlpha ML Internship*
