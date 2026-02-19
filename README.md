
# QuickLoan Mobile Ethical Data Review

## 📋 Project Overview

This repository contains a comprehensive data governance review for **QuickLoan Mobile**, a fast-growing fintech startup based in Ghana that offers instant micro-loans via a mobile app. The review was conducted as an independent data governance consultant to identify and address serious concerns about their data practices, specifically around Governance, Quality, and Ethics.

## 🎯 Project Objectives

This project demonstrates the ability to:

1. **Identify Risks**: Classify and analyze issues related to:
   - Data Quality
   - Legal Compliance (Ghana's Data Protection Act, Act 843)
   - Algorithmic Fairness/Bias

2. **Apply Principles**: Propose solutions using core principles:
   - Data Minimization
   - Consent Management
   - Data Classification
   - Data Retention

3. **Drive Ethical Practice**: Recommend practical, ethical reporting metrics to ensure transparency in automated decision-making processes.

## 🔍 Key Findings

### Data Quality Risk
- Core loan fields are often missing or inconsistently formatted
- Noisy data (contact lists, device logs) used without validation
- Impact: Unreliable model features leading to incorrect loan decisions

### Legal & Compliance Risk
- Excessive PII collection (full contact list, GPS history, device logs)
- No explicit consent capture mechanism
- Violation of Ghana's Data Protection Act (Act 843)
- **Data Classification**: Confidential / Sensitive

### Bias & Fairness Risk
- ML model uses proxy variables (location clusters, phone type, contact networks)
- Historical training data reflects financial exclusion patterns
- No monitoring of approval outcomes by demographic groups
- Risk of disparate impact on vulnerable groups (rural residents, women, informal workers)

## 📊 Proposed Solution: Fair Approval Parity Ratio (FAPR)

**Metric Definition**: 
```
FAPR = (minimum approval rate across groups) / (maximum approval rate across groups)
```

**Purpose**: Track fairness in loan approval decisions across demographic groups (gender, region, income type) to ensure equitable treatment.

**Visualization**: Grouped bar chart or time-series line chart with threshold indicators (e.g., 0.8) to flag when parity drops to risky levels.

## 📁 Repository Structure

```
Data_Governance/
├── README.md                                    # This file
├── quickloan_governance_lab_answers.md         # Complete lab answers (Markdown format)
└── quickloan_governance_lab_answers.txt        # Complete lab answers (Text format)
```

## 📝 Deliverables

### Deliverable 1: Governance Review Card
Complete analysis of three distinct risk findings:
- Data Quality Risk
- Legal & Compliance Risk (with Data Classification)
- Bias & Fairness Risk (with Source of Bias identification)
- Storytelling/Reporting Metric (FAPR)

### Deliverable 2: Corrected Data Flow Diagram
Six key corrections identified and annotated:
1. Data Minimization at Step 1 (User Mobile App)
2. Consent & Policy Service between Step 2-3 (API Gateway to Raw Data DB)
3. Classification & Retention Rules at Step 3 (Raw Data DB)
4. Quality Checks & Feature Store at Step 5 (Preprocessing Service)
5. Decision Logging & Transparency at Step 7 (Decision Service)
6. Masking & Anonymization at Step 9 (Analytics DB)

### Deliverable 3: Summary of Review Process
200-300 word essay explaining:
- How Data Lifecycle and Classification principles were used to identify risks
- How the proposed FAPR metric ensures ethical and transparent governance

## 🔧 Key Recommendations

1. **Data Minimization**: Collect only necessary data for credit scoring
2. **Consent Management**: Implement explicit, granular opt-in consent with audit logs
3. **Data Classification**: Label all PII as Confidential/Sensitive with appropriate access controls
4. **Retention Policies**: Define and enforce data retention schedules
5. **Quality Controls**: Implement validation rules and data quality dashboards
6. **Fairness Monitoring**: Regular bias audits and FAPR tracking by demographic groups
7. **Transparency**: Decision logging with explanations and human review for borderline cases
8. **Data Protection**: Masking/anonymization in analytics and secure handling of PII

## 📚 Legal Framework

This review is conducted in compliance with:
- **Ghana's Data Protection Act, 2012 (Act 843)**
- Core principles: Lawfulness, Data Minimization, Purpose Limitation, Storage Limitation, Accuracy, Integrity & Confidentiality

## 👤 Author

**Niyonkuru Valens**  
Independent Data Governance Consultant

## 📄 License

This project is for educational and professional purposes.

## 🔗 Repository

[GitHub Repository](https://github.com/valensniyonkuru/Data_Governance.git)

---

*Last Updated: February 2026*
