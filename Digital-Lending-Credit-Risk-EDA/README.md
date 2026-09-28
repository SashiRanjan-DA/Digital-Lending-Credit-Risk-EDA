# Digital Lending & Credit Risk Analysis

## Exploratory Data Analysis (EDA) Project

A Python-based exploratory data analysis project focused on borrower characteristics, loan behaviour and observed loan-default patterns in a digital lending dataset.

> **Note:** This project identifies patterns and associations in the observed data. It is not a production credit-scoring model and does not establish causal relationships.

## Business Problem

Digital lenders need to understand borrower profiles and loan characteristics associated with repayment outcomes. This project explores the dataset to identify portfolio patterns that can support deeper credit-risk analysis.

## Key Business Questions

- What is the overall distribution of loan defaults?
- How do borrower income and age vary across default and non-default groups?
- Which loan purposes show relatively higher observed default rates?
- How does loan grade relate to observed default rate and interest rate?
- Does loan amount relative to borrower income differ across default groups?
- How does previous recorded credit-default history relate to current loan status?
- Which borrower segments show comparatively higher observed default rates?

## Dataset

- **Rows:** 32,581
- **Columns:** 12
- **Target variable:** `loan_status`
- **Format:** CSV

### Variables

| Variable | Description | Type |
|---|---|---|
| `person_age` | Borrower's age | Numerical |
| `person_income` | Annual borrower income | Numerical |
| `person_home_ownership` | Home ownership category | Categorical |
| `person_emp_length` | Employment length in years | Numerical |
| `loan_intent` | Purpose of the loan | Categorical |
| `loan_grade` | Loan risk grade | Categorical |
| `loan_amnt` | Requested loan amount | Numerical |
| `loan_int_rate` | Loan interest rate | Numerical |
| `loan_status` | Loan default indicator | Binary |
| `loan_percent_income` | Loan amount as a proportion of income | Numerical |
| `cb_person_default_on_file` | Previous credit default recorded | Categorical |
| `cb_person_cred_hist_length` | Length of credit history | Numerical |

## Data Quality & Cleaning

The raw dataset contains missing values in `person_emp_length` and `loan_int_rate`, along with extreme observations such as unusually high ages and an employment-length value of 123 years. The notebook investigates these issues before analysis.

The cleaning workflow includes duplicate removal, validity checks, median imputation for selected numerical variables, and preservation of the target variable.

## Analysis Workflow

```text
Data Loading
     ↓
Data Quality Assessment
     ↓
Data Cleaning
     ↓
Feature Engineering
     ↓
Univariate Analysis
     ↓
Bivariate Analysis
     ↓
Multivariate Analysis
     ↓
Correlation Analysis
     ↓
Credit Risk Analysis
     ↓
Business Insights & Recommendations
```

## Analysis Areas

- Default distribution
- Borrower age and income
- Home ownership
- Loan purpose
- Loan grade
- Interest rates
- Loan amount
- Loan-to-income burden
- Previous credit-default history
- Credit history length
- Employment length
- Multivariate segment analysis
- Correlation analysis

## Tools & Technologies

**Python · Pandas · NumPy · Matplotlib · Seaborn · Plotly · Gradio · Jupyter Notebook**

## Repository Structure

```text
Digital-Lending-Credit-Risk-EDA/
│
├── Digital_Lending_Credit_Risk_EDA.ipynb
├── credit_risk_dataset.csv
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run

1. Clone or download this repository.
2. Keep `Digital_Lending_Credit_Risk_EDA.ipynb` and `credit_risk_dataset.csv` in the same folder.
3. Install the required packages:

```bash
pip install -r requirements.txt
```

4. Open the notebook in Jupyter Notebook, JupyterLab or Google Colab.
5. Run the cells from top to bottom.

## Business Interpretation

The project uses cautious interpretation throughout the analysis. Segment-level differences are described as observed associations rather than causal effects. Small segments should be interpreted with care, and EDA findings should not be treated as production credit-approval rules.

## Project Limitations

- The data is observational, so associations should not be interpreted as causal effects.
- Missing-value treatment is designed for exploratory analysis and may require different treatment in production.
- Some extreme observations are treated as implausible based on basic validity checks.
- The dataset does not represent every lender, borrower population or geography.
- A production credit-risk model would require separate validation, fairness checks, monitoring and regulatory review.

## Next Step

A natural extension of this project is to build and properly validate a credit-risk model using appropriate statistical and machine-learning techniques.

---

**Project Theme:** FinTech → Digital Lending → Credit Risk → Loan Default Analysis
