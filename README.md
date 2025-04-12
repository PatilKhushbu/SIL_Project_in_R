# SIL-Project-in-R
# Early Stage Heart Disease Detection

## Project Overview

This project focuses on early detection of heart disease using machine learning techniques. The goal is to analyze various health indicators and predict the likelihood of heart disease in patients. The project uses the UCI Heart Disease Dataset Comprehensive, which contains information on individuals referred to a cardiac clinic for testing between 1988 and 1991.

## Dataset

The dataset includes 12 variables (features) that describe different aspects of patients' health and medical history. The target variable is a binary classification indicating the presence or absence of heart disease.

### Variables:
1. **Age**: Patient's age in years
2. **Sex**: Patient's sex (1 = male; 0 = female)
3. **Chest pain type (cp)**: Type of chest pain experienced (1 = typical angina, 2 = atypical angina, 3 = non-anginal pain, 4 = asymptomatic)
4. **Resting blood pressure (trestbps)**: Patient's resting blood pressure (in mm Hg)
5. **Serum cholesterol (chol)**: Patient's serum cholesterol level (in mg/dL)
6. **Fasting blood sugar (fbs)**: Whether fasting blood sugar > 120 mg/dL (1 = true; 0 = false)
7. **Resting electrocardiographic results (restecg)**: Results of resting electrocardiogram (0 = normal, 1 = ST-T wave abnormality, 2 = left ventricular hypertrophy)
8. **Maximum heart rate achieved (thalach)**: Patient's maximum heart rate during exercise
9. **Exercise induced angina (exang)**: Whether angina occurred during exercise (1 = yes; 0 = no)
10. **ST depression induced by exercise (oldpeak)**: Amount of ST depression induced by exercise relative to rest
11. **Slope of peak exercise ST segment (slope)**: Slope of peak exercise ST segment (1 = upsloping, 2 = flat, 3 = downsloping)
12. **Target**: Presence or absence of heart disease (0 = absence, 1 = presence)

## Project Structure

- **Exploratory Data Analysis (EDA)**: Initial analysis to understand data distribution, correlations, and patterns.
- **Data Preprocessing**: Handling missing values, converting categorical variables, and splitting data into training and testing sets.
- **Model Building**: Implementation of various machine learning models including:
  - Logistic Regression (Base Model)
  - Logistic Lasso Regression (glmnet)
  - Logistic Ridge Regression
  - Linear Discriminant Analysis (LDA)
- **Model Evaluation**: Comparing models based on accuracy, AUC values, and other performance metrics.

## Results

- **Logistic Regression**: Achieved an accuracy of 86.76% with an AUC of 0.89.
- **LDA**: Achieved an AUC of 0.90, showing better discrimination ability compared to other models.

## How to Use This Repository

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/early-heart-disease-detection.git
   ```
2. **Install required packages**:
   ```R
   install.packages(c("tidyverse", "corrplot", "ggplot2", "dplyr", "glmnet", "mgcv", "caret", "car", "Metrics", "MASS", "pROC"))
   ```
3. **Run the R script**:
   - Open the R script in RStudio or any R environment.
   - Execute the script to reproduce the analysis.

## Dependencies

- R (>= 3.6.0)
- R Packages:
  - tidyverse
  - corrplot
  - ggplot2
  - dplyr
  - glmnet
  - mgcv
  - caret
  - car
  - Metrics
  - MASS
  - pROC

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Author

**Khushbu Mahendra Patil**  
GitHub: [yourusername](https://github.com/yourusername)  
Email: your.email@example.com

## Acknowledgments

- UCI Machine Learning Repository for the dataset.
- Contributors to the R packages used in this project.
