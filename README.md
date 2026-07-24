# Handwritten Digit Recognition using CNN (MNIST)

A Convolutional Neural Network (CNN) built using TensorFlow/Keras to classify handwritten digits from the MNIST dataset.

---
## 👨‍💻 Author

**Deepanshu Gupta**

- 🎓 B.Tech Student, Malaviya National Institute of Technology (MNIT) Jaipur
- 💻 Interested in Artificial Intelligence, Machine Learning, Deep Learning, and Data Structures & Algorithms


## Project Overview

This project demonstrates how a CNN can be used for image classification. The model is trained on the MNIST dataset, which contains grayscale images of handwritten digits (0–9).

The CNN automatically learns features such as edges, curves, and digit shapes using convolutional layers instead of manually engineering features.

---

## Dataset

- **Dataset:** MNIST
- **Training Images:** 60,000
- **Testing Images:** 10,000
- **Image Size:** 28 × 28 pixels
- **Channels:** 1 (Grayscale)
- **Classes:** 10 (Digits 0–9)

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib

---

## Model Architecture

| Layer | Output Shape |
|--------|--------------|
| Conv2D (32 filters, 3×3, ReLU) | 26 × 26 × 32 |
| MaxPooling2D (2×2) | 13 × 13 × 32 |
| Conv2D (64 filters, 3×3, ReLU) | 11 × 11 × 64 |
| MaxPooling2D (2×2) | 5 × 5 × 64 |
| Flatten | 1600 |
| Dense (128, ReLU) | 128 |
| Dropout (0.3) | 128 |
| Dense (10, Softmax) | 10 |

---

## Model Summary

- Total Parameters: **225,034**
- Trainable Parameters: **225,034**

---

## Data Preprocessing

- Reshape images from

```
(28,28)
```

to

```
(28,28,1)
```

to include the channel dimension.

- Normalize pixel values

```python
X_train = X_train.astype("float32") / 255.0
X_test = X_test.astype("float32") / 255.0
```

---

## Training

```python
model.compile(
    optimizer="adam",
    loss="sparse_categorical_crossentropy",
    metrics=["accuracy"]
)

history = model.fit(
    X_train,
    y_train,
    epochs=10,
    validation_split=0.2
)
```

---

## Prediction

Predict a single image:

```python
prediction = model.predict(X_test[0:1])
print(prediction.argmax(axis=1))
```

---

## Results

- Training Accuracy: ~99%
- Test Accuracy: ~99%

(The exact accuracy may vary slightly after each training run.)

---

## Project Structure

```
MNIST-CNN/
│
├── MNIST_CNN.ipynb
├── README.md
└── requirements.txt
```

---

## Key Concepts Learned

- Image preprocessing
- Convolutional Neural Networks
- Convolution layer
- Max Pooling
- Flatten layer
- Fully Connected (Dense) layers
- Dropout for regularization
- Softmax activation
- Multi-class classification
- Model evaluation and prediction

---

## Future Improvements

- Hyperparameter tuning
- Batch Normalization
- Data Augmentation
- Early Stopping
- Model Checkpointing
- Transfer Learning on larger datasets

---

## How to Run

1. Clone the repository

```bash
git clone https://github.com/your-username/MNIST-CNN.git
```

2. Install dependencies

```bash
pip install tensorflow numpy matplotlib
```

3. Run the notebook

```bash
jupyter notebook
```

or upload the notebook to **Google Colab**.

---

## Sample Output

```
Predicted Digit : 7
Actual Digit    : 7
```

---

