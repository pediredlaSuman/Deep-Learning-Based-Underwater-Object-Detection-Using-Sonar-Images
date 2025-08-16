# 🌊 Adapted Deep Learning Models and Sensor Fusion for Robust Underwater Object Detection in Sonar Imaging

A deep learning-based project aimed at enhancing underwater object detection (humans, ships, planes) in noisy and low-visibility sonar images using YOLOv5, Faster R-CNN, CenterNet, and sensor fusion techniques.

---

## 📚 Table of Contents

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Problem Statement](#problem-statement)
4. [Approach](#approach)
5. [Model Architectures](#model-architectures)
6. [Training and Evaluation](#training-and-evaluation)
7. [Results](#results)
8. [Future Work](#future-work)
9. [Skills & Tech Used](#skills--tech-used)

---

## 🧠 Introduction

### 🎯 Objective:
To build a robust, noise-tolerant object detection system for underwater surveillance using sonar images by integrating and comparing multiple deep learning models.

### 🐠 Motivation:
Underwater environments are inherently challenging due to turbidity, noise, and occlusions. Reliable object detection is critical for defense, navigation, marine research, and search-and-rescue operations.

---

## 🗂 Dataset

- **Source**: Publicly available sonar image datasets & custom-labeled sonar images.
- **Objects**: Humans, Planes, Ships
- **Image Properties**: Grayscale sonar images with high noise levels
- **Preprocessing**: Resizing, denoising, histogram equalization, CLAHE, normalization

**Dataset Composition:**

![Dataset Composition](https://github.com/user-attachments/assets/f4ea4fae-027a-4008-9901-fb660a859ca2)

---

## 📌 Problem Statement

Enhance detection accuracy and robustness of underwater objects from sonar images by adapting state-of-the-art deep learning models and combining multiple sensor modalities.

---

## 🔍 Approach

1. **Model Comparison**: Evaluate and compare YOLOv5, Faster R-CNN, and CenterNet architectures on sonar data.
2. **Adaptation**: Modify CenterNet with weighted heatmap scaling and focal loss to improve detection of small/occluded objects.
3. **Sensor Fusion**: Integrate sonar and optical images using feature-level fusion to improve accuracy in high-turbidity conditions.
4. **Evaluation**: Use standard detection metrics such as mAP, IoU, precision, recall.

---

## 🏗 Model Architectures

- **YOLOv5**: Real-time object detection with anchor boxes and spatial pyramid pooling.
- **Faster R-CNN**: Region proposal-based detector, good for high-accuracy object localization.
- **CenterNet**: Keypoint-based object detection; modified with focal loss and adaptive heatmaps.
- **Fusion Module**: Combines sonar and optical features using weighted attention mechanism.

**Fusion-Based Detection:**

![Fusion-Based Detection](https://github.com/user-attachments/assets/43546747-68e2-4c53-9b87-6ea7c767eca7)

**YOLO Architecture:**

![YOLO Architecture](https://github.com/user-attachments/assets/89e77393-12f6-4a78-87ce-2d7578d3ab1f)

**Faster R-CNN Architecture:**

![Faster R-CNN](https://github.com/user-attachments/assets/d07825df-98e9-4678-a427-234ea51a88a3)

**CenterNet Architecture:**

![CenterNet](https://github.com/user-attachments/assets/009bf30d-896a-439c-8f06-1c4dbd9aa60f)

---

## 🧪 Training and Evaluation

- **Frameworks**: PyTorch, TensorFlow
- **Augmentation**: Rotation, Flipping, CLAHE, Gaussian noise injection
- **Loss Functions**:
  - YOLOv5: CIoU Loss, Objectness Loss
  - Faster R-CNN: Smooth L1 Loss, Classification Loss
  - CenterNet: Focal Loss + Heatmap Scaling
- **Metrics**:
  - Mean Average Precision (mAP)
  - IoU
  - Precision / Recall

---

## 📈 Results

- **YOLOv5**: Fastest, but missed small objects in noisy backgrounds
- **Faster R-CNN**: Higher localization accuracy but slower inference
- **CenterNet (Modified)**: Improved detection of occluded/small targets with ~6% mAP boost
- **Sensor Fusion (Sonar + Optical)**:
  - Achieved a 5% gain in accuracy under low-visibility scenarios
  - Enhanced object boundary detection in cluttered sonar images

**Performance Metrics:**

![Results Table](https://github.com/user-attachments/assets/394e870f-648d-4077-bda8-e1d533eca555)
![Results Accuracy](https://github.com/user-attachments/assets/9903d153-9f56-42ce-90d9-351c64610ee5)

**Ship Detection:**

![Ship Detection](https://github.com/user-attachments/assets/de0b8aad-590b-4d08-90e9-5212bc6cf7ba)

**Aircraft Detection:**

![Aircraft Detection](https://github.com/user-attachments/assets/ba6ed629-1fdf-47bb-8a46-c2e0f266a9ee)

---

## 🚀 Future Work

- Extend to multi-class marine object detection (corals, debris, etc.)
- Use 3D CNNs or Transformers for volumetric sonar scans
- Deploy the system on embedded underwater drones or real-time surveillance hardware

---

## 🧠 Skills & Tech Used

`Deep Learning` • `YOLOv5` • `Faster R-CNN` • `CenterNet` • `Sonar Imaging` • `Sensor Fusion` • `Object Detection` • `PyTorch` • `Computer Vision`
