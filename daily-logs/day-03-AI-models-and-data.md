# 🤖 Day 3: AI Models & Data

**Platform:** [TryHackMe](https://tryhackme.com)  
**Path:** AI Security  
**Module:** AI Fundamentals  
**Room:** AI Models & Data  

---

## 📌 Room Overview
This room covers the core mechanics of how Artificial Intelligence and Machine Learning models process, clean, and utilize data to make predictions and generate content.

---

## 🔑 Key Concepts & Notes

### 1. The Role of Data in AI
- Data is the foundation of any Machine Learning model. The quality, diversity, and balance of the training data directly impact the performance and security of the model (*Garbage In, Garbage Out*).
- **Data Pipeline:** Data Collection ➡️ Data Preprocessing/Cleaning ➡️ Model Training ➡️ Evaluation ➡️ Deployment.

### 2. Types of Machine Learning
- **Supervised Learning:** The model is trained on labeled data (e.g., email marked as "spam" or "not spam").
- **Unsupervised Learning:** The model finds hidden patterns or groupings in unlabeled data (e.g., clustering customer behaviors).
- **Reinforcement Learning:** The model learns by trial and error using a system of rewards and penalties.

### 3. Training vs. Testing Data
- **Training Set:** The portion of dataset used to build and teach the model (typically ~70-80%).
- **Testing/Validation Set:** Unseen data used to evaluate how accurately the model generalizes to real-world scenarios.

### 4. Overfitting vs. Underfitting
- **Overfitting:** The model memorizes the training data too closely (including noise and errors) and fails on new, unseen data.
- **Underfitting:** The model is too simple to capture the underlying trend of the data.

### 5. Security Relevance (Data Risks)
- **Data Poisoning:** Adversaries inject malicious or manipulated data into the training pipeline to degrade model accuracy or introduce backdoors.
- **Data Privacy:** Sensitive information contained in training datasets can sometimes be extracted using prompt techniques or extraction attacks.

---

## 🎯 Progress Summary
- **Status:** Completed ✅
- **Key Takeaway:** AI model security relies heavily on ensuring the integrity, sanitization, and privacy of the underlying training data before and during model training.
