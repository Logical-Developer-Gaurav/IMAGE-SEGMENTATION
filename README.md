# 🐾 Pet Image Segmentation | U-Net + ResNet

A high-performance semantic segmentation pipeline implemented on the **Oxford-IIIT Pet Dataset**. This project leverages a **U-Net** architecture with a **ResNet** backbone to achieve precise pixel-level classification.

---

## 🎯 Project Objective
The goal is to perform 3-class segmentation on pet images:
1.  **Interior:** The body of the pet.
2.  **Boundary:** The outline/contour (critical for fine details like fur).
3.  **Background:** Everything else.

## 🏗️ Architecture
This implementation replaces the standard U-Net encoder with a **ResNet** feature extractor. 
* **Encoder:** ResNet (Residual Connections) helps in training deeper layers without gradient degradation.
* **Decoder:** Transpose convolutions and skip-connections from ResNet blocks to recover spatial information.
* **Input Size:** $128 \times 128$ (or $224 \times 224$) RGB images.

