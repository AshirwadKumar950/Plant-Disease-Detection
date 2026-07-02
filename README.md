# 🌿 Plant Disease Detection using Hybrid CNN–DS CBAM–Vision Transformer

## Overview

This project presents a novel hybrid deep learning architecture for automated plant disease detection. Instead of relying entirely on pretrained convolutional networks, the model combines a **self-designed Convolutional Neural Network (CNN)** with a **Depthwise Separable Convolution-based Convolutional Block Attention Module (DS-CBAM)** and a **Vision Transformer (ViT)** to effectively learn both local and global image features.
The proposed architecture is designed to improve disease classification accuracy while maintaining computational efficiency. The custom CNN extracts fine-grained local disease characteristics, the DS-CBAM module emphasizes informative feature regions through channel and spatial attention, and the Vision Transformer captures long-range contextual relationships across the image.


---- Architecture ----

**Input Image (224 × 224 × 3)**

⬇️

**Self-Designed CNN**

* Custom convolutional feature extractor
* Learns disease-specific local patterns such as lesions, discoloration, texture variations, and leaf damage
* Built entirely from scratch instead of using pretrained CNN architectures

⬇️

**Depthwise Separable CBAM (DS-CBAM)**

* Depthwise Separable Convolution for computational efficiency
* Channel Attention to identify the most informative feature maps
* Spatial Attention to focus on disease-affected regions while suppressing background noise

⬇️

**Vision Transformer (ViT)**

* Feature embedding into transformer patches
* Utilizes **only the last two Transformer Encoder layers**
* Learns global relationships between different regions of the leaf image

⬇️

**Classification Head**

* Fully Connected Layer
* Softmax Activation
* Final disease prediction

---

## Key Features

* Custom CNN developed from scratch
* Lightweight DS-CBAM attention mechanism
* Hybrid CNN + Transformer architecture
* Uses only the last two ViT encoder layers for efficient global feature learning
* Combines local feature extraction with global contextual understanding
* Improved attention towards disease-affected regions
* Efficient and scalable architecture suitable for real-world plant disease classification

---

## Technologies Used

* Python
* PyTorch
* NumPy
* OpenCV
* Matplotlib
* Google Colab

---

## Dataset

The model was trained and evaluated using the **PlantVillage** dataset containing multiple plant species and disease classes. Images were preprocessed, resized to **224 × 224**, normalized, and divided into training, validation, and testing sets before model training.

---

## Experimental Results

| Metric              |      Score |
| ------------------- | ---------: |
| Test Accuracy       | **XX.XX%** |
| Precision           | **XX.XX%** |
| Recall              | **XX.XX%** |
| F1-Score            | **XX.XX%** |
| Validation Accuracy | **XX.XX%** |

> Replace the above values with your actual experimental results.

---

## Project Highlights

* Designed an original hybrid deep learning architecture combining CNN, DS-CBAM, and Vision Transformer.
* Extracted robust local and global representations for accurate disease recognition.
* Reduced computational complexity through Depthwise Separable Convolutions.
* Improved feature representation using dual attention mechanisms.
* Achieved strong classification performance on plant disease images.

---

## Future Improvements

* Deployment as a web or mobile application.
* Real-time disease detection from live camera input.
* Support for additional crop species and diseases.
* Model optimization for edge devices using TensorRT or ONNX.

---

## Repository Structure

```text
Plant-Disease-Detection/
│── PlantDiseaseDetection.ipynb
│── README.md
│── requirements.txt
│── images/
│── results/
└── models/
```

## Author

**Ashirwad Kumar**

If you find this project useful, feel free to ⭐ the repository.
