# 🛰️ CubeSat Image Classification Hackathon – Team 3

This repository contains the code and models developed during the Hack4Dev Regional Hackathon to solve the **CubeSat Image Quality Classification** challenge. Our goal was to classify satellite images into five categories based on visual quality:

- **Blurry**
- **Corrupt**
- **Missing_Data**
- **Noisy**
- **Priority**

We implemented and compared both **Machine Learning (XGBoost)** and **Deep Learning (CNN)** pipelines. The final submission was based on the XGBoost model due to its balance of high accuracy and resource efficiency.

---

## 🚀 Project Highlights

- 📊 **XGBoost Pipeline** – 89.2% Accuracy, ~4.7MB model size, fast training and inference.
- 🧠 **CNN Pipeline** – 99.8% Accuracy, but large model size and long training time.
- ⚙️ Efficient preprocessing tailored to each pipeline.
- 🧪 Evaluation using a dedicated script (`evaluate.py`) simulating deployment constraints.

---

## 🗂️ Repository Structure

├── ML_pipeline.ipynb # Notebook for preprocessing + XGBoost training and evaluation
├── CNN_pipeline.ipynb # Notebook for CNN training and evaluation 
├── evaluation.ipynb # Evaluation of both models using provided metrics framework 
├── models/ │ ├── ml_model.pkl # Trained XGBoost model (used for submission) │
├── cnn_model.pkl # Trained CNN model 
├── evaluate.py # Evaluation pipeline provided by the organizers 
├── README.md # Project documentation


> 📦 **Note**: Dataset files are not included in this repository due to size and licensing constraints.

---

## 🧪 Reproducing the Results

> Ensure you are using a Python 3.8+ environment with `tensorflow`, `xgboost`, `scikit-learn`, `numpy`, `matplotlib`, and `joblib` installed.

### 1. Prepare Your Data

Place the following `.npy` files into a `data/` folder:

- `train_images.npy`, `train_labels.npy`
- `val_images.npy`, `val_labels.npy`
- `test_images.npy`, `test_labels.npy`

Structure:
data/ 
├── train_images.npy 
├── train_labels.npy 
├── val_images.npy 
├── val_labels.npy 
├── test_images.npy 
├── test_labels.npy


### 2. Run the Pipelines

- For **XGBoost**, open and run `ML_pipeline.ipynb`
- For **CNN**, open and run `CNN_pipeline.ipynb`

Both notebooks include:
- Preprocessing
- Model definition
- Training and evaluation
- Saving the model

### 3. Evaluate the Model

Use `evaluation.ipynb` to simulate the official evaluation pipeline on the test set. It will report:
- Accuracy, F1 Score
- Confusion Matrix
- Evaluation Time
- Peak Memory and CPU usage
- Code Size (Model + Preprocessing)

---

## 📈 Results Summary

| Metric              | XGBoost        | CNN           |
|---------------------|----------------|---------------|
| Accuracy (Test)     | **89.2%**      | 99.8%         |
| F1 Score            | 88.9%          | 99.8%         |
| Training Time       | ~1.5 min       | ~14 min       |
| Model Size          | 4.7 MB         | 1.1 MB        |
| Evaluation Time     | ~37 sec        | ~698 sec      |
| Memory Usage (Peak) | 18.6 GB        | 57.1 GB       |

---

## 📌 Notes

- The XGBoost model was selected for submission due to its efficiency and strong accuracy.
- The CNN model, despite excellent accuracy, was computationally intensive and not ideal for the resource-constrained environment simulated in the challenge.

---

## ✍️ Authors

**Team 3 – Hack4Dev Regional Hackathon**  
Developed by: Christophe HOUNWANOU, Noella  
Organization: African Institute for Mathematical Sciences

---

## 📄 License

This project is shared for educational and non-commercial use.  




