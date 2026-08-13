# CNN MNIST Digit Classification

## 📌 Project Overview

This project implements a **Convolutional Neural Network (CNN)** to classify handwritten digits from the **MNIST dataset**.

The MNIST dataset contains **60,000 training images and 10,000 test images**, with each image represented as a **28 × 28 grayscale image**.

The project uses **TensorFlow/Keras** to build and train the CNN model for multi-class digit classification.

---

## 🎯 Objective

The main objective of this project is to develop a Deep Learning model that can accurately recognize handwritten digits from **0 to 9**.

The project covers:

* Loading the MNIST dataset
* Exploring handwritten digit images
* Preparing image data
* Building a CNN architecture
* Training the neural network
* Using Early Stopping
* Evaluating model performance
* Predicting handwritten digits

---

## 📊 Dataset

The project uses the **MNIST handwritten digit dataset** available through TensorFlow/Keras.

### Dataset Split

| Dataset  | Number of Images | Image Size |
| -------- | ---------------: | ---------: |
| Training |           60,000 |    28 × 28 |
| Testing  |           10,000 |    28 × 28 |

The notebook loads the dataset directly using:

```python
from tensorflow.keras.datasets import mnist

(x_train, y_train), (x_test, y_test) = mnist.load_data()
```

### Classes

The model classifies images into **10 digit classes**:

```text
0 1 2 3 4 5 6 7 8 9
```

---

## 🛠️ Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook / Google Colab

---

## 🧠 CNN Architecture

The project implements a CNN using TensorFlow/Keras.

The architecture includes:

```text
Input Image (28 × 28 × 1)
        ↓
Conv2D (32 filters, 3 × 3)
        ↓
MaxPooling2D
        ↓
Conv2D (64 filters, 3 × 3)
        ↓
MaxPooling2D
        ↓
Flatten
        ↓
Dense (128 neurons)
        ↓
Dropout (0.5)
        ↓
Dense (10 neurons, Softmax)
```

The CNN defined in the notebook uses two convolutional layers with **32 and 64 filters**, max-pooling layers, a 128-neuron Dense layer, Dropout of 0.5, and a 10-neuron Softmax output layer.

---

## 🔍 CNN Components

### 1. Convolutional Layers

`Conv2D` layers extract important visual features from handwritten digit images.

```python
Conv2D(32, kernel_size=(3,3), activation='relu')
```

and:

```python
Conv2D(64, kernel_size=(3,3), activation='relu')
```

---

### 2. Max Pooling

`MaxPooling2D` reduces the spatial dimensions of feature maps while retaining important features.

```python
MaxPooling2D(pool_size=(2,2))
```

The notebook applies max pooling after both convolutional layers.

---

### 3. Flatten Layer

The `Flatten()` layer converts the extracted feature maps into a one-dimensional vector before passing them to the Dense layer.

---

### 4. Dense Layer

The model contains a Dense layer with **128 neurons** and ReLU activation.

```python
Dense(128, activation='relu')
```

---

### 5. Dropout

A Dropout rate of **0.5** is used to help reduce overfitting.

```python
Dropout(0.5)
```

---

### 6. Output Layer

The final layer contains **10 neurons** with Softmax activation, corresponding to the ten digit classes.

```python
Dense(10, activation='softmax')
```

---

## ⏹️ Early Stopping

The notebook uses the Keras `EarlyStopping` callback.

The configured callback monitors accuracy and uses:

* `patience=5`
* `restore_best_weights=True`

This helps stop training when the monitored metric no longer improves.

---

## 📈 Model Training

The notebook records training and validation metrics including:

* Training accuracy
* Training loss
* Validation accuracy
* Validation loss

During training, the model reaches approximately **92.7% validation accuracy by epoch 6** in the recorded output.

---

## 🔄 Project Workflow

```text
MNIST Dataset
      ↓
Load Training & Testing Data
      ↓
Explore Images
      ↓
Image Preprocessing
      ↓
Reshape Image Data
      ↓
Build CNN
      ↓
Compile Model
      ↓
Train Model
      ↓
Early Stopping
      ↓
Evaluate Model
      ↓
Digit Prediction
```

---

## 📊 Model Evaluation

The project evaluates the trained model using classification performance metrics.

The notebook also imports Scikit-learn's `classification_report` for classification evaluation.

Important evaluation metrics include:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

---

## 💡 Key Learning Outcomes

Through this project, I practiced:

* Deep Learning fundamentals
* Convolutional Neural Networks
* Image classification
* MNIST dataset handling
* Convolution operations
* Max pooling
* Flattening
* Dense neural networks
* Dropout regularization
* Softmax classification
* Early stopping
* Model training and evaluation
* TensorFlow/Keras

---

## 📁 Project Structure

```text
CNN-MNIST-Digit-Classification/
│
├── CNN_Minst_DL.ipynb
└── README.md
```

---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/CNN-MNIST-Digit-Classification.git
```

### 2. Install Required Libraries

```bash
pip install tensorflow numpy pandas matplotlib seaborn scikit-learn
```

### 3. Open the Notebook

Open:

```text
CNN_Minst_DL.ipynb
```

using **Jupyter Notebook** or **Google Colab**.

### 4. Run the Notebook

Run the cells sequentially to:

1. Load the MNIST dataset
2. Explore the images
3. Preprocess the data
4. Build the CNN
5. Train the model
6. Evaluate performance
7. Make digit predictions

---

## 📌 Conclusion

This project demonstrates how **Convolutional Neural Networks** can be used for handwritten digit recognition.

Using the MNIST dataset and a CNN architecture consisting of convolution, max-pooling, flattening, Dense, Dropout, and Softmax layers, the project provides practical experience with **Deep Learning and Computer Vision classification tasks**.

---

## 👨‍💻 Author

**Krish Makwana**

M.Sc. IT | Data Science / AI-ML Enthusiast

### Skills Demonstrated

`Python` `TensorFlow` `Keras` `CNN` `Deep Learning` `Computer Vision` `MNIST` `Image Classification` `NumPy` `Scikit-learn`
