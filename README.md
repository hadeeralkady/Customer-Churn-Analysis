# Customer Churn Analysis & Early Warning System

![Python](https://img.shields.io/badge/Python-3.8%2B-blueviolet)
![Pandas](https://img.shields.io/badge/Pandas-Data_Cleaning-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Predictive_Modeling-orange)
![License](https://img.shields.io/badge/Status-Complete-green)

## Project Overview
This project provides a comprehensive end-to-end analysis of customer churn. The goal is to identify why customers leave and build a machine learning model to predict potential churners. By combining **Exploratory Data Analysis (EDA)** with **Random Forest Modeling**, we transform raw data into strategic business recommendations.

---

## Key Business Insights

### 1. The Power of Financial History
Our analysis revealed that **Late Payments** are the single most significant predictor of churn. 
*   **Correlation:** 0.50 (Moderate-Strong)
*   **Observation:** Customers with a history of late payments are 5x more likely to discontinue service.

### 2. The "Red Flag" Zone
By crossing **Service Call frequency** with **Late Payments**, we identified a critical segment:
*   Customers with **3+ service calls** AND **2+ late payments** have a near-100% probability of churning.
*   *Insight:* Dissatisfaction combined with financial stress is the primary driver of attrition.

### 3. Tenure & Data Usage Paradox
Contrary to popular belief, churn in this dataset is **consistent across the lifecycle**. 
*   Long-term customers (high tenure) churn at nearly the same rate as new customers.
*   Data usage levels do not significantly distinguish churners from loyalists, suggesting that the "Value Proposition" is more important than "Usage Volume."

---

## Data Science Workflow

### Data Cleaning & Preprocessing
- Handled missing values in `monthly_data_gb` using **Median** (to avoid outlier bias).
- Encoded categorical variables (`contract_type`, `internet_service`) for modeling.
- Scaled numerical features using **StandardScaler**.

### Predictive Modeling
I utilized a **Random Forest Classifier** to capture non-linear relationships between features.
| Metric | Score |
| :--- | :--- |
| **Accuracy** | 85% |
| **Primary Driver** | Late Payments (31% Importance) |
| **Secondary Driver** | Monthly Charges (13% Importance) |

---

## Strategic Recommendations

### High Priority: Automated Alerts
Implement an **Early-Warning System** that triggers SMS/Email reminders 3 days before payment deadlines to mitigate the #1 churn driver (Late Payments).

### Proactive Support: The Loyalty Task-Force
Identify customers hitting the "Red Flag Zone" in real-time. Route these accounts to a specialized retention team for priority technical resolution and personalized offers.

### Contract Incentives
Since monthly contracts show higher volatility, launch a campaign to migrate "Monthly" users to "Annual" plans by offering a 10-15% loyalty discount.

### Lifecycle Rewards
Shift focus from just "Onboarding" to "Continuous Engagement." Introduce rewards for milestones (e.g., 24-month anniversary) to stabilize churn among veteran users.

---

## Visualizations

| Correlation Heatmap | Feature Importance |
| :---: | :---: |
| ![Heatmap](https://via.placeholder.com/400x300?text=Heatmap+Placeholder) | ![Importance](https://via.placeholder.com/400x300?text=Importance+Placeholder) |

---
