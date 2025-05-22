# Chromosome Classification using Deep Learning

## 📌 Overview

This project aims to **automate and enhance the karyotyping process** using deep learning by accurately detecting and classifying all 23 types of human chromosomes. The system also enables chromosome-level abnormality detection in future iterations. Our best model achieves **96.6% classification accuracy**, outperforming current state-of-the-art solutions (max 94%).

---

## 🔬 Motivation

Chromosomal abnormalities affect 1 in 150 newborns. Traditional karyotyping is time-consuming, requires expert supervision, and is prone to human error. Automating this using deep learning not only saves time but also increases diagnostic reliability.

---

## 🧠 Key Features

- **Object Detection**: Detectron2 and YOLOv4 for localizing chromosomes.
- **Super Resolution**: Laplacian Pyramid Super Resolution Network to upscale chromosome images from 20×20 to 120×120.
- **Classification Models**:
  - EfficientNet (B0, B5, B6)
  - ResNet
  - VGG-16
  - Custom CNN
- **Best Accuracy**: EfficientNet-B6 + Super Resolution yielded **96.6% accuracy**.
- **Data Annotation**: 62 base metaphase images were annotated using COCO Annotator, resulting in ~2480 individual chromosome strands for training and testing.

---

## 📁 Project Structure

<pre> chromosome-classification/ 
  ├── chromosome_resnet_1.ipynb # ResNet-based classification model 
  ├── Final Project.ipynb # Full pipeline with EfficientNet, super-resolution, and classification 
  ├── Project Report.docx # Detailed writeup and analysis 
  ├── dataset/ # Segmented and enhanced chromosome strands (not included here) 
  └── README.md # Project overview and instructions 
</pre>

## 🚀 Running the Project

### 1. Run the Jupyter Notebooks

- Open **`Final Project.ipynb`** for the full chromosome classification pipeline using EfficientNet and super-resolution.
- Open **`chromosome_resnet_1.ipynb`** to view or compare performance with a ResNet-based implementation.

---

## 🧪 Model Performance

| Model             | Super Resolution | Accuracy |
|------------------|------------------|----------|
| EfficientNet B6  | ✅               | **96.6%** |
| EfficientNet B5  | ✅               | 95.2%    |
| EfficientNet B0  | ✅               | 92.06%   |
| VGG-16           | ✅               | 94.0%    |
| Custom CNN       | ✅               | 88.0%    |
| EfficientNet B0  | ❌               | 88.75%   |

---

## 📊 Evaluation Metrics

| Metric     | Value   |
|------------|---------|
| Accuracy   | 96.6%   |
| Precision  | 97.01%  |
| Recall     | 96.10%  |
| F1-Score   | 96.41%  |

---

## 🧰 Tools & Technologies Used

- **Annotation**: COCO Annotator (Docker)
- **Object Detection**: Detectron2 (PyTorch), YOLOv4
- **Super Resolution**: Laplacian Pyramid Super-Resolution Network (LapSRN)
- **Training Platform**: Google Colab with GPU acceleration
- **Languages & Libraries**: 
  - Python
  - TensorFlow
  - PyTorch
  - Keras
  - OpenCV
  - NumPy
  - Matplotlib

---

## 🔮 Future Scope

- ✅ Integrate **abnormality detection** (e.g., Down Syndrome, Turner Syndrome, structural translocations).
- ✅ Deploy as a **clinical decision support system** for hospitals.
- ✅ Expand dataset and retrain models to improve generalization across diverse image sources.

---

## 📚 References

For detailed references and literature review, see Project Report.docx.

