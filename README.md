# 💓 Early Stage Heart Disease Detection 🩺

![Heart Disease Prediction](https://img.shields.io/badge/Model-Logistic%20Regression%20%7C%20LDA-blue)  
![License](https://img.shields.io/badge/License-MIT-green)  
![R](https://img.shields.io/badge/Language-R-%2766CCFF)  

A machine learning project to predict heart disease risk using clinical data.  
**Goal**: Early detection of cardiovascular disease (CVD) to reduce global mortality rates (CVD causes ~31% of deaths worldwide 🌍).

---

## 📂 Dataset  
**Source**: [UCI Heart Disease Dataset](https://archive.ics.uci.edu/ml/datasets/Heart+Disease)  
**Samples**: 1,190 patients | **Features**: 12 clinical attributes  

### 🔍 Key Features  
| Variable               | Description                          |
|------------------------|--------------------------------------|
| `Age`                  | Patient age (years)                  |
| `Sex`                  | Gender (♂️ = 1, ♀️ = 0)            |
| `Chest pain type`      | 4 types (e.g., angina)               |
| `Resting BP`           | Blood pressure (mmHg)                |
| `Cholesterol`          | Serum cholesterol (mg/dL)            |
| `Max heart rate`       | Peak exercise heart rate (bpm) 💓    |
| **Target** (`0`/`1`)   | Heart disease **absent**/**present** |

---

## 🔬 Exploratory Analysis (EDA)  
📊 **Insights**:  
- 70% patients were male ♂️ | 30% female ♀️  
- 51% diagnosed with heart disease (⚠️ **alarming!**)  
- Strong correlation: `max.heart.rate` ↔ `target` (AUC = 0.90)  

![Correlation Heatmap](https://via.placeholder.com/400?text=Correlation+Heatmap) *(Example visualization)*  

---

## 🛠️ Model Performance  

| Model                  | Accuracy | AUC   | Notes                          |
|------------------------|----------|-------|--------------------------------|
| **Logistic Regression**| 86.76%   | 0.89  | Best AIC (692.21)              |
| **LDA**                | -        | 0.90  | 🏆 **Best discriminator**      |
| **Ridge Regression**   | -        | 0.89  | Lambda optimized              |

**Confusion Matrix** (Logistic Regression):  
```
          Predicted 0  Predicted 1  
Actual 0      87 (TN)      15 (FP)  
Actual 1      12 (FN)      90 (TP)  
```

---

## 🚀 How to Run  
1. **Clone repo**:  
   ```bash
   git clone https://github.com/yourusername/early-heart-disease-detection.git
   ```
2. **Install dependencies**:  
   ```r
   install.packages(c("tidyverse", "caret", "pROC", "glmnet", "MASS"))
   ```
3. **Execute R script**:  
   ```r
   source("heart_disease_prediction.R")
   ```

---

## 📌 Key Takeaways  
✅ **Top predictors**:  
- `Max heart rate` (↑ rate → ↑ risk)  
- `Chest pain type` (asymptomatic = high risk 🚨)  
- `Oldpeak` (ST depression)  

⚠️ **Limitations**:  
- Dataset from 1988–1991 (may need newer data)  
- Binary classification (no severity grading)  

---

## 📜 License  
MIT © [Khushbu Mahendra Patil](https://github.com/PatilKhushbu)  

---

## 🙏 Acknowledgments  
- [UCI ML Repository](https://archive.ics.uci.edu/) for the dataset  
- R community for open-source packages 📦  

---

**Let’s fight heart disease with data!** ❤️‍🩹
