# Handwritten Digit Recognition using CNN | MNIST

A Convolutional Neural Network trained on the MNIST dataset to classify handwritten digits (0–9). Built using the Keras Functional API with Batch Normalization and Early Stopping.

## Dataset
- **MNIST** — 70,000 grayscale images at 28×28 pixels
- 60,000 training / 10,000 test images
- 10 classes (digits 0 through 9)

## Model Architecture

```
Input (28×28×1)
   → Conv2D(32) → BatchNorm → MaxPool
   → Conv2D(64) → BatchNorm → MaxPool
   → Conv2D(128) → BatchNorm
   → Flatten → Dense(256) → Dropout(0.4)
   → Softmax Output (10 classes)
```

## Results

| Metric        | Score  |
|---------------|--------|
| Test Accuracy | ~99%   |
| Optimizer     | Adam   |
| Loss Function | Sparse Categorical Crossentropy |

## Features
- Keras **Functional API** (more flexible than Sequential)
- **Batch Normalization** after each conv block for stable training
- **Early Stopping** — stops training when val_loss plateaus, restores best weights
- Confusion matrix heatmap for per-class error analysis

## How to Run

1. Clone the repo
```bash
git clone https://github.com/harisyar-ai/CodeAlpha_HandwrittenCharacterRecognition
cd CodeAlpha_HandwrittenCharacterRecognition
```

2. Install dependencies
```bash
pip install tensorflow scikit-learn seaborn numpy matplotlib
```

3. Open and run the notebook
```bash
jupyter notebook MNIST_CNN_Reworked.ipynb
```

## Tech Stack
- Python 3.10
- TensorFlow / Keras
- NumPy, Matplotlib, Seaborn, Scikit-learn

## Author
**Haider Haroon**
