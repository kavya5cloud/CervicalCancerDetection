# Cervical Cancer Detection using CNN
### A Scalable Screening System for Early Detection in Resource-Constrained Healthcare
Settings

![Python](https://img.shields.io/badge/Python-3.8+-blue) ![TensorFlow](https://img.shields.io/badge/Framework-TensorFlow%2FKeras-orange) ![Accuracy](https://img.shields.io/badge/Accuracy-94.15%25-brightgreen) ![Dataset](https://img.shields.io/badge/Dataset-SIPaKMeD-purple)

---

##  Overview

A machine learning system for **real-time cervical cancer detection** from Pap smear images using Convolutional Neural Networks (CNN). Built to assist early screening in resource-constrained healthcare settings where trained cytologists and lab infrastructure are limited.

> Submitted to **EEML 2026** — Eastern European Machine Learning Summer School

---

##  How It Works

```
Cervical Image Input
        ↓
Preprocessing & Lesion Detection
        ↓
CNN Feature Extraction
        ↓
Real-Time Classification Output
```

The pipeline takes raw colposcopy or Pap smear images, preprocesses them into standardized patches, extracts features using a CNN, and outputs a classification with confidence scores in real time.

---

##  Results

| Metric | Value |
|---|---|
| Training Accuracy | 94.15% |
| Validation Accuracy | 94.14% |
| Train/Test Split | 80% / 20% |
| Training Images | 3,241 |
| Testing Images | 808 |
| Total Images | 4,049 |

> **No overfitting observed** — gap between train and validation accuracy is only 0.01%

---

##  Dataset

**SIPaKMeD** — a publicly available cervical cytology benchmark dataset containing 4,049 cell images across 5 classes:

| Class | Type |
|---|---|
| Superficial-Intermediate | Benign |
| Parabasal | Benign |
| Koilocytotic | Abnormal |
| Dyskeratotic | Abnormal |
| Metaplastic | Benign |

---

##  Methodology

1. **Data Acquisition** — SIPaKMeD dataset (image-level 80/20 split)
2. **Preprocessing** — Lesion detection, cropping, patch standardization, normalization
3. **Data Augmentation** — Rotation, flipping, brightness adjustments to improve generalization
4. **CNN Classification** — Multi-layer CNN with regularization and validation monitoring![Uploading Screenshot 2026-03-28 at 10.24.50 PM.png…]()

5. **Real-Time Prediction** — Integrated screening interface returning results in seconds

---

##  Getting Started

### Prerequisites
```bash
pip install tensorflow keras numpy opencv-python matplotlib scikit-learn
```

### Clone the Repository
```bash
git clone https://github.com/yourusername/cervical-cancer-detection.git
cd cervical-cancer-detection
```

### Download Dataset
Download SIPaKMeD from the [official source](https://www.cs.uoi.gr/~marina/sipakmed.html) and place it in the `/data` directory.

### Train the Model
```bash
python train.py --epochs 50 --batch_size 32
```

### Run Real-Time Prediction
```bash
python predict.py --image path/to/image.jpg
```

---

##  Project Structure

```
cervical-cancer-detection/
│
├── data/                   # SIPaKMeD dataset
├── models/                 # Saved model weights
├── notebooks/              # Jupyter notebooks for experiments
├── src/
│   ├── preprocess.py       # Image preprocessing pipeline
│   ├── model.py            # CNN architecture
│   ├── train.py            # Training script
│   └── predict.py          # Real-time prediction interface
├── results/                # Accuracy plots, confusion matrix
└── README.md
```

---

##  Future Work

- [ ] Patient-level train/test splitting to eliminate data leakage
- [ ] Multi-class classification for granular diagnostic output (LSIL, HSIL, ASC-US)
- [ ] Transfer learning with ResNet50 / EfficientNet
- [ ] Integration with telemedicine platforms for remote screening
- [ ] Clinical validation on real-world hospital data

---

##  References

1. Ronneberger, O., Fischer, P., and Brox, T. (2015). *U-Net: Convolutional Networks for Biomedical Image Segmentation*
2. Litjens, G. et al. (2017). *A Survey on Deep Learning in Medical Image Analysis*
3. WHO. *Comprehensive Cervical Cancer Control: A Guide to Essential Practice*
4. Zhang, L. et al. (2019). *Automated Cervical Cell Classification using Deep Learning*. IEEE Access
5. Plissiti, M.E. et al. (2018). *SIPaKMeD: A New Dataset for Feature and Image Based Classification of Normal and Pathological Cervical Cells*

---

##  Author

**Kavya Shree**
Computer Science Engineering — Pandit Deendayal Energy University (PDEU), India
📧 kavyax888@gmail.com

---

##  License

This project is for academic and research purposes only. Not intended for clinical use without proper medical validation.
