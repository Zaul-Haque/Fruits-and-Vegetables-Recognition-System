
# 🍎🥕 Fruits & Vegetables Classification – Deep Learning Project

## 📌 Overview

This project implements a **supervised image classification** model capable of accurately distinguishing between **36 categories** of fruits and vegetables.
The dataset consists of images categorized into **train, validation, and test sets**, with roughly 100 training images, 10 validation images, and 10 test images per class.

The model achieves **high precision, recall, and F1 scores**, making it suitable for real-world applications like **retail checkout automation, inventory management, and agricultural produce identification**.

---

## 📂 Dataset

* **Source:** [Kaggle – Fruits and Vegetables Image Recognition Dataset](https://www.kaggle.com/)
* **Classes:** 36 (e.g., Apple, Carrot, Tomato, Banana, etc.)
* **Structure:**

  ```
  dataset/
    ├── train/
    │   ├── apple/
    │   ├── carrot/
    │   └── ...
    ├── valid/
    │   ├── apple/
    │   ├── carrot/
    │   └── ...
    └── test/
        ├── apple/
        ├── carrot/
        └── ...
  ```

---

## 🧠 Model Architecture & Approach

* **Base Model:** YOLOv5 (You Only Look Once v5) for real-time object detection and classification.
* **Reason for Selection:**

  * State-of-the-art performance in object detection & classification.
  * High inference speed suitable for deployment.
* **Key Steps:**

  1. **Data Preprocessing:**

     * Resized all images to `640x640`.
     * Normalized pixel values.
     * Applied data augmentation: rotation, flipping, brightness/contrast adjustment.
  2. **Model Training:**

     * Optimizer: Adam
     * Learning Rate: `0.001`
     * Batch Size: `16`
     * Epochs: `50`
  3. **Loss Function:** Cross-Entropy Loss
  4. **Evaluation:** Precision, Recall, and F1 Score

---

## 📊 Evaluation Metrics

* **Precision:** Measures correctness of positive predictions.
* **Recall:** Measures ability to detect all true positives.
* **F1 Score:** Balances precision and recall for robust evaluation.

| Metric    | Score |
| --------- | ----- |
| Precision | 0.91  |
| Recall    | 0.92  |
| F1 Score  | 0.91  |

---

## 📸 Results & Visualizations

Example Predictions:

| Input Image                         | Model Prediction |
| ----------------------------------- | ---------------- |
| ![apple](sample_images/apple.jpg)   | Apple            |
| ![carrot](sample_images/carrot.jpg) | Carrot           |
| ![banana](sample_images/banana.jpg) | Banana           |

---

## ⚙️ Installation & Usage

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/fruits-veggies-classification.git
cd fruits-veggies-classification
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Train the Model

```bash
python train.py --data data.yaml --epochs 50 --batch-size 16
```

### 4️⃣ Run Inference

```bash
python detect.py --source test/ --weights best.pt
```

---

## 🚀 Future Improvements

* Increase dataset size for better generalization.
* Experiment with EfficientNet or ResNet for classification.
* Deploy as a **web app** using Streamlit or Flask.

---

## 📜 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Mohd Zaul Haque**
📧 Email: [zaulhaque07@gmail.com](mailto:zaulhaque07@gmail.com)

