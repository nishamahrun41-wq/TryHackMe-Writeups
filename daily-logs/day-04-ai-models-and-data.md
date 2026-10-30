# 🤖 Day 4: AI Models & Data (TryHackMe)

*Platform:* [TryHackMe](https://tryhackme.com/room/aimodelsdata)  
*Topic:* AI Security, Model Architecture & Data Supply Chain  
*Difficulty:* Medium

---

## 💡 Room Conclusion & Core Recap

- **Key Takeaway 1:** AI training data is frequently drawn from poorly documented, unaudited web scraping sources (like Common Crawl), leading to serious data provenance and privacy risks.
- **Key Takeaway 2:** Fine-tuning a pre-trained base model inherits all beneath it; any unpatched vulnerabilities, backdoors, or biases in the base model carry over, and safety alignment degrades rapidly.
- **Key Takeaway 3:** Model weights are opaque "black boxes," making auditing difficult; post-training optimizations like quantisation can silently strip away built-in safety mechanisms.

---

## 📌 Task: Understanding Data Supply Chains & Model Risks

## 🧠 Core Concepts & Structure

AI security risks are shaped long before a model reaches production, rooted in data ingestion and architectural choices.

The AI Model lifecycle follows a structured path with inherent security risks:
1. **Data Sourcing & Cleaning:** Gathering data without proper provenance checks often bakes PII, copyrighted material, or credentials into model weights.
2. **Model Training & Validation:** Overfitting across too many epochs can lead to memorisation and secret leakage; lack of validation set checks hides upstream dataset poisoning.
3. **Optimisation & Fine-Tuning:** Applying post-training changes like quantisation or fine-tuning inherited base models introduces unmonitored behavior changes.

---

## 📊 Key Categories & Techniques

- **Data Provenance & Web Scraping:** Knowing where data originated, when it was collected, and whether it was tampered with. Datasets like Common Crawl often bake exposed credentials directly into model weights.
- **Overfitting & Memorisation:** When a model trains for too many epochs and memorises specific data points instead of generalising patterns, making it prone to reproducing sensitive training data when prompted.
- **Quantisation:** Post-training optimisation that reduces the numerical precision of weights (e.g., 32-bit floats to 8-bit) to cut compute costs, which can degrade safety alignment and break backdoor defences.
- **The Inheritance Problem:** Fine-tuning a base model carries over all original vulnerabilities, while safety mechanisms degrade with as few as 10 adversarial examples.
- **Black Box Problem & Model Cards:** Trained model weights are opaque, meaning security testing can only sample behavior rather than audit it. Model cards serve as the main transparency tool to document these risks.
