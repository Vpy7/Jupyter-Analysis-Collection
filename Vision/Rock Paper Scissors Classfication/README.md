
## 📌 Introduction

This project aims to develop a deep learning model capable of recognizing hand gestures from the classic game Rock-Paper-Scissors, combining both classification and object detection tasks. Using TensorFlow and Keras, the model is trained to predict not only the gesture class but also the bounding box that localizes the hand in the image.

---

## 📊 Dataset Description

The **Rock-Paper-Scissors SXSW** dataset, a collection of **7,521 grayscale images** at a uniform resolution of 640×640 pixels. Each image contains a single hand performing one of three gestures: **rock**, **paper**, or **scissors**. It can be found here: https://www.kaggle.com/datasets/adilshamim8/rock-paper-scissors/data

- **Format**: TensorFlow Object Detection  
- **Labels**: Each sample includes a class label and bounding box coordinates  
- **Augmentations**: The dataset includes on-the-fly transformations (e.g., flips, brightness/contrast changes, and crops) to enhance model robustness to real-world variation

---

## 🎯 Objective

The goal is to train a multi-output model that:  
1. **Classifies** each image into one of the three gesture categories (`rock`, `paper`, or `scissors`)  
2. **Predicts** the bounding box that tightly encloses the hand performing the gesture  

This dual-task approach enables the development of more complete gesture recognition systems, capable of identifying both the *type* and the *location* of gestures within an image.


## Conclusions

###  What worked well
- One-hot encoding and bounding box extraction were cleanly handled.
- The data pipeline using TensorFlow Datasets was efficient and scalable.
- The use of custom augmentations likely helped with generalization.
- The model compiled and trained without issues and produced solid results.

###  What I plan to improve
- Try deeper or pretrained CNNs like MobileNet or EfficientNet for better performance.
- Add spatial data augmentation like flips or rotations.
- Improve bounding box accuracy using IoU-based loss functions.
- Visualize model predictions to better understand where it fails.
- Expand the dataset to improve the model’s robustness and generalization.

This setup gives me a solid baseline for tackling vision tasks that require both classification and object detection.
