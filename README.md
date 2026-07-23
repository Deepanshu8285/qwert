# Handwritten Digit Classification using Artificial Neural Networks (ANN)

A deep learning project that classifies handwritten digits (0–9) from the MNIST dataset using a Feedforward Artificial Neural Network (ANN) built with TensorFlow and Keras.

---

## 📌 Project Overview

This project demonstrates how to build, train, and evaluate an Artificial Neural Network (ANN) for image classification.

The model is trained on the MNIST handwritten digit dataset and is capable of predicting the digit present in unseen images.

---

## 🚀 Features

- Load the MNIST dataset
- Normalize image pixel values
- Build a Sequential ANN model
- Train using TensorFlow/Keras
- Validate model performance
- Visualize training & validation loss
- Visualize training & validation accuracy
- Predict handwritten digits from test images

---

## 🛠️ Tech Stack

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn

---

## 📂 Dataset

Dataset: **MNIST**

- 60,000 Training Images
- 10,000 Testing Images
- Image Size: 28 × 28 pixels
- Classes: 10 (Digits 0–9)

---

## 🧠 Model Architecture

Input

```
28 × 28 Grayscale Image
```

↓

Flatten Layer

```
784 Neurons
```

↓

Dense Layer

```
128 Neurons
Activation: ReLU
```

↓

Dense Layer

```
32 Neurons
Activation: ReLU
```

↓

Output Layer

```
10 Neurons
Activation: Softmax
```

---

## ⚙️ Model Configuration

Optimizer

```
Adam
```

Loss Function

```
Sparse Categorical Crossentropy
```

Metric

```
Accuracy
```

Epochs

```
25
```

Validation Split

```
20%
```

---

## 📈 Training

The model is trained using:

```python
model.fit(
    X_train,
    Y_train,
    epochs=25,
    validation_split=0.2
)
```

---

## 📊 Visualizations

The notebook includes:

- Training Loss
- Validation Loss
- Training Accuracy
- Validation Accuracy
- Sample Test Images
- Predicted Digits

---

## 📁 Project Structure

```
.
├── mnist_ann.ipynb
├── README.md
└── images/            (Optional)
```

---

## ▶️ How to Run

1. Clone the repository

```bash
git clone https://github.com/yourusername/your-repository.git
```

2. Install dependencies

```bash
pip install tensorflow matplotlib scikit-learn numpy
```

3. Open the notebook

```bash
jupyter notebook
```

or run it in **Google Colab**.

---

## 📚 Learning Outcomes

This project covers:

- Artificial Neural Networks (ANN)
- TensorFlow & Keras
- Sequential Models
- Dense Layers
- ReLU & Softmax Activation
- Forward Propagation
- Backpropagation
- Adam Optimizer
- Loss Functions
- Model Evaluation
- Data Normalization
- Image Classification

---

## 🔮 Future Improvements

- Convolutional Neural Network (CNN)
- Dropout Regularization
- Batch Normalization
- Confusion Matrix
- Precision, Recall & F1 Score
- Model Deployment using Streamlit or Flask

---

## 👨‍💻 Author

**Deepanshu Gupta**

GitHub: https://github.com/Deepanshu8285
