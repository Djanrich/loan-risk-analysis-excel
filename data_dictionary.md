# Data Dictionary - Loan Risk Analysis

## Original Dataset Columns

| Column Name | Data Type | Description | Example Values |
|-------------|-----------|-------------|----------------|
| Loan_ID | Text | Unique identifier for each loan application | LP001002, LP001003 |
| Gender | Text | Applicant's gender | Male, Female |
| Married | Text | Marital status of applicant | Yes, No |
| Dependents | Text | Number of dependents | 0, 1, 2, 3+ |
| Education | Text | Education level of applicant | Graduate, Not Graduate |
| Self_Employed | Text | Self-employment status | Yes, No |
| ApplicantIncome | Number | Primary applicant's income (monthly) | 5849, 4583, 3000 |
| CoapplicantIncome | Number | Co-applicant's income (monthly) | 0, 1508, 2358 |
| LoanAmount | Number | Loan amount requested (thousands) | 128, 66, 120 |
| Loan_Amount_Term | Number | Loan term in months | 360, 120, 240 |
| Credit_History | Number | Credit history indicator (1=Yes, 0=No) | 1, 0 |
| Property_Area | Text | Property location type | Urban, Semiurban, Rural |
| Loan_Status | Text | Loan approval status | Y (Approved), N (Rejected) |

## Calculated/Derived Columns

| Column Name | Formula/Logic | Description | Business Purpose |
|-------------|---------------|-------------|------------------|
| Total_Income | ApplicantIncome + CoapplicantIncome | Combined household income | Better assessment of repayment capacity |
| Income_Category | IF statements based on Total_Income | Low/Medium/High income brackets | Segmentation for analysis |
| Loan_Size_Category | IF statements based on LoanAmount | Small/Medium/Large loan categories | Risk assessment by loan size |
| Risk_Score | Weighted scoring algorithm | Numerical risk assessment (0-100) | Quantitative risk measurement |
| Risk_Category | IF statements based on Risk_Score | Very High/High/Medium/Low Risk | Categorical risk classification |
| Monthly_Payment | PMT function calculation | Estimated monthly payment | Affordability assessment |
| Loan_Decision | Complex IF/AND logic | Automated approval recommendation | Decision support system |

## Data Quality Notes

### Missing Value Treatment
- **Gender**: Replaced blanks with "Unknown"
- **Dependents**: Replaced blanks with "0" 
- **Self_Employed**: Replaced blanks with "No"
- **LoanAmount**: Replaced blanks with dataset average
- **Loan_Amount_Term**: Replaced blanks with 360 (standard 30-year term)
- **Credit_History**: Replaced blanks with 0 (no credit history)

### Data Validation Rules
- **Income values**: Must be positive numbers
- **Loan amounts**: Must be positive numbers  
- **Credit_History**: Must be 0 or 1
- **Categorical fields**: Standardized to consistent values

## Business Logic

### Risk Scoring Algorithm
```
Risk_Score = Credit_History_Points + Education_Points + Income_Points + Location_Points

Where:
- Credit_History_Points: 40 if Yes, 0 if No
- Education_Points: 20 if Graduate, 0 if Not Graduate  
- Income_Points: 20 if >$5000, 0 if ≤$5000
- Location_Points: 10 if Urban, 5 if Semiurban/Rural
```

### Approval Decision Logic
```
APPROVE if:
- Credit_History = 1 AND
- Risk_Score > 25 AND  
- Total_Income ≥ 30% of Loan_Amount

Otherwise: REVIEW/REJECT
```

### Income Categories
- **Low Income**: ≤ $4,000
- **Medium Income**: $4,001 - $10,000
- **High Income**: > $10,000

### Loan Size Categories  
- **Small Loan**: ≤ $100K
- **Medium Loan**: $101K - $200K
- **Large Loan**: > $200K