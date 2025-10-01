# License Plate Recognition System (TensorFlow + OpenCV)

This project implements a License Plate Recognition (LPR) system using TensorFlow and OpenCV. It detects and recognizes vehicle number plates from images using a combination of bounding box regression and OCR techniques.

## 🔍 Features

- Detects license plate location using CNN and InceptionResNetV2
- Extracts license text using Tesseract OCR
- Trained with Pascal VOC format annotations (XML)
- Evaluation using accuracy, precision, recall, and F1-score
- Visualization of predictions using Matplotlib

---

## 📂 Dataset

- Input: Images of vehicles with visible license plates
- Annotations: Pascal VOC format (XML)
- Each image has an associated XML file marking the bounding box of the license plate

---

## 🛠️ Tech Stack

- **Python 3**
- **TensorFlow / Keras**
- **OpenCV**
- **Tesseract OCR**
- **Matplotlib**
- **Scikit-learn**
- **NumPy**

---

## 🧠 Models Used

### 1. CNN Model (Sequential)
- Built from scratch using `Conv2D`, `MaxPooling2D`, and `Dense` layers.
- Used for bounding box regression to locate the license plate.

### 2. InceptionResNetV2
- Pre-trained InceptionResNetV2 used as the base model.
- Custom head added for bounding box prediction.
- Fine-tuned on custom dataset.

---

## 🧪 Evaluation

- Both models were trained and evaluated on the dataset.
- Metrics used: **Accuracy**, **Precision**, **Recall**, and **F1-score**
- Visualized prediction results and error analysis with Matplotlib charts.

---

## 📊 Results Comparison

| Metric       | Sequential CNN | InceptionResNetV2 |
|--------------|----------------|-------------------|
| Accuracy     | 85%            | 93%               |
| Precision    | 0.83           | 0.91              |
| Recall       | 0.84           | 0.92              |
| F1-Score     | 0.835          | 0.915             |

> InceptionResNetV2 showed superior performance in both detection accuracy and OCR clarity after cropping.

---

## 🖼️ Sample Output

1. Vehicle image → 2. Detected license plate (bounding box) → 3. Cropped → 4. OCR → 5. Extracted text

---

## 🚀 How to Run

### 1. Clone the repo
```bash
git clone https://github.com/yourusername/license-plate-recognition.git
cd license-plate-recognition
