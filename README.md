# Churn Prediction

## Objective
This project predicts customer churn using machine learning to help businesses identify at-risk customers and implement targeted retention strategies. The goal is to develop a model that enhances customer engagement and minimizes churn-related revenue loss.

## Dataset Overview
- **Records**: 7,043 customers  
- **Variables**: 33 total (24 categorical/mixed, 9 numeric)  
- **Target Variable**: `Churn Value` (1 = Churned, 0 = Retained)  
- **Class Distribution**:  
  - **Retained**: 5,174 (73.5%)  
  - **Churned**: 1,869 (26.5%)  

## Data Preprocessing
### Missing Data Handling
- No missing values except for `Churn Reason`, which was ignored in modeling.

### Feature Selection
- Removed redundant variables (e.g., Customer ID, location-based columns).
- Addressed collinearity in categorical features with target encoding.

### Encoding & Transformation
- One-hot encoding applied for categorical variables.
- Square root transformation applied to `Total Charges` to correct skewness.

### Class Imbalance Handling
- Used **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the dataset.

## Exploratory Data Analysis (EDA)
### Customer Tenure & Churn
- **Customers with shorter tenure (0-12 months) have the highest churn rates.**
- **Customers with longer tenure (over 60 months) are significantly more likely to stay.**
- **Recommendation**: Focus retention efforts early in a customer’s lifecycle.

### Monthly Charges & Churn
- Higher churn is observed among customers with **higher monthly charges**.
- Customers with lower charges tend to remain subscribed.
- **Recommendation**: Implement **tiered pricing models** or **loyalty discounts**.

### Contract Type & Churn
- **Month-to-month contracts** have the highest churn.
- **Two-year contracts** have the lowest churn.
- **Recommendation**: Encourage long-term contracts through **discounts & incentives**.

### Churn Reasons
- Many customers leave due to **competitor offers, pricing issues, and service dissatisfaction**.
- **Recommendation**: Improve service quality, offer competitive pricing, and create personalized retention strategies.

## Modeling & Evaluation
### Models Tested
- Logistic Regression  
- Random Forest  
- Neural Network  

### Performance Metrics
| Model               | AUC-ROC Score |
|---------------------|--------------|
| Logistic Regression | 0.9697       |
| Random Forest      | **0.9768**   |
| Neural Network     | 0.9649       |

- **Best Model**: *Random Forest* (highest AUC-ROC & balanced recall).

### Key Predictors of Churn
✔ **Churn Score** – Higher values indicate churn risk.  
✔ **Contract Type** – Month-to-month contracts have the highest churn.  
✔ **Tenure** – Shorter tenures correlate with higher churn rates.  
✔ **Monthly Charges** – Higher charges increase churn risk.  
✔ **Phone Service & Dependents** – Service-related and household factors play a role.  

## Business Implications & Recommendations
✔ **Early Customer Engagement** – Implement onboarding programs and proactive customer support.  
✔ **Long-Term Contract Incentives** – Offer discounts and benefits for multi-year contracts.  
✔ **Pricing Optimization** – Introduce tiered pricing plans to reduce churn risk.  
✔ **Service Enhancements** – Improve customer support and network reliability.  
✔ **Retention Offers** – Use predictive modeling to identify high-risk customers and provide tailored retention incentives.  

## Conclusion
This project demonstrates how **machine learning** can be leveraged to optimize customer retention by identifying key churn drivers. By implementing **strategic interventions**, businesses can significantly **reduce churn rates and improve customer loyalty**. 🚀  
