# 🩺 Early Detection of Diabetic Retinopathy Through Deep Learning Using Fundus Photography

## 📌 Problem Statement

Diabetic Retinopathy (DR) is one of the leading causes of preventable blindness among diabetic patients worldwide. Early detection is critical to prevent severe vision loss. However, traditional diagnosis relies on manual examination of retinal fundus images by ophthalmologists, which is:

* Time-consuming
* Expensive
* Limited by the availability of specialists
* Difficult to scale for large populations

This project proposes an **automated deep learning-based system** that analyzes retinal fundus images and detects diabetic retinopathy at early stages using **Convolutional Neural Networks (CNNs)**. 

---

# 🧠 Project Overview

This project develops an **automated deep learning model** capable of detecting and classifying **Diabetic Retinopathy severity levels** from retinal fundus photographs.

The system performs:

1. Image preprocessing
2. Feature extraction using CNN
3. Multi-class classification of DR stages

The model identifies retinal abnormalities such as:

* Microaneurysms
* Hemorrhages
* Exudates

By automating detection, the system aims to support **early diagnosis, large-scale screening, and improved healthcare accessibility**, especially in rural or underserved regions. 

---

# 🎯 Objectives

The main objectives of the project are:

* Develop a **deep learning-based system** for early detection of Diabetic Retinopathy.
* Automatically **analyze retinal fundus images**.
* Identify early retinal abnormalities such as:

  * Microaneurysms
  * Hemorrhages
  * Exudates
* Classify images into **different DR severity stages**.
* Improve diagnostic efficiency and reduce dependency on manual screening.

---

# 📊 Dataset Information

The system is trained using **retinal fundus photographs** captured using fundus cameras.

### Dataset Characteristics

* Image Type: Retinal Fundus Images
* Format: RGB images
* Resolution: Varies depending on dataset
* Labels: DR severity levels

Typical classification categories:

```
0 — No DR
1 — Mild DR
2 — Moderate DR
3 — Severe DR
4 — Proliferative DR
```

Each image contains retinal structures such as:

* Blood vessels
* Optic disc
* Macula

These features are used by the CNN model to detect disease patterns.

---

# ⚙️ Methodology

The system follows a **deep learning pipeline** consisting of the following stages:

```
Input Image
     ↓
Preprocessing
     ↓
Feature Extraction
     ↓
CNN Model
     ↓
Classification Output
```

### Step-by-step Workflow

1. **Image Acquisition**

   * Fundus images collected from patients.

2. **Preprocessing**

   * Resize images
   * Noise removal
   * Contrast enhancement
   * Pixel normalization

3. **Feature Extraction**

   * CNN automatically extracts hierarchical features.

4. **Classification**

   * Fully connected layers classify the DR stage.

---

# 🧠 Model Architecture (CNN)

The core model used is a **Convolutional Neural Network (CNN)** designed for medical image classification.

Typical CNN layers include:

```
Input Layer
   ↓
Convolution Layer
   ↓
ReLU Activation
   ↓
Max Pooling
   ↓
Convolution Layer
   ↓
Pooling Layer
   ↓
Flatten Layer
   ↓
Fully Connected Layer
   ↓
Softmax Output Layer
```

### CNN Components

| Layer           | Function                        |
| --------------- | ------------------------------- |
| Convolution     | Extract image features          |
| ReLU            | Non-linear activation           |
| Pooling         | Reduce spatial dimensions       |
| Flatten         | Convert feature maps to vectors |
| Fully Connected | Perform classification          |

---

# 🧹 Data Preprocessing

Preprocessing improves the quality of retinal images before training.

Techniques used:

* Image resizing
* Noise reduction
* Normalization
* Contrast enhancement
* Pixel scaling

Benefits:

* Better feature visibility
* Reduced noise
* Improved model performance

---

# 🏋️ Training Process

The CNN model is trained using labeled fundus images.

### Training Steps

1. Load dataset
2. Apply preprocessing
3. Split dataset

   * Training set
   * Validation set
4. Train CNN model
5. Evaluate performance

### Training Configuration

Example:

```
Epochs: 20–50
Batch Size: 32
Optimizer: Adam
Loss Function: Categorical Crossentropy
```

---

# 📈 Results / Evaluation Metrics

Model performance is evaluated using standard classification metrics.

### Metrics Used

* **Accuracy**
* **Sensitivity (Recall)**
* **Specificity**
* **F1 Score**
* **Confusion Matrix**

These metrics help measure how effectively the system detects diabetic retinopathy.

---

# 📁 Project Folder Structure

Example repository structure:

```
diabetic-retinopathy-detection/
│
├── dataset/
│   ├── train/
│   ├── test/
│   └── validation/
│
├── preprocessing/
│   └── image_preprocessing.py
│
├── models/
│   └── cnn_model.py
│
├── training/
│   └── train_model.py
│
├── evaluation/
│   └── evaluate_model.py
│
├── notebooks/
│   └── training_experiments.ipynb
│
├── results/
│   ├── confusion_matrix.png
│   └── accuracy_plot.png
│
├── requirements.txt
└── README.md
```

---

# 💻 Installation Instructions

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/diabetic-retinopathy-detection.git
cd diabetic-retinopathy-detection
```

### 2️⃣ Create Virtual Environment

```bash
conda create -n dr-detection python=3.9
conda activate dr-detection
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

# ▶️ How to Run the Project

### Train the Model

```bash
python training/train_model.py
```

### Evaluate the Model

```bash
python evaluation/evaluate_model.py
```

### Predict on a New Image

```bash
python predict.py --image sample_fundus.jpg
```

---

# 🛠 Technologies Used

| Technology         | Purpose                   |
| ------------------ | ------------------------- |
| Python             | Core programming language |
| TensorFlow / Keras | Deep learning framework   |
| OpenCV             | Image preprocessing       |
| NumPy              | Numerical computations    |
| Matplotlib         | Visualization             |
| Anaconda           | Environment management    |

---

# 📊 Current Project Status

✔ Literature review completed
✔ System architecture designed
✔ Image preprocessing pipeline implemented
✔ CNN model architecture defined

🚧 Model training and optimization ongoing
🚧 Evaluation experiments in progress

The current implementation demonstrates the feasibility of **automated DR detection using deep learning**.

---

# 🚀 Future Improvements

Potential enhancements for this project:

* Use **transfer learning models**:

  * ResNet
  * EfficientNet
  * Vision Transformers
* Train on **larger datasets**
* Implement **attention mechanisms**
* Deploy as **web or mobile application**
* Integrate with **cloud-based healthcare platforms**
* Real-time screening using **IoT-enabled fundus cameras**

These improvements can significantly enhance detection accuracy and scalability. 

---

# 🙏 Acknowledgements

This project is inspired by research in **deep learning for medical image analysis**.

Key references include:

* LeCun, Bengio & Hinton – *Deep Learning*
* Krizhevsky et al. – *ImageNet Classification with Deep CNNs*
* Gulshan et al. – *Development and Validation of a Deep Learning Algorithm for DR Detection*
* Ting et al. – *Deep Learning System for DR Detection*

Special thanks to the research community working on **AI in healthcare and medical imaging**. 

---

## 👥 Team Members

This project was developed as part of an academic project by students from the **Department of Artificial Intelligence & Machine Learning**.

| Name | Student ID |
|-----|-----|
| **Syed Inzemam Hussain** | 160922729010 |
| **Farhaan Jameel** | 160922729024 |
| **Mohammed Faraaz** | 160922729052 |

**Department:** Artificial Intelligence & Machine Learning
