# Handwritten Digit Recognition using Convolutional Neural Network (CNN)

A deep learning project that classifies handwritten digits (0–9) from the MNIST dataset using a Convolutional Neural Network (CNN) built with TensorFlow/Keras.

---

## 👨‍💻 Author

**Deepanshu Gupta**

- 🎓 B.Tech Student, Malaviya National Institute of Technology (MNIT) Jaipur
- 💻 Interested in Artificial Intelligence, Machine Learning, Deep Learning, and Data Structures & Algorithms

---

## 📌 Project Overview

This project demonstrates the implementation of a Convolutional Neural Network (CNN) for handwritten digit classification.

Unlike Artificial Neural Networks (ANNs), CNNs automatically learn spatial features such as edges, curves, and shapes through convolution operations, making them highly effective for image classification tasks.

The model is trained on the MNIST dataset and achieves approximately **98–99% test accuracy**.

---

## 📂 Dataset

**MNIST Handwritten Digits Dataset**

- Training Images: **60,000**
- Testing Images: **10,000**
- Image Size: **28 × 28 pixels**
- Channels: **1 (Grayscale)**
- Number of Classes: **10 (Digits 0–9)**

---

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn

---

## 🧠 CNN Architecture

| Layer | Configuration | Output Shape |
|--------|--------------|--------------|
| Conv2D | 32 Filters, 3×3, ReLU | 26 × 26 × 32 |
| MaxPooling2D | 2×2 | 13 × 13 × 32 |
| Conv2D | 64 Filters, 3×3, ReLU | 11 × 11 × 64 |
| MaxPooling2D | 2×2 | 5 × 5 × 64 |
| Flatten | — | 1600 |
| Dense | 128 Neurons, ReLU | 128 |
| Dropout | 0.3 | 128 |
| Dense | 10 Neurons, Softmax | 10 |

---

## ⚙️ Data Preprocessing

- Loaded the MNIST dataset from TensorFlow.
- Reshaped images from:

```
(28,28)
```

to

```
(28,28,1)
```

to include the channel dimension.

- Normalized pixel values from **0–255** to **0–1** using:

```python
X_train = X_train / 255.0
X_test = X_test / 255.0
```

---

## 🚀 Model Compilation

```python
model.compile(
    optimizer='adam',
    loss='sparse_categorical_crossentropy',
    metrics=['accuracy']
)
```

---

## 🏋️ Training

The model was trained using:

- Optimizer: **Adam**
- Loss Function: **Sparse Categorical Crossentropy**
- Metric: **Accuracy**
- Validation Split: **20%**
- Early Stopping to prevent overfitting

```python
early_stopping = EarlyStopping(
    monitor='val_loss',
    patience=3,
    restore_best_weights=True
)
```

---

## 📊 Results

- Training Accuracy: **~99%**
- Test Accuracy: **~98–99%**

The model accurately classifies handwritten digits while maintaining good generalization on unseen test data.

---

## 🔍 Sample Prediction

```python
prediction = model.predict(X_test[0:1])
predicted_digit = prediction.argmax(axis=1)[0]
print(predicted_digit)
```

---

## 📈 Key Concepts Demonstrated

- Image Preprocessing
- Convolution Operation
- Feature Extraction
- Max Pooling
- Flatten Layer
- Dense Neural Networks
- Dropout Regularization
- Softmax Classification
- Early Stopping
- CNN Model Evaluation

---

## 📁 Project Structure

```
MNIST-CNN/
│
├── Handwritten_Digit_Recognition_CNN.ipynb
├── README.md
└── requirements.txt
```

---

## ▶️ How to Run

1. Clone the repository

```bash
git clone https://github.com/your-username/MNIST-CNN.git
```

2. Install the required libraries

```bash
pip install tensorflow numpy matplotlib scikit-learn
```

3. Open the notebook

```bash
jupyter notebook
```

or upload it to **Google Colab**.

---

## 🔮 Future Improvements

- Batch Normalization
- Data Augmentation
- Hyperparameter Tuning
- Learning Rate Scheduling
- Model Saving and Loading
- Testing on Custom Handwritten Images

---

## ⭐ If you found this project useful, consider giving it a star!

