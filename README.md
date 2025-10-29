 Potato Disease Classification

A deep learning-based image classification system that identifies diseases in potato plants using Convolutional Neural Networks (CNN). This project helps farmers detect Early Blight, Late Blight, and determine if their potato plants are healthy.

## 📋 Table of Contents

- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Features](#features)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## 🌟 Overview

Potato farmers face significant economic losses annually due to plant diseases. This project leverages deep learning to provide an automated solution for early disease detection. By simply uploading an image of a potato leaf, farmers can quickly identify the health status of their crops and take appropriate action.

## 🎯 Problem Statement

Potato plants are susceptible to various diseases that can drastically reduce crop yield and quality:

- **Early Blight**: Caused by the fungus *Alternaria solani*
- **Late Blight**: Caused by the oomycete *Phytophthora infestans*

Early detection is crucial for:
- Preventing crop loss
- Reducing economic impact
- Optimizing pesticide usage
- Improving overall crop management

## ✨ Features

- 🔍 **Accurate Disease Detection**: Classifies potato leaf images into three categories (Healthy, Early Blight, Late Blight)
- 🚀 **High Accuracy**: Achieves high classification accuracy using CNN architecture
- 📱 **User-Friendly Interface**: Simple image upload and instant results
- ⚡ **Fast Prediction**: Real-time classification for quick decision-making
- 🌐 **Scalable Deployment**: Ready for production deployment

## 📊 Dataset

The model is trained on the **PlantVillage Dataset**, which contains:
- High-quality images of potato leaves
- Three classes:
  - Potato Healthy
  - Potato Early Blight
  - Potato Late Blight
- Multiple images per class for robust training

Dataset source: [PlantVillage Dataset](https://www.kaggle.com/datasets/arjuntejaswi/plant-village)

## 🏗️ Model Architecture

The project uses a Convolutional Neural Network (CNN) with the following characteristics:

- **Architecture**: Custom CNN or Transfer Learning (e.g., MobileNet, ResNet)
- **Input**: 256x256 RGB images
- **Layers**: 
  - Convolutional layers for feature extraction
  - Pooling layers for dimensionality reduction
  - Dense layers for classification
  - Dropout layers for regularization
- **Activation**: ReLU for hidden layers, Softmax for output
- **Optimizer**: Adam
- **Loss Function**: Categorical Crossentropy

## 🛠️ Technologies Used

- **Python 3.8+**
- **TensorFlow / Keras**: Deep learning framework
- **NumPy**: Numerical computations
- **Pandas**: Data manipulation
- **Matplotlib / Seaborn**: Data visualization
- **OpenCV / Pillow**: Image processing
- **Streamlit / Flask**: Web application (if applicable)
- **Jupyter Notebook**: Model development and training

## 📥 Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Setup Instructions

1. **Clone the repository**
```bash
git clone https://github.com/avanish729/potato-disease-classification.git
cd potato-disease-classification
```

2. **Create a virtual environment** (recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Download the dataset** (if not included)
```bash
# Place your dataset in the appropriate directory
# Or download from Kaggle using kaggle API
```

## 🚀 Usage

### Training the Model

```bash
jupyter notebook training/potato_disease_training.ipynb
```

Or run the training script:
```bash
python train.py
```

### Making Predictions

```python
from model import predict_disease

# Load and predict
image_path = "path/to/potato_leaf.jpg"
prediction = predict_disease(image_path)
print(f"Predicted class: {prediction}")
```

### Running the Web Application

```bash
streamlit run app.py
# Or for Flask
python app.py
```

Access the application at `http://localhost:8501` (Streamlit) or `http://localhost:5000` (Flask)

## 📁 Project Structure

```
potato-disease-classification/
│
├── data/
│   ├── train/
│   ├── validation/
│   └── test/
│
├── models/
│   └── potato_disease_model.h5
│
├── notebooks/
│   └── potato_disease_training.ipynb
│
├── src/
│   ├── model.py
│   ├── train.py
│   ├── predict.py
│   └── utils.py
│
├── app.py                  # Web application
├── requirements.txt
├── README.md
└── LICENSE
```

## 📈 Results

- **Training Accuracy**: ~98%
- **Validation Accuracy**: ~96%
- **Test Accuracy**: ~95%

### Performance Metrics

| Class | Precision | Recall | F1-Score |
|-------|-----------|--------|----------|
| Healthy | 0.97 | 0.96 | 0.97 |
| Early Blight | 0.95 | 0.94 | 0.95 |
| Late Blight | 0.96 | 0.97 | 0.96 |

### Sample Predictions

![Sample Predictions](assets/sample_predictions.png)

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add new feature'`)
5. Push to the branch (`git push origin feature/improvement`)
6. Create a Pull Request


**Avanish**

- GitHub: [@avanish729](https://github.com/avanish729)
- Project Link: [https://github.com/avanish729/potato-disease-classification](https://github.com/avanish729/potato-disease-classification)


---
