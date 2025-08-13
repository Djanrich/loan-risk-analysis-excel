# 🏦 Loan Risk Analysis - Excel Portfolio Project

A comprehensive loan risk assessment and prediction model built entirely in Microsoft Excel, showcasing advanced data analysis, visualization, and business intelligence skills.

## 📊 Project Overview

This project analyzes a loan dataset of 614 applications to identify risk factors, approval patterns, and business insights using advanced Excel techniques. The analysis includes data cleaning, statistical analysis, interactive dashboards, and executive reporting.

**🎯 Key Objectives:**
- Predict loan approval likelihood based on applicant characteristics
- Identify key risk factors influencing loan decisions  
- Create interactive business intelligence dashboard
- Provide actionable recommendations for lending strategy

## 🛠️ Technical Skills Demonstrated

### Core Excel Skills
- **Data Cleaning & Preparation**: Handling missing values, standardizing formats
- **PivotTables & PivotCharts**: Multi-dimensional analysis and visualization
- **VLOOKUP & INDEX/MATCH**: Advanced lookup functions and data retrieval
- **Conditional Formatting**: Visual data analysis and KPI highlighting
- **Data Validation**: Creating interactive dropdown menus and user inputs
- **Financial Functions**: PMT calculations for loan payment estimates

### Advanced Features
- **Interactive Dashboard**: Multi-chart dashboard with slicers and filters
- **Risk Scoring Model**: Calculated risk assessment algorithm
- **Loan Eligibility Calculator**: Dynamic decision-making tool
- **Executive Summary Report**: Professional business intelligence reporting

## 📁 File Structure

```
📦 loan-risk-analysis-excel/
├── 📄 Loan_Risk_Analysis_Portfolio.xlsx    # Main Excel workbook
├── 📄 README.md                            # Project documentation
├── 📄 Project_Methodology.md               # Detailed technical approach
├── 📄 Data_Dictionary.md                   # Column definitions and explanations
└── 📸 screenshots/                         # Dashboard and analysis screenshots
    ├── dashboard_overview.png
    ├── pivot_analysis.png
    └── risk_calculator.png
```

## 🔍 Analysis Highlights

### Key Findings
- **Overall Approval Rate**: 68.7% (422 out of 614 applications)
- **Income Impact**: Higher income categories show 15%+ better approval rates
- **Credit History**: Single strongest predictor of loan approval
- **Geographic Patterns**: Urban areas average higher loan amounts ($142K+)

### Risk Distribution
- **High Risk**: 28.3% of applications
- **Medium Risk**: 54.2% of applications  
- **Low Risk**: 17.4% of applications

## 📈 Dashboard Features

### Interactive Elements
- **Loan Approval Analysis**: Breakdown by demographics and income
- **Risk Assessment Charts**: Visual risk distribution and patterns
- **Geographic Analysis**: Property area impact on loan characteristics
- **KPI Scorecards**: Real-time portfolio performance metrics

### Business Tools
- **Loan Eligibility Calculator**: Interactive decision-making tool
- **Risk Scoring System**: Automated applicant risk assessment
- **What-If Analysis**: Scenario planning for different criteria

## 🎯 Business Recommendations

### Immediate Actions
1. **Enhanced Income Verification**: Strengthen documentation requirements
2. **Risk Model Refinement**: Weight credit history more heavily in decisions
3. **Process Optimization**: Create fast-track approval for low-risk applicants

### Strategic Initiatives  
1. **Market Expansion**: Target educated professionals in growth areas
2. **Portfolio Monitoring**: Implement real-time risk tracking dashboards
3. **Predictive Modeling**: Develop advanced default probability models

## 📊 Technical Methodology

### Data Processing Pipeline
1. **Data Import & Quality Assessment**: Identified missing values and inconsistencies
2. **Data Cleaning**: Applied business logic to handle missing values
3. **Feature Engineering**: Created calculated fields for risk scoring and categorization
4. **Analysis & Modeling**: Built PivotTable-based analytical framework
5. **Visualization**: Developed interactive dashboard with multiple chart types
6. **Reporting**: Generated executive summary with actionable insights

### Excel Functions Utilized
```excel
# Risk Scoring Formula
=(IF(Credit_History=1,40,0))+(IF(Education="Graduate",20,0))+(IF(Income>5000,20,0))

# Loan Decision Logic  
=IF(AND(Credit_History=1,Risk_Score>25,Total_Income>=Loan_Amount*0.3),"APPROVE","REVIEW")

# Monthly Payment Calculation
=PMT(0.08/12,360,-Loan_Amount*1000)
```

## 🚀 How to Use This Project

### Prerequisites
- Microsoft Excel 2016 or later
- Basic understanding of Excel functions and PivotTables

### Getting Started
1. **Download** the Excel file from this repository
2. **Enable macros** if prompted (for full interactivity)
3. **Explore sheets** in this order:
   - `Raw_Data` → Original dataset
   - `Clean_Data` → Processed data with calculations
   - `Analysis` → PivotTable analysis and loan calculator
   - `Dashboard` → Interactive visual dashboard
   - `Summary_Report` → Executive findings and recommendations

### Interactive Features
- Use **slicers** on Dashboard to filter data by demographics
- Try the **Loan Calculator** in Analysis sheet with different inputs
- Explore **PivotTables** by dragging fields to different areas

## 📸 Screenshots

### 🎯 Interactive Dashboard Overview
![Dashboard Overview](screenshots/dashboard_overview.png)
*Professional Excel dashboard featuring loan approval analysis, risk distribution charts, KPI scorecards, and interactive slicers for filtering by demographics and loan characteristics*

### 🧮 Dynamic Loan Risk Calculator  
![Risk Calculator](screenshots/risk_calculator.png)
*Interactive loan eligibility calculator with dropdown menus, real-time risk scoring, automated approval decisions, and monthly payment calculations*

### 📊 Advanced PivotTable Analysis
![PivotTable Analysis](screenshots/pivot_analysis.png)
*Comprehensive PivotTable analysis showing loan approval patterns across multiple demographic and financial variables*

## 🎓 Learning Outcomes

This project demonstrates proficiency in:
- **Data Analysis**: Statistical analysis and pattern recognition
- **Business Intelligence**: KPI development and performance monitoring  
- **Excel Mastery**: Advanced functions, PivotTables, and visualization
- **Risk Management**: Credit risk assessment and scoring methodologies
- **Communication**: Executive reporting and recommendation development



## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

**⭐ If this project helped you learn Excel or data analysis techniques, please give it a star!**

*Built with ❤️ and lots of Excel formulas*