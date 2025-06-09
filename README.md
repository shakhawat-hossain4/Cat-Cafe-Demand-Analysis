## 🐾 Evaluating the Demand for a Cat Cafe in Dhaka

This machine learning project explores whether opening a cat cafe in Dhaka is a viable business idea. We surveyed 499 individuals and applied data analysis and classification models to determine interest and feasibility based on demographics and preferences.

---

### 📝 Project Overview

- **Course**: CSE 445.10 – Machine Learning
- **Team Members**: Shakhawat Hossain, Wahidun Akter, Ashfaqur Rahman Chowdhury, Rashedul Islam Tonu
- **Dataset**: 508 responses (499 after cleaning)

---

### 📊 Hypotheses and Validation

| Hypothesis | Statement | Result |
|-----------|-----------|--------|
| **H1** | Cat lovers will stay longer at the cafe. | ✅ Supported (Correlation: 0.4) |
| **H2** | Younger age groups are more encouraged. | ❌ Not supported (Weak correlation) |
| **H3** | Females are more likely to be cat lovers and stay longer. | ✅ Supported (Correlation: 0.2) |

---

### 📁 Dataset Highlights

- Features: Age, Gender, Occupation, Preferred Location, Cafe Duration, Love for Cats, Encouragement Factors, Allergy Issues
- Cleaned entries: 499
- Encoded with One Hot Encoding for analysis and model training

---

### 📊 Key Visual Insights (described from report)

#### 📈 Age Demographic
- **Most participants** are aged **20–29**, indicating a **young-biased dataset**.

#### 📊 Gender Demographics
- While males dominated in count, **females showed a stronger love for cats** and longer intended cafe stays.

#### 🔗 Correlation Matrix
- "Cat Lover: Strongly Agree" ↔ "Stay Duration: >2hrs" → **Strong positive correlation**
- Other insights:
  - Older individuals often cited **allergy** as a reason for disinterest.
  - **Location preference** varied by age: older (Banani/Gulshan), younger (Bashundhara R/A).

---

### ⚙️ Feature Engineering

- **Dimensionality Reduction**: Removed low-correlation features like `Age`, `Occupation`, `Encouragement`, and `Additional Features`
- **Target Label**: Derived binary interest label (`Interested` vs `Not Interested`) based on cafe stay duration and love for cats

---

### 🤖 Model Performance

| Model              | Accuracy | Notes |
|-------------------|----------|-------|
| Logistic Regression | 92%     | Strong performance with good precision and recall |
| KNN (K=5)           | 92%     | Nearly identical to Logistic Regression |
| Linear Regression   | ❌ Poor | R² = -0.43 (not suitable for classification) |

- 🧪 **Train/Test Split**: 80/20
- 🧪 **Unbiased Data Added**: Accuracy dropped slightly to 83% (highlighting original bias)

---

### 🧠 Final Model Discussion

- ✅ **True Positives (TP)**: 80 users correctly identified as interested
- ❌ **False Positives (FP)**: 10 users wrongly identified as interested
- ❌ **False Negatives (FN)**: 7 interested users incorrectly flagged as not interested

This shows **high model precision and strong positive predictions**, indicating **strong potential for the success of a cat cafe** in Dhaka.

---

### 📄 Full Report

📥 [**Download PDF Report**](https://github.com/shakhawat-hossain4/Bangla-STT-Transcriber/blob/main/CSE445_final%20report.pdf)

---

### 🛠 Tools Used

- **Python, Pandas, Matplotlib, Scikit-learn**
- **One Hot Encoding** for categorical variables
- **Correlation analysis** and **dimensionality reduction**

