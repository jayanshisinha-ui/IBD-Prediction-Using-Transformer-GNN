# 🧠 IBD Prediction Using Gut Microbiome and Hybrid Transformer–GNN Model

## 📌 Project Overview

This project presents a **Hybrid Transformer–Graph Neural Network (GNN)** model for predicting **Inflammatory Bowel Disease (IBD)** using gut microbiome data.

The model combines **Transformer-based feature learning** with **Graph Neural Networks** to capture microbial interaction patterns and improve disease prediction accuracy.

The system classifies:

- 🧬 **Crohn’s Disease**
- 🧫 **Ulcerative Colitis**

based on microbial abundance patterns.

---

## 📊 Dataset Information

- 📁 **Dataset:** Gut Microbiome Dataset  
- 📄 **File Name:** `microbiome.csv`  
- 🔢 **Samples:** 3387  
- 🧪 **Features:** 571 microbial species  

The dataset contains microbial abundance values associated with different IBD conditions.

---

## ⚙️ Methodology

The proposed workflow consists of the following steps:

### 🔹 1. Data Preprocessing

- Cleaning diagnosis labels  
- Handling missing values using **Mean Imputation**  
- Feature scaling using **StandardScaler**  
- Dimensionality reduction using **PCA (50 Components)**  

---

### 🔹 2. Train–Test Split

- 📊 **Training Data:** 70%  
- 🧪 **Testing Data:** 30%  
- ⚖️ Stratified sampling used to maintain class balance  

---

### 🔹 3. Transformer Encoder (Feature Learning)

The **Transformer Encoder** captures complex relationships between microbial features using:

- Multi-Head Attention  
- Feed Forward Network  
- Layer Normalization  

This improves feature representation before graph learning.

---

### 🔹 4. KNN Graph Construction

A **K-Nearest Neighbor (KNN)** graph is created to model microbial interactions.

- 🧩 **Nodes:** Microbial samples  
- 🔗 **Edges:** Microbial similarity  
- 🔢 **k-value:** 5 neighbors  

This models microbial interaction relationships.

---

### 🔹 5. Graph Neural Network (GCN)

A **Graph Convolutional Network (GCN)** learns microbial interaction patterns.

Architecture:

- GCN Layer 1 → ReLU Activation  
- GCN Layer 2 → Output Layer  

The GCN predicts disease classes using graph structure.

---

### 🔹 6. Model Evaluation

The model is evaluated using:

- 🎯 Accuracy  
- 📉 Confusion Matrix  
- 📈 ROC Curve  
- 📊 ROC–AUC Score  

---

### 🔹 7. SHAP Explainability

SHAP analysis helps:

- Identify important microbial features  
- Understand model decisions  
- Improve interpretability  

---

## 📈 Model Configuration Parameters

| Parameter | Value |
|----------|------|
| PCA Components | 50 |
| KNN Neighbors | 5 |
| Learning Rate | 0.005 |
| Epochs | 75 |
| Train–Test Split | 70%–30% |

---

## 📊 Results

The proposed hybrid model achieved strong classification performance:

- 🎯 **Accuracy:** 88.24%  
- 📈 **ROC–AUC Score:** 0.93  
- 🔍 **Precision:** 0.89  
- 🔁 **Recall:** 0.93  
- ⚖️ **F1-score:** 0.91  

These results demonstrate reliable prediction of Crohn’s Disease and Ulcerative Colitis.

---

## 📉 Generated Visual Outputs

The model produces the following visualizations:

- 📉 Training Loss Curve  
- 📊 Transformer Feature Visualization  
- 📊 Confusion Matrix  
- 📈 ROC Curve  
- 📌 SHAP Feature Importance Plot  

These visualizations help evaluate model learning and interpret results.

---

## 🧪 Technologies Used

- Python  
- NumPy  
- Pandas  
- PyTorch  
- PyTorch Geometric  
- Matplotlib  
- Seaborn  
- NetworkX  
- SHAP  
- Scikit-learn  

---


---

## 🎯 Applications

This project can be applied in:

- 🏥 Early disease prediction  
- 🧬 Microbiome-based diagnostics  
- 🧠 Personalized medicine  
- 📊 Clinical decision support systems  

---

## 🔬 Future Work

Potential improvements include:

- Integration of multi-omics datasets  
- Advanced graph construction techniques  
- Larger microbiome datasets  
- Real-time clinical implementation  

---

## 📜 License

This project is developed for **academic and research purposes only**.
