
# Telecom Customer Churn Analysis & Prediction

<img src="https://github.com/Chaos-72/Telecom-customer-churn-analysis/blob/main/image.png" alt="Dashboard Image">

---

## Project Story

Customer churn is one of the biggest challenges for subscription-based businesses like telecom companies. Losing customers directly impacts revenue, and companies often struggle to understand **why customers leave and which customers are at risk of leaving next**.

In this project, I performed an **end-to-end customer churn analysis** to identify the factors influencing customer churn and built a **machine learning model to predict future churners**.

The goal was to combine **data analysis, business intelligence, and machine learning** to help telecom companies make **data-driven retention decisions**.

---

## My Approach

To solve this problem, I designed a workflow that covers the complete analytics pipeline:

1. **Prepare and clean raw telecom data using SQL**
2. **Analyze churn patterns and visualize insights using Power BI**
3. **Build a machine learning model in Python to predict churn**
4. **Create dashboards to identify high-risk customers**

This allowed me to transform raw customer data into **actionable business insights and predictive intelligence**.

---

## Data Preparation (SQL Server)

The first step was preparing the dataset for analysis.

I imported the raw telecom customer dataset into **SQL Server** and performed several cleaning and transformation steps to ensure the data was reliable for analysis.

Key actions included:

* Handling missing values and replacing NULL entries with meaningful values
* Standardizing categorical fields
* Converting the churn column from **Yes/No into a binary format (1/0)** for easier analysis
* Creating additional analytical columns such as **Age Group** and **Churn Status**

To make the analysis easier, I also created SQL views such as:

* **Churned Customers View**
* **New Joiners View**

These views helped simplify reporting and were directly used in the Power BI dashboards.

---

## Churn Analysis & Dashboard (Power BI)

After cleaning the dataset, I connected **Power BI directly to the SQL Server database** and built an interactive dashboard to analyze customer churn patterns.

The dashboard allows exploration of churn across multiple dimensions, including:

### Customer Demographics

* Gender distribution
* Age group analysis

### Account Characteristics

* Contract type
* Payment methods
* Customer tenure

### Geographic Patterns

* State-wise churn distribution

### Service Usage

* Internet service type
* Security services
* Additional telecom features

To monitor overall churn performance, I created several **DAX measures** such as:

* Total Customers
* Total Churn
* Churn Rate
* New Joiners

The dashboard also includes interactive filters and tooltips that allow users to drill down into specific churn segments.

---

## Key Insights from the Analysis

The analysis revealed several important patterns behind customer churn.

Some of the most notable insights include:

* Customers with **month-to-month contracts churn significantly more often** than customers with long-term contracts.
* **Fiber internet users show higher churn rates** compared to DSL users.
* Customers who do not subscribe to **security services** are more likely to leave.
* Certain geographic regions show **higher churn concentration**, indicating potential service or pricing issues.

These insights highlight areas where telecom companies can focus their **customer retention strategies**.

---

## Predicting Customer Churn (Machine Learning)

Beyond analyzing past churn behavior, I wanted to predict **which customers are most likely to churn in the future**.

Using **Python in Jupyter Notebook**, I built a machine learning model to perform churn prediction.

The workflow included:

* Data preprocessing using **Pandas**
* Encoding categorical variables
* Removing non-informative fields such as **CustomerID**
* Splitting the dataset into training and testing sets

I then trained a **Random Forest Classifier**, which works well with structured datasets and can capture complex relationships between features.

---

## Model Performance

The model was evaluated using a **confusion matrix and classification report**.

The Random Forest model achieved an accuracy of approximately **84%**, indicating strong performance in identifying customers who are likely to churn.

The trained model was then used to generate predictions for a new dataset.

The predicted churn results were exported into a **CSV file**, which was later integrated back into Power BI for visualization.

---

## Churn Prediction Dashboard

To make the predictions useful for decision-makers, I created an additional **Power BI dashboard focused on predicted churners**.

This dashboard highlights:

* Customers who are most likely to churn
* Potential revenue at risk
* Demographic characteristics of high-risk customers
* Service usage patterns among predicted churners

This enables businesses to quickly identify **high-risk customer segments**.

---

## Business Impact

This project demonstrates how combining **data analysis and machine learning** can help telecom companies move from reactive to proactive decision-making.

With this system, companies can:

* Identify customers at risk of leaving
* Run targeted retention campaigns
* Offer personalized incentives
* Reduce revenue loss caused by churn

Instead of reacting after customers leave, companies can **predict churn and act early**.

---

## Project Structure

```
Customer-Churn-Analysis
│
├── Data
│   ├── Customer_Data.csv
│   ├── cleaned_dataset.xlsx
│
├── SQL
│   ├── Create_and_distibur.sql
│   ├── churn_views.sql
│
├── powerbi
│   ├── churn_dashboard.pbix  
│
├── python
│   ├── churn_prediction_model.ipynb
│
├── predictions
│   ├── predicted_churn_customers.csv
│
└── README.md
```

---

## Tools & Technologies

* **SQL Server (SSMS)** – Data cleaning and transformation
* **Power BI** – Data visualization and dashboards
* **Python (Jupyter Notebook)** – Machine learning modeling
* **Pandas & Scikit-learn** – Data preprocessing and model training

---

## Future Improvements

Potential improvements to extend this project include:

* Deploying the model using **Streamlit or Flask**
* Automating the data pipeline with **ETL workflows**
* Testing additional machine learning models such as **XGBoost and Logistic Regression**
* Creating **real-time churn prediction dashboards**

---

## Conclusion

This project showcases a complete **data analytics and predictive modeling workflow**:

* Data preparation with SQL
* Insight generation with Power BI
* Predictive modeling with Python

By combining these tools, businesses can better understand customer behavior and take **proactive steps to improve customer retention**.
