# AGR-Net-Age-Gender-Race-Network-
# AGR-Net 🧠

**Multi-Task Learning for Age, Gender & Race Prediction**

This repository contains a deep learning project that performs **multi-task learning** to simultaneously predict **Age (regression)**, **Gender (binary classification)**, and **Race (multi-class classification)** using facial images from the UTKFace dataset.

---

## 📌 Key Features

* 🧑‍🧒 **Multi-task CNN** with a shared feature extractor and separate task-specific heads.
* 🧠 Uses a **custom-built deep neural network** instead of pre-trained models.
* 📊 Simultaneous training on three tasks using joint loss functions.
* 🎯 Metrics:

  * Age → Mean Absolute Error (MAE)
  * Gender → Accuracy
  * Race → Accuracy

---

## 📁 Project Structure

```
├── AGR_Net_(Age_Gender_Race_Network).ipynb  # Main training & evaluation notebook
├── data/                                    # UTKFace images (not included, must be added)
├── models/                                  # (Optional) Saved model checkpoints
├── results/                                 # Plots, confusion matrices, metrics
└── README.md
```

---

## 📊 Dataset

**[UTKFace Dataset](https://susanqq.github.io/UTKFace/)**
A large-scale face dataset with over 20,000+ images labeled for:

* **Age:** 0–116 years
* **Gender:** Male/Female
* **Race:** White, Black, Asian, Indian, Others

---

## 🚀 How to Run

### 1. Clone the repo

```bash
git clone https://github.com/your-username/agr-net.git
cd agr-net
```

### 2. Set up environment

```bash
pip install -r requirements.txt
```

### 3. Add Dataset

Place UTKFace images in the `data/` folder.

### 4. Launch notebook

Open `AGR_Net_(Age_Gender_Race_Network).ipynb` in Google Colab or Jupyter and run all cells.

---

## 🧠 Model Architecture

* **Input:** 128×128 facial image
* **Shared Layers:** Convolutional layers for feature extraction
* **Output Heads:**

  * **Age Head:** Regression (1 neuron, ReLU)
  * **Gender Head:** Binary Classification (2 neurons, Softmax)
  * **Race Head:** Multi-class Classification (5 neurons, Softmax)

---

## 📈 Results

| Task   | Metric   | Result (Example) |
| ------ | -------- | ---------------- |
| Age    | MAE      | \~6.8 years      |
| Gender | Accuracy | \~91%            |
| Race   | Accuracy | \~82%            |

(*Metrics vary by training conditions and seed*)

---

## 📷 Sample Outputs

* Confusion matrices for gender & race
* Age prediction vs actual plots
* Sample predictions with facial images (see `results/` folder)

---

## 📌 Future Improvements

* Switch to a **pretrained CNN** like VGG/ResNet for better feature extraction
* Use **transfer learning** and data augmentation
* Improve **race class balance** and **regularization**

---

## 📄 License

This project is for educational purposes. Please cite the UTKFace dataset and original sources if reused.

