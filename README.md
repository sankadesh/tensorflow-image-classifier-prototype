# TensorFlow Cats vs Dogs Image Classifier (Colab Prototype)

A TensorFlow/Keras image classification prototype built in Google Colab using the **Kaggle Dogs vs Cats** dataset.  
This notebook covers a complete workflow: **dataset download via Kaggle API → preprocessing & normalization → data augmentation → CNN training → evaluation metrics → prediction pipeline**, and a clear path to **improve accuracy with Transfer Learning**.

## What’s Inside
- ✅ Kaggle dataset download (Cats vs Dogs) using Kaggle API
- ✅ Train/validation split
- ✅ Image resizing + **normalization**
- ✅ **Data augmentation** (flip/rotate/zoom, etc.)
- ✅ Custom **CNN model** built with TensorFlow/Keras
- ✅ Evaluation metrics:
  - Accuracy
  - Precision
  - Recall
- ✅ Prediction pipeline:
  - Predict a single image
  - Predict a batch/folder of images
  - Display predicted class + confidence
- ✅ Next improvement step: **Transfer Learning**

## Dataset
This project uses the Kaggle dataset:

**Dogs vs Cats** (Kaggle)  
Dataset is downloaded inside Colab via Kaggle API and is **not included** in this repository.

## Repository Structure
tensorflow-image-classifier-prototype/
└── notebooks/
└── prototype.ipynb

## How to Run (Colab)
1. Open the notebook from GitHub in Google Colab.
2. In Kaggle: Account → API → **Create New API Token** → download `kaggle.json`
3. Upload `kaggle.json` into Colab (Files panel → Upload)
4. Run the notebook cells in order:
   - Kaggle API setup
   - Download + unzip dataset
   - Preprocess / normalize
   - Data augmentation
   - Train CNN
   - Evaluate metrics
   - Run prediction pipeline

> ⚠️ Do not commit `kaggle.json` to GitHub. It is private.

## Further Accuracy Improvements (Transfer Learning)
To boost accuracy beyond a basic CNN:
- Use a pretrained backbone (recommended):
  - **MobileNetV2** (fast, good baseline)
  - **EfficientNetB0/B1** (strong accuracy)
  - **ResNet50** (classic, heavier)
- Strategy:
  1) Train classifier head with frozen base  
  2) Fine-tune top layers with a low learning rate  
  3) Add callbacks:
     - EarlyStopping
     - ReduceLROnPlateau
     - ModelCheckpoint
  4) Consider class balancing (if needed) and stronger augmentation

## Notes
- This repository is notebook-focused (prototype).
- No `requirements.txt` is included because the workflow is intended to run directly on Google Colab with standard installs.

## License
MIT License (optional — add one if needed).
