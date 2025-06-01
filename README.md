#  Personality Prediction Using Machine Learning

Predict whether a person is an introvert or extrovert based on behavioral traits using supervised machine learning.

---

##  Personality Prediction Project – Summary

###  Objective:
The goal of this project was to develop a machine learning model that can accurately predict whether a person is an **Introvert** or an **Extrovert** based on behavioral features such as time spent alone, social event attendance, online activity, and more.

---

###  Dataset Overview:
- **Total Records**: 2,900
- **Features**: 7 input features + 1 target label (`Personality`)
- **Feature Types**:
  - **Numeric**: `Time_spent_Alone`, `Social_event_attendance`, `Going_outside`, `Friends_circle_size`, `Post_frequency`
  - **Categorical**: `Stage_fear`, `Drained_after_socializing`
  - **Target**: `Personality` (`Introvert` = 0, `Extrovert` = 1)

---

###  Exploratory Data Analysis (EDA):
- Most numeric features were **right-skewed**
- **Boxplots** showed clear behavioral separation between introverts and extroverts
- **Correlation Matrix** revealed:
  - **Negative correlation** between `Time_spent_Alone` and all social traits
  - **Positive correlation** among `Post_frequency`, `Going_outside`, and `Social_event_attendance`

---

###  Data Preprocessing:
- Missing values handled using:
  - **Mean imputation** for numeric columns
  - **Mode imputation** for categorical columns
- Categorical variables encoded:
  - Yes/No → 1/0
  - Personality → 1/0

---

###  Models Trained:
- Random Forest
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Gradient Boosting
- XGBoost

---

###  Evaluation (Test Set):
All models achieved **accuracy > 91%**

| Model               | Accuracy |
|--------------------|----------|
| **SVM & Gradient Boosting** | **92.93%**  |
| KNN                | 92.59%   |
| Random Forest      | 92.24%   |
| XGBoost            | 91.72%   |

---

###  Cross-Validation (5-Fold):

| Model               | Mean Accuracy | Std Dev |
|--------------------|---------------|---------|
| **Gradient Boosting**  | **93.07%**       | 0.0167 |
| Logistic Regression | 92.90%        | 0.0193 |
| SVM (Linear)        | 92.86%        | 0.0189 |
| KNN                 | 92.59%        | 0.0166 |
| XGBoost             | 91.66%        | 0.0166 |

---

##  Conclusion:
Behavioral data can be used to predict personality type with high accuracy. Gradient Boosting emerged as the most accurate and stable model, making it suitable for further use or deployment.


##  Data Source & License

This project uses a dataset originally published on [Kaggle](https://www.kaggle.com/) by **Rakesh Kapilavayi**.  
The dataset is licensed under the [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/) license.

You are free to use, share, and adapt the dataset and this project, as long as:
- Proper credit is given to the original author.
- Any derivative works are shared under the same license (CC BY-SA 4.0).