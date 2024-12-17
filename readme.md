# Credit Card Default Prediction Project

## Results
Developed a machine learning model to predict next-month defaults for credit card users, achieving a prediction accuracy of **70.2%**. Model performance was optimized by tuning **LightGBM** hyperparameters (using random search) to reduce overfitting and improve training and prediction speed.

---

## Project Objective
Using the **UCI Credit Card Dataset**, the goal was to build a model that predicts the likelihood of credit card defaults in the following month by combining various features such as **credit limits, age, payment patterns, and billing amounts**. The project also aimed to identify key predictive factors.

---

## Problem-Solving Approach

### 1. Data Preprocessing and EDA
- Removed unnecessary data like **IDs**, which are unrelated to customers' credit status.
- Encoded categorical variables such as **gender** and **education level** using **OneHotEncoder** for analysis.
- Analyzed correlations among variables like **PAY**, **BILL**, and **PAY_AMT** to identify key factors affecting default likelihood.
- Confirmed that **PAY_0** (most recent delinquency status) has the most significant influence.

### 2. Modeling and Performance Evaluation
- Compared the performance of various models, including **Dummy Classifier, Logistic Regression, Random Forest, SVC**, and **LightGBM**.
- Selected **LightGBM** as the final model and optimized hyperparameters, such as **learning rate**, **n_estimators**, and **subsample**, using **random search**.
- Improved the model’s prediction accuracy to **70.2%**.

### 3. Feature Importance Analysis and Interpretation
- Used **SHAP** and **eli5** to analyze the importance of key features. Features such as:
  - **PAY_0** (most recent delinquency rate),
  - **LIMIT_BAL** (credit limit),
  - **PAY_AMT2** (second month’s repayment amount)
  were identified as the most influential predictors.
- Highlighted a strong correlation between **PAY** (delinquency information) and **BILL_AMT** (billing amount), emphasizing their critical role in predicting defaults.

---

## Key Achievements
- **Achieved 70.2% Accuracy**: The optimized **LightGBM** model outperformed other models, including **Dummy Classifier** and **Logistic Regression**.
- **Identified Key Features**: Data analysis confirmed that variables such as **LIMIT_BAL** (credit limit) and **PAY_0** (recent delinquency) play a significant role in predicting defaults, offering valuable insights for customer risk assessment.
- **Noise and Outlier Handling**: Proposed strategies to handle noise and outliers discovered during EDA, improving both data reliability and model performance.

---

## Strengths Demonstrated in the Project
- **Persistence and Dedication**: Repeatedly experimented with multiple models and adjusted hyperparameters to achieve the best results.
- **Problem Recognition and Customer Insight**: Identified anomalies in customer data and improved elements that negatively affected model performance.
- **Quantifiable Results and Evidence-Based Reporting**: Demonstrated project success with clear prediction accuracy and feature importance metrics, ensuring credibility and trust.

---

## Future Improvement Plans

### 1. Handling Data Noise
- Clean “unknown” values in **marital status** and **education** fields.
- Develop strategies to address incorrectly entered data, such as erroneous **age** values.

### 2. Feature Engineering
- Create a new feature by calculating the difference between **BILL_AMT** (billing amount) and **PAY_AMT** (repayment amount) to predict the **amount owed**. This could enhance prediction accuracy.

### 3. Model Improvement
- Compare and analyze additional machine learning models to further improve prediction performance for the **default** class.
