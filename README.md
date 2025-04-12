# ❤️ Early Stage Heart Disease Detection 🏥

![Heart Disease Prediction](https://img.shields.io/badge/Model-Logistic%20Regression%20%7C%20LDA-blue)  
![License](https://img.shields.io/badge/License-MIT-green)  
![R](https://img.shields.io/badge/Language-R-%2766CCFF)  

A machine learning project to predict heart disease risk using clinical data from the Cleveland dataset.

---

## 📂 Dataset  
**Source**: [Heart Disease Cleveland Dataset on Kaggle](https://www.kaggle.com/datasets/ritwikb3/heart-disease-cleveland)  
**Samples**: 303 patients | **Features**: 14 clinical attributes  

### 🔍 Key Features
| Variable          | Description                          |
|-------------------|--------------------------------------|
| `age`            | Patient age in years                 |
| `sex`            | Gender (1 = male, 0 = female)        |
| `cp`             | Chest pain type (4 values)           |
| `trestbps`       | Resting blood pressure (mmHg)        |
| `chol`           | Serum cholesterol (mg/dL)            |
| `fbs`            | Fasting blood sugar > 120 mg/dL      |
| `restecg`        | Resting ECG results                  |
| `thalach`        | Maximum heart rate achieved          |
| `exang`          | Exercise induced angina              |
| `oldpeak`        | ST depression induced by exercise    |
| `slope`          | Slope of peak exercise ST segment    |
| `ca`             | Number of major vessels              |
| `thal`           | Thalassemia status                   |
| **Target**       | Heart disease diagnosis (0/1)        |

---

## 🔬 Key Findings
### 📊 Exploratory Analysis
- 54% of patients had heart disease (target=1) ⚠️
- Strongest predictors:
  - Maximum heart rate (thalach) 📈
  - Chest pain type (cp) 💔
  - ST depression (oldpeak) 📉
- Age distribution: 
  - Mean age = 54.4 years
  - Heart disease patients slightly younger (mean=52.4) than healthy patients (mean=56.6)

### 🧠 Model Performance
| Model                  | Accuracy | AUC   | Key Insight                     |
|------------------------|----------|-------|---------------------------------|
| **Logistic Regression**| 86.76%   | 0.89  | Best AIC (692.21)               |
| **LDA**                | -        | 0.90  | 🏆 Best discriminator           |
| **Ridge Regression**   | -        | 0.89  | Lambda optimized                |

**Confusion Matrix** (Logistic Regression):
```
          Predicted 0  Predicted 1  
Actual 0      87 (TN)      15 (FP)  
Actual 1      12 (FN)      90 (TP)  
```

---

## 🚀 How to Use
1. **Clone repo**:  
   ```bash
   git clone https://github.com/yourusername/heart-disease-prediction.git
   ```
2. **Install dependencies**:  
   ```r
   install.packages(c("tidyverse", "caret", "pROC", "glmnet", "MASS"))
   ```
3. **Run analysis**:  
   ```r
   source("heart_disease_analysis.R")
   ```

---

## 📌 Key Takeaways
✅ **Top risk factors**:
- Chest pain (especially asymptomatic)
- High ST depression (oldpeak)
- Lower maximum heart rate

⚠️ **Limitations**:
- Moderate sample size (n=303)
- Data from 1988 (may need newer data)

---

## 🙏 Acknowledgments  
- [Ritwik Bose](https://www.kaggle.com/ritwikb3) for the [Heart Disease Cleveland Dataset](https://www.kaggle.com/datasets/ritwikb3/heart-disease-cleveland)
- University Hospital Cleveland for original data collection
- Kaggle community for open data sharing
- R community for open-source packages 📦  

---

**Let's fight heart disease with data science!** ❤️🩺📊
