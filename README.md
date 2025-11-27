# Face Expression Analysis (using CNN)

A deep learning project that automatically recognizes human emotions from facial images. The model classifies an image into **7 emotion categories**:
**Angry, Disgust, Fear, Happy, Neutral, Sad, Surprise** (see page 3 of the report). :contentReference[oaicite:6]{index=6}

---

## 🚀 Introduction
Facial expressions play a major role in human communication and are widely used in applications such as HCI, surveillance, healthcare and AI systems (page 2). :contentReference[oaicite:7]{index=7}  
The goal of this project is to detect the emotion from a face image using a CNN-based neural network.

---

## 📌 Dataset: FER2013
We use the **FER2013** benchmark dataset containing **35k+ grayscale images of size 48×48** across 7 emotion categories (page 4). :contentReference[oaicite:8]{index=8}  
The dataset includes large variations in lighting, angle and face types.

---

## 🧠 Model Architecture
A custom CNN architecture was designed consisting of 3 convolutional blocks and fully connected layers (pages 5–6). :contentReference[oaicite:9]{index=9}  

### CNN Blocks:
- Conv2D → BatchNorm → Conv2D → BatchNorm → MaxPool → Dropout
- Filters: **64, 128, 256**

### Fully Connected:
- Dense(512)
- Dense(256)
- Output layer: Softmax (7 classes)

---

## ⚙️ Training Setup
- Optimizer: **SGD with momentum + Nesterov**
- LR scheduler: **ReduceLROnPlateau**
- Loss: Sparse Categorical Crossentropy
- Batch size: 32
- Epochs: Up to 200 (used EarlyStopping) (page 7). :contentReference[oaicite:10]{index=10}

---

## 📈 Results

### Final Test Accuracy
**67.55%** on the FER2013 test set (page 8). :contentReference[oaicite:11]{index=11}  

### Sample Visuals
Accuracy and loss curves available on pages 9–10. :contentReference[oaicite:12]{index=12}  
Confusion matrix & classification report on pages 11–12. :contentReference[oaicite:13]{index=13}  

---

### Classification Report Highlights
(F1-score by emotion) from page 12: :contentReference[oaicite:14]{index=14}

| Emotion | F1-score |
|--------|----------|
| Angry | 0.61 |
| Disgust | 0.61 |
| Fear | 0.51 |
| Happy | 0.88 |
| Neutral | 0.64 |
| Sad | 0.56 |
| Surprise | 0.78 |

The model performs best on **Happy and Surprise** emotions.

---

### Example Predictions
Screenshot demo results available on page 13. :contentReference[oaicite:15]{index=15}

