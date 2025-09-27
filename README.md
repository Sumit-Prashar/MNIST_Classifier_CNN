# MNIST Handwritten Digit Classification using CNN

## Project Overview
This project demonstrates building a **Convolutional Neural Network (CNN)** using **TensorFlow/Keras** to classify handwritten digits from the **MNIST dataset**.  
The goal is to create a simple yet effective deep learning model and document the workflow from data loading to model evaluation.

---

## Dataset
- **Name:** MNIST (Modified National Institute of Standards and Technology)  
- **Source:** Built-in TensorFlow dataset (`tf.keras.datasets.mnist`)  
- **Description:** 70,000 grayscale images of handwritten digits (0–9), each of size 28×28 pixels.  
  - 60,000 training images  
  - 10,000 test images  

---

## Preprocessing
- **Normalization:** Pixel values scaled from `[0, 255]` → `[0, 1]`  
- **Reshape:** Added channel dimension → `(28,28,1)` for CNN input  
- **Train/Validation Split:** 10% of training set used for validation  
- **Labels:** Kept as integers 0–9 for `sparse_categorical_crossentropy` loss  

---

## CNN Architecture
1. **Conv2D:** 32 filters, 3×3 kernel, ReLU activation  
2. **MaxPooling2D:** 2×2  
3. **Conv2D:** 64 filters, 3×3 kernel, ReLU activation  
4. **MaxPooling2D:** 2×2  
5. **Flatten + Dropout:** 50%  
6. **Dense:** 128 units, ReLU activation  
7. **Dense:** 10 units, Softmax activation (output layer)  

**Optimizer:** Adam  
**Loss Function:** Sparse Categorical Crossentropy  
**Metrics:** Accuracy  

---

## Training
- **Epochs:** 10  
- **Batch size:** 128  
- **Validation:** Monitored during training  

Training and validation accuracy/loss curves were plotted to evaluate the model’s learning process.

---

## Results
- **Final Test Accuracy:** ~[Insert your test accuracy here]  
- **Observations:**  
  - Model converges quickly due to simplicity of MNIST  
  - Minimal overfitting observed with Dropout  

---

## Next Steps
- Increase epochs or experiment with batch size  
- Add **data augmentation** to further reduce overfitting  
- Explore **deeper architectures** (more conv layers or filters)  
- Experiment with **different optimizers** or learning rates  

---

## How to Run
1. Clone the repository  
2. Open `MNIST_CNN.ipynb` in **Kaggle Notebook** or **Jupyter**  
3. Run all cells sequentially  
4. The model will train and generate plots for accuracy and loss  
