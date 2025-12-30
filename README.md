# IoT DDoS Attack Detection Using Machine Learning

## 📌 Project Overview
Distributed Denial of Service (DDoS) attacks are one of the most serious threats to modern Internet of Things (IoT) environments. Due to limited computational power, memory, and security mechanisms, IoT devices are highly vulnerable to large-scale traffic flooding attacks.

This project presents a **machine learning–based DDoS detection system for IoT networks**, focusing on **behavioral traffic analysis** rather than identity-based features. A Random Forest classifier is used to accurately distinguish between normal IoT traffic and DDoS attack traffic.

---

## 🚨 What is a DDoS Attack?
A **Distributed Denial of Service (DDoS)** attack is a cyberattack in which multiple compromised devices (often IoT devices) simultaneously send a large volume of traffic to a target system, server, or network.

### Key Characteristics:
- Traffic flooding from multiple sources
- Exhaustion of network bandwidth or server resources
- Legitimate users are denied service
- Common in IoT botnets (e.g., Mirai-like attacks)

In IoT environments, even a small increase in malicious traffic can severely disrupt operations due to constrained device resources.

---

## 🌐 Why IoT is Chosen
- IoT devices are **resource-constrained**
- Security mechanisms are often minimal or absent
- Large-scale deployment increases attack surface
- IoT devices are frequently used as **botnet nodes**

Therefore, detecting DDoS attacks in IoT networks is both **critical and challenging**, making it a strong and relevant research problem.

---

## 🎯 Problem Statement
Traditional signature-based intrusion detection systems fail to detect evolving and high-volume DDoS attacks in IoT networks.

This project aims to:
- Detect DDoS attacks using **machine learning**
- Learn **traffic behavior patterns** instead of relying on IP addresses
- Achieve high accuracy with **low computational overhead**
- Ensure robustness through validation and feature analysis

---

## 🧠 Proposed Solution
We propose a **machine learning-based IoT DDoS detection framework** that:
1. Cleans and preprocesses IoT traffic data
2. Extracts behavior-based features (frequency, message count, payload size)
3. Trains a Random Forest classifier
4. Validates results using cross-validation and feature importance analysis

---

## 🗂 Dataset Information
The dataset used in this project consists of **IoT network traffic containing both normal and DDoS attack scenarios**.

### 📥 Dataset Source
Since the dataset is large, it is **not uploaded to this repository**.

You can download it from the official source:

🔗 **IoT DDoS Dataset (Official Repository / Research Dataset)**  
- https://data.mendeley.com/datasets/2bw34ght8b/1

📌 **Note:**  
After downloading, place the dataset file in the project root directory before running the code.

---

## 🧹 Data Preprocessing Steps
The following preprocessing steps were applied:

### 1. Data Cleaning
- Removed IP addresses and timestamps
- Dropped redundant textual description columns
- Removed identifier-based attributes to avoid data leakage

### 2. Feature Encoding
- Categorical features (e.g., protocol) were encoded using **One-Hot Encoding**

### 3. Feature Scaling
- Numerical features were scaled using **StandardScaler**
- Ensures faster convergence and stable learning

---

## 🤖 Machine Learning Model
### Random Forest Classifier
Random Forest was chosen due to:
- Ability to handle non-linear relationships
- Robustness to noise
- High performance with minimal tuning
- Built-in feature importance for interpretability

---

## 📊 Model Evaluation
The model was evaluated using:
- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

To ensure robustness:
- **Stratified Train-Test Split** was used
- **5-Fold Stratified Cross-Validation** was performed
- **F1-score** was used as the primary metric

---

## 🔍 Feature Importance Analysis
Feature importance analysis showed that:
- Traffic frequency
- Total message count
- Payload size
- Monitoring-based metrics

were the most influential features.

This confirms that the model learns **traffic behavior**, not identity-based information.

---

## ✅ Key Results
- Near-perfect detection accuracy
- Very low variance across cross-validation folds
- Stable performance after removing low-importance features
- No evidence of overfitting or data leakage

---

## 🏁 Conclusion
This project demonstrates that **machine learning-based behavioral analysis** can effectively detect DDoS attacks in IoT networks with high reliability.

The proposed approach is:
- Accurate
- Interpretable
- Computationally efficient
- Suitable for real-world IoT environments

---

## 🚀 Future Work
- Testing on real-time streaming IoT traffic
- Deployment as a lightweight IDS using Flask
- Extension to multi-class attack classification
- Integration with edge-computing environments

---


## 🛠 Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib / Seaborn

---

## 📜 License
This project is intended for **academic and research purposes only**.
