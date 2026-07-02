# Database Architecture

## Retail Banking Risk & Fraud Analytics Platform

---

# Overview

This project combines two real-world banking datasets to build a complete analytics platform capable of:

* Detecting fraudulent transactions
* Predicting loan default risk
* Performing customer risk analysis
* Supporting business decision-making through dashboards

The complete system follows an end-to-end data analytics pipeline.

---

# System Architecture

```
                Raw CSV Files
                       │
        ┌──────────────┴──────────────┐
        │                             │
 Home Credit Dataset          IEEE Fraud Dataset
        │                             │
        └──────────────┬──────────────┘
                       │
                Data Cleaning
                       │
                Feature Engineering
                       │
                 SQL Database
                       │
        ┌──────────────┼──────────────┐
        │              │              │
     Python EDA      ML Models     Power BI
        │              │              │
        └──────────────┼──────────────┘
                       │
                Business Insights
```

---

# Project Folder Structure

```
Retail-Banking-Risk-Fraud-Analytics/

│
├── data/
│   ├── home_credit/
│   └── ieee_fraud/
│
├── notebooks/
│
├── sql/
│
├── powerbi/
│
├── outputs/
│
├── screenshots/
│
├── docs/
│
├── README.md
│
└── requirements.txt
```

---

# Dataset Relationships

## Home Credit Dataset

application_train

↓

previous_application

↓

bureau

↓

bureau_balance

↓

installments_payments

↓

credit_card_balance

↓

POS_CASH_balance

---

## IEEE Fraud Dataset

train_transaction

↓

TransactionID

↓

train_identity

---

# Primary Keys

| Table                | Primary Key   |
| -------------------- | ------------- |
| application_train    | SK_ID_CURR    |
| bureau               | SK_ID_BUREAU  |
| previous_application | SK_ID_PREV    |
| train_transaction    | TransactionID |
| train_identity       | TransactionID |

---

# Relationship Keys

| Parent Table         | Child Table           | Key           |
| -------------------- | --------------------- | ------------- |
| application_train    | bureau                | SK_ID_CURR    |
| application_train    | previous_application  | SK_ID_CURR    |
| bureau               | bureau_balance        | SK_ID_BUREAU  |
| previous_application | installments_payments | SK_ID_PREV    |
| previous_application | credit_card_balance   | SK_ID_PREV    |
| previous_application | POS_CASH_balance      | SK_ID_PREV    |
| train_transaction    | train_identity        | TransactionID |

---

# Technology Stack

| Layer            | Technology                    |
| ---------------- | ----------------------------- |
| Programming      | Python                        |
| Data Processing  | Pandas, NumPy                 |
| Visualization    | Matplotlib, Seaborn, Power BI |
| Database         | SQL                           |
| Machine Learning | Scikit-learn                  |
| IDE              | VS Code                       |
| Notebook         | Jupyter                       |

---

# Data Flow

1. Import raw CSV files.
2. Perform data cleaning and preprocessing.
3. Engineer useful features.
4. Store processed data in SQL tables.
5. Build Machine Learning models.
6. Create Power BI dashboards.
7. Generate business insights.

---

# Future Architecture

* Real-time fraud prediction API
* Streamlit dashboard
* Flask backend
* Cloud deployment
* Automated ETL pipeline
