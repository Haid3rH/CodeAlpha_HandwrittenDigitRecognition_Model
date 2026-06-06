# 🧠 MNIST Digit Classifier — CNN from Scratch

> *Teach a machine to read handwriting. Turns out it gets better at it than most people.*

Built by **Haider Haroon**

---

## What is this?

A Convolutional Neural Network that looks at a tiny 28×28 image of a handwritten digit and tells you exactly what number it is — with ~99% accuracy. Trained on MNIST, one of the most classic datasets in ML.

No pretrained models. No shortcuts. Built and trained from scratch.

---

## How the model thinks

Every image goes through three rounds of feature extraction before a final decision is made:

```
Raw Pixels (28×28)
    ↓
[Conv → BatchNorm → MaxPool]   ← finds edges and basic shapes
    ↓
[Conv → BatchNorm → MaxPool]   ← starts recognizing curves and loops
    ↓
[Conv → BatchNorm]             ← puts it all together into digit-level patterns
    ↓
Flatten → Dense(256) → Dropout
    ↓
Softmax → one of 10 digits
```

Batch Normalization keeps training stable. Dropout (40%) stops the model from memorizing. Early Stopping makes sure we don't overtrain.

---

## Numbers

| What | How much |
|------|----------|
| Dataset | MNIST — 70,000 images |
| Training split | 60,000 images |
| Test split | 10,000 images |
| Test Accuracy | ~99% |
| Optimizer | Adam |
| Loss | Sparse Categorical Crossentropy |

---

## Run it yourself

```bash
# 1. grab the repo
git clone https://github.com/Haid3rH/MNIST-CNN
cd MNIST-CNN

# 2. install what you need
pip install tensorflow scikit-learn seaborn numpy matplotlib

# 3. fire it up
jupyter notebook MNIST_CNN_Reworked.ipynb
```

---

## Stack

`Python 3.10` · `TensorFlow/Keras` · `NumPy` · `Matplotlib` · `Seaborn` · `Scikit-learn`

---

*Haider Haroon · [LinkedIn](https://linkedin.com/in/haider-haroon-8a0209306/) · [GitHub](https://github.com/Haid3rH)*
