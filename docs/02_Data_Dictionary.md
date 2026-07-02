# Data Dictionary

## Project
Retail Banking Risk & Fraud Analytics Platform

---

# Home Credit Default Risk Dataset

| Dataset | Description |
|----------|-------------|
| application_train | Customer loan application with target variable |
| application_test | Customer application without target |
| bureau | Previous loans from other institutions |
| bureau_balance | Monthly bureau balance history |
| previous_application | Previous loan applications |
| POS_CASH_balance | POS and cash loan monthly balance |
| installments_payments | Installment payment history |
| credit_card_balance | Monthly credit card balance |

---

# IEEE-CIS Fraud Detection Dataset

| Dataset | Description |
|----------|-------------|
| train_transaction | Transaction information |
| train_identity | Customer identity information |
| test_transaction | Test transactions |
| test_identity | Test identities |

---

# Important Features

## Transaction Features

| Feature | Description |
|----------|-------------|
| TransactionID | Unique transaction ID |
| TransactionDT | Time elapsed from first transaction |
| TransactionAmt | Transaction Amount |
| ProductCD | Product Category |
| card1-card6 | Card information |
| addr1 | Billing Region |
| addr2 | Billing Country |
| dist1 | Distance feature |
| dist2 | Secondary distance feature |

---

## Identity Features

| Feature | Description |
|----------|-------------|
| DeviceType | Desktop or Mobile |
| DeviceInfo | Device Name |
| id_01-id_38 | Identity related engineered features |

---

## Home Credit Features

| Feature | Description |
|----------|-------------|
| TARGET | Loan Default Target |
| AMT_CREDIT | Credit Amount |
| AMT_INCOME_TOTAL | Customer Income |
| DAYS_BIRTH | Customer Age |
| DAYS_EMPLOYED | Employment Duration |
| NAME_INCOME_TYPE | Income Type |
| OCCUPATION_TYPE | Occupation |
| ORGANIZATION_TYPE | Employer Type |

---

# Target Variables

| Dataset | Target |
|----------|--------|
| Home Credit | TARGET |
| IEEE Fraud | isFraud |

---

# Notes

- IEEE dataset focuses on transaction fraud detection.
- Home Credit dataset focuses on loan default prediction.
- Both datasets together provide customer behaviour, financial history and fraud related information for advanced analytics.