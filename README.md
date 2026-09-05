# 🛰️ Satellite Image Classification

<p align="center">
  <b>Deep Learning Project for Satellite Image Classification</b>
</p>

---

## 📌 Overview

This project implements an end-to-end **Deep Learning pipeline for satellite image classification** using a **Convolutional Neural Network (CNN)**.

The model learns visual patterns from satellite images and classifies them into four categories:

* ☁️ Cloudy
* 🏜️ Desert
* 🌊 Water
* 🌳 Green Area

The dataset contains **5,631 images**, divided into training and validation sets using an **80/20 split**.

The objective is to automatically classify unseen satellite images based on their visual features.

---

## ✨ Key Features

* 🛰️ Satellite image classification
* 🧠 Convolutional Neural Network
* 🖼️ Automatic image loading and resizing
* 🔄 Image preprocessing
* 📊 80/20 training-validation split
* 🎯 Multi-class image classification
* 📈 Model training and evaluation
* 🔍 Image prediction
* ⚡ TensorFlow/Keras implementation

---

## 🧠 Deep Learning Workflow

```text
                    ┌────────────────────┐
                    │  Satellite Images  │
                    │       data/        │
                    └──────────┬─────────┘
                               │
                               ▼
                    ┌────────────────────┐
                    │  Dataset Loading   │
                    │    5,631 Images    │
                    └──────────┬─────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │ Train / Validation Split│
                  │       80% / 20%         │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │   Image Preprocessing   │
                  │   Resize & Normalize    │
                  └────────────┬────────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │       CNN Model         │
                  │                         │
                  │ Conv2D → Pooling        │
                  │ Conv2D → Pooling        │
                  │ Conv2D → Pooling        │
                  │ Flatten → Dense         │
                  └────────────┬────────────┘
                               │
                               ▼
                    ┌────────────────────┐
                    │   Model Training   │
                    └──────────┬─────────┘
                               │
                               ▼
                    ┌────────────────────┐
                    │    Evaluation      │
                    └──────────┬─────────┘
                               │
                               ▼
                    ┌────────────────────┐
                    │    Prediction      │
                    └────────────────────┘
```

---

## 🛰️ Dataset

The images are loaded from the `data/` directory using TensorFlow's image dataset utilities. The notebook uses an image size of **72 × 128 pixels** and a batch size of **32**.

### Dataset Classes

| Class | Category      |
| ----: | ------------- |
|     0 | ☁️ Cloudy     |
|     1 | 🏜️ Desert    |
|     2 | 🌊 Water      |
|     3 | 🌳 Green Area |

These four class names are explicitly defined in the notebook.

### Dataset Statistics

| Property          | Value |
| ----------------- | ----: |
| Total Images      | 5,631 |
| Training Images   | 4,505 |
| Validation Images | 1,126 |
| Classes           |     4 |
| Validation Split  |   20% |
| Image Height      |    72 |
| Image Width       |   128 |
| Batch Size        |    32 |

---

## 🛠️ Technologies Used

| Technology    | Purpose                    |
| ------------- | -------------------------- |
| 🐍 Python     | Programming language       |
| 🧠 TensorFlow | Deep learning framework    |
| ⚙️ Keras      | Neural network development |
| 🔢 NumPy      | Numerical operations       |
| 📊 Pandas     | Data handling              |
| 📈 Matplotlib | Visualization              |
| 🛰️ CNN       | Image classification       |

---

## 📂 Project Structure

```text
Satellite-Image-Classification/
│
├── 📓 main.ipynb
├── 📁 data/
│   ├── ☁️ cloudy/
│   ├── 🏜️ desert/
│   ├── 🌊 water/
│   └── 🌳 green_area/
│
└── 📖 README.md
```

### File Description

**`main.ipynb`**

Contains the complete deep learning workflow, including dataset loading, preprocessing, CNN model creation, training, evaluation, visualization, and prediction.

**`data/`**

Contains the satellite images organized into four categories:

* `cloudy/`
* `desert/`
* `water/`
* `green_area/`

**`README.md`**

Contains the documentation and instructions for the project.

---

## ⚙️ Image Processing

The notebook loads the images and resizes them to:

```text
Height : 72 pixels
Width  : 128 pixels
```

The data is processed using batches of:

```text
Batch Size : 32
```

The training and validation datasets are created using an **80/20 validation split**.

---

## 🧠 CNN Model

The project uses a **Convolutional Neural Network (CNN)** for image classification.

```text
Input Image
     ↓
Conv2D
     ↓
MaxPooling2D
     ↓
Conv2D
     ↓
MaxPooling2D
     ↓
Conv2D
     ↓
MaxPooling2D
     ↓
Flatten
     ↓
Dense
     ↓
Classification Output
```

The CNN extracts visual features from satellite images and uses the learned features to determine the corresponding class.

---

## 🔀 Data Splitting

The dataset is divided into:

```text
80% → Training
20% → Validation
```

The notebook reports:

```text
Total Images      : 5,631
Training Images   : 4,505
Validation Images : 1,126
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/lokeshjakhar7781/Land-Cover-Classification-from-Satellite-Imagery.git
cd Land-Cover-Classification-from-Satellite-Imagery
```

### 2. Install Dependencies

```bash
pip install tensorflow numpy pandas matplotlib
```

### 3. Run the Project

Open:

```text
main.ipynb
```

Run the notebook cells sequentially to load the dataset, preprocess the images, train the CNN, evaluate the model, and generate predictions.


---

## 🔄 How the Project Works

### 1. Dataset Loading

Images are loaded from the `data/` directory and automatically assigned to their respective classes.

### 2. Image Preprocessing

Images are resized to **72 × 128 pixels** and prepared in batches of **32**.

### 3. CNN Training

The CNN learns important visual patterns from the satellite images through convolutional and pooling layers.

### 4. Model Evaluation

The model is evaluated using the validation dataset to determine how well it performs on unseen images.

### 5. Prediction

The trained model predicts the class of an image and maps the predicted class index to its category:

```text
0 → cloudy
1 → desert
2 → water
3 → green_area
```

---

## 📊 Prediction

For an input satellite image, the model generates a class prediction.

```text
Satellite Image
       ↓
     CNN Model
       ↓
Feature Extraction
       ↓
Class Prediction
       ↓
┌─────────────────┐
│ Cloudy          │
│ Desert          │
│ Water           │
│ Green Area      │
└─────────────────┘
```

The notebook also visualizes the image along with its **true label and predicted label**.

---

## 🎯 Project Goal

The goal of this project is to demonstrate how **Deep Learning and Convolutional Neural Networks can be applied to satellite imagery for automated image classification**.

```text
Satellite Images
       ↓
Dataset Loading
       ↓
Image Preprocessing
       ↓
CNN Feature Extraction
       ↓
Model Training
       ↓
Model Evaluation
       ↓
Satellite Image Classification
```

---

<p align="center">
  <b>🛰️ Turning Satellite Imagery into Intelligent Insights 🤖</b>
</p>
