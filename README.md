# Telecom Customer Churn Analysis & Prediction

<img src="https://github.com/Chaos-72/Telecom-customer-churn-analysis/blob/main/image.png" alt="Dashboard Image">


## Project Overview

Customer churn is one of the most critical challenges for subscription-based businesses such as telecom companies. Understanding **why customers leave** and identifying **who is likely to leave in the future** helps companies design better retention strategies.

This project performs an **end-to-end customer churn analysis** using:

* **SQL Server** for data extraction, transformation, and cleaning
* **Power BI** for data visualization and dashboard creation
* **Python (Jupyter Notebook)** for machine learning churn prediction

The goal of the project is to:

* Analyze historical customer data to identify **key churn drivers**
* Build **interactive dashboards** to explore churn patterns
* Train a **machine learning model** to predict future churners
* Help businesses take **data-driven retention actions**

---

# Tech Stack

| Tool                          | Purpose                                           |
| ----------------------------- | ------------------------------------------------- |
| **SQL Server (SSMS)**         | Data cleaning, transformation, and creating views |
| **Power BI**                  | Data visualization and dashboard creation         |
| **Python (Jupyter Notebook)** | Machine learning modeling and prediction          |
| **Pandas & Scikit-learn**     | Data preprocessing and model training             |
| **Excel / CSV**               | Data export and exchange between tools            |

---

# Project Workflow

## 1. Data ETL & Cleaning (SQL Server)

The project begins with importing raw telecom customer data into **SQL Server**.

Key steps performed:

* Created a **new database** to store the telecom dataset
* Imported raw customer data into SQL tables
* Cleaned missing values
* Standardized categorical values
* Created calculated columns

### Data Cleaning Tasks

* Replaced **NULL values** with appropriate values such as:

  * `None`
  * `Other`
* Converted churn column:

  * `Yes → 1`
  * `No → 0`
* Created new analytical columns:

  * **Churn Status**
  * **Age Group**

### SQL Views Created

Two views were created to simplify analysis:

* **Churned Customers View**
* **New Joiners View**

These views were later used directly in **Power BI dashboards**.

---

# 2. Data Visualization (Power BI)

Power BI was connected directly to the **SQL Server database** to import the cleaned data and views.

## KPI Metrics (DAX)

Several measures were created using **DAX**:

* Total Customers
* Total Churn
* Churn Rate
* New Joiners

These KPIs help monitor customer retention performance.

---

## Dashboard Analysis

The Power BI dashboard analyzes churn across multiple dimensions:

### Demographic Analysis

* Gender
* Age Groups

### Account Analysis

* Contract Type
* Payment Method
* Tenure

### Geographic Analysis

* State wise churn distribution

### Service Usage Analysis

* Internet type
* Security services
* Additional telecom services

### Interactivity Features

The dashboard includes:

* **Dropdown filters** for dynamic exploration
* **Tooltips** showing churn reasons
* Interactive visuals for drill-down analysis

---

# 3. Machine Learning Prediction (Python)

A **machine learning model** was developed to predict which customers are likely to churn.

## Data Preparation

Steps performed in Jupyter Notebook:

* Imported cleaned dataset
* Removed non-relevant columns such as:

  * `CustomerID`
* Converted categorical variables to numerical format using encoding
* Split the data into **training and testing datasets**

---

## Model Training

A **Random Forest Classifier** was used to train the churn prediction model.

Why Random Forest?

* Handles complex feature interactions
* Works well with tabular datasets
* Reduces overfitting compared to single decision trees

---

## Model Evaluation

Model performance was evaluated using:

* **Confusion Matrix**
* **Classification Report**

### Model Accuracy

**~84% accuracy**

This indicates the model performs well in predicting potential churners.

---

## Prediction Output

The trained model was then used to:

* Predict churn probability on a new dataset
* Export predictions to a **CSV file**

This file was later used inside **Power BI** for visualization.

---

# 4. Predicted Churn Dashboard (Power BI)

The predicted dataset was imported into Power BI to create a **Churn Prediction Profile Page**.

This page helps identify **high-risk customers**.

### Insights Provided

* List of predicted churners
* Revenue impact from potential churn
* Customer demographic profile
* Customer service usage patterns

### Business Value

This enables companies to:

* Run **targeted retention campaigns**
* Offer **personalized incentives**
* Reduce revenue loss from churn

---

# Project Structure

```
Customer-Churn-Analysis
│
├── Data
│   ├── Customer_Data.csv
│   ├── cleaned_dataset.xlsx
│
├── SQL
│   ├── Create_and_distibur .sql
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

# Key Insights from Analysis

Some typical churn insights discovered:

* Customers with **month-to-month contracts** churn more frequently
* **Fiber internet users** show higher churn compared to DSL
* Customers without **security services** have higher churn probability
* Certain **states/regions** show significantly higher churn rates

These insights can guide **customer retention strategies**.

---

# Future Improvements

Possible enhancements to the project:

* Deploy model using **Streamlit or Flask**
* Automate pipeline with **ETL workflows**
* Implement additional ML models:

  * XGBoost
  * Logistic Regression
* Add **real-time churn prediction dashboards**

---

# How to Run the Project

### 1️⃣ SQL Server

* Import the dataset into SQL Server
* Run the SQL cleaning scripts
* Create views

### 2️⃣ Power BI

* Connect Power BI to SQL Server
* Load cleaned tables and views
* Open the `.pbix` dashboard file

### 3️⃣ Python

* Open the Jupyter Notebook
* Install required libraries:

```bash
pip install pandas scikit-learn matplotlib seaborn
```

* Run the notebook to train the model and generate predictions.

---

# Conclusion

This project demonstrates a **complete data analytics workflow**:

* Data Cleaning (SQL)
* Business Intelligence (Power BI)
* Predictive Analytics (Machine Learning)

It shows how businesses can combine **data analysis and machine learning** to proactively reduce customer churn and improve customer retention.

---

