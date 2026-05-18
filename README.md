**Author:** Amr Thabet | Healthcare Data & Business Analyst | Abu Dhabi, UAE
**Tools:** Python · scikit-learn · SQL · pandas · matplotlib · seaborn
**Dataset:** Synthetic 3,000-member GCC chronic disease cohort (2023–2024)

## Business Context

Chronic diseases account for the majority of health insurance spend across the UAE and GCC.
Diabetes, hypertension, and cardiac conditions alone drive billions in annual claims.
This project answers three core questions every UAE insurer and RCM team faces:

1. Which conditions and member segments are driving the most cost?
2. Which clinical factors predict high-cost membership before costs spike?
3. What is the financial case for early intervention programmes?

## Key Findings

- Diabetes + Cardiac members average AED 72,923/year — 3.4x more than Hypertension alone
- Top 20% of members account for 37.4% of total portfolio spend (AED 45.2M of AED 120.8M)
- Random Forest model achieves AUC 0.950 — correctly catches 87% of high-cost members
- Top predictors: condition type, age, BMI, inpatient days, systolic BP
- Potential saving of AED 3.4M if 70% of high-cost members are flagged for early intervention

## Project Structure

- data/ — chronic_disease_cohort.csv (3,000-member synthetic GCC cohort)
- notebooks/01_generate_dataset.ipynb — Dataset generation with GCC parameters
- notebooks/02_exploratory_analysis.ipynb — 9 charts answering business questions
- notebooks/03_sql_views.ipynb — 6 analyst-grade SQL queries
- notebooks/04_predictive_model.ipynb — Random Forest + Logistic Regression model
- outputs/ — All chart PNGs and SQL CSV exports

## Notebooks

### 01 — Dataset generation
3,000-member synthetic cohort with realistic UAE parameters: 7 payers (Daman HAAD,
AXA Gulf, BUPA Global, MetLife, ADNIC, Cigna, Sukoon), 5 emirates, 5 chronic
conditions, cost drivers calibrated to GCC health insurance benchmarks.

### 02 — Exploratory analysis
9 business-focused charts: cost by condition, risk tier, emirate exposure,
payer benchmarking, BMI vs cost, ER utilisation, care type breakdown,
age distribution, and high-cost member rate by condition.

### 03 — SQL views
6 analyst-grade SQLite queries: cost by condition, high-cost member profile,
payer benchmarking with portfolio variance, compliance impact,
risk tier by emirate, and cost concentration (80/20 rule).

### 04 — Predictive model
Logistic Regression baseline (AUC 0.785) vs Random Forest (AUC 0.950).
Includes ROC curve, confusion matrix, feature importance, and AED business ROI.

## Model Performance

| Model | AUC-ROC |
|---|---|
| Logistic Regression | 0.785 |
| Random Forest | 0.950 |

## Related Projects

- Project 1 — UAE Claims Denial Analysis: https://github.com/AmrThabetA/healthcare-claims-analysis
- Project 2 — RCM Performance Dashboard: https://public.tableau.com/views/UAE-MENA-RCM-Dashboard/UAEMENARCMPerformanceDashboard2023-2024
