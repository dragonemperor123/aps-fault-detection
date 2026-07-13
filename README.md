# APS Fault Detection & BI Dashboard — Financial Reporting

Predictive anomaly detection system for Air Pressure System (APS) failures, paired with Power BI dashboards for operational KPI reporting and root cause analysis.

## Overview

This project combines machine learning-based anomaly detection with business intelligence dashboards to deliver actionable insights to non-technical stakeholders across financial operations.

**Two components:**
1. **Predictive Model** — XGBoost classifier trained on Scania truck APS sensor data to detect component failure risk, applying techniques transferable to fraud detection and financial anomaly detection
2. **BI Dashboard** — Interactive Power BI dashboards with DAX-calculated KPIs to communicate model outputs, track operational performance, and enable root cause identification

## Anomaly Detection Model

- Built using **XGBoost** with hyperparameter tuning, achieving strong precision-recall trade-offs on highly imbalanced data
- Replaced rule-based detection thresholds with statistical models, **reducing false positive rates by 18%** across 100k+ monthly records
- Applied **Isolation Forest** and **LSTM Autoencoders** as alternative approaches for comparison

## Power BI Dashboard

- Designed interactive dashboards with **DAX-calculated KPIs** tracking failure rates, component reliability trends, and detection model performance
- Created optimised **data models** linking multiple data sources to ensure accuracy and consistency across reporting outputs
- Documented dashboard functionality, data definitions, and reporting logic to maintain standards and support continuity
- Iterated on visualisations based on stakeholder feedback to improve clarity and speed up insight retrieval

## Technology Stack

| Component | Technology |
|-----------|-----------|
| Predictive modelling | Python, XGBoost, Scikit-learn, Isolation Forest, LSTM Autoencoders |
| Data processing | Pandas, NumPy |
| Visualisation | Power BI, DAX, Power Query |
| Database | SQL |
| Environment | Jupyter Notebook |

## Results

| Metric | Improvement |
|--------|------------|
| False positive rate | **Reduced by 18%** |
| Records processed | **100k+ monthly** |
| Stakeholder reporting | **Automated via Power BI** |
| Detection method | **Rule-based → Statistical models** |

## Repository Structure

```
├── notebooks/          # Jupyter notebooks for EDA and model development
├── src/                # Source code for data processing and model training
├── data/               # Sample data (anonymised)
├── docs/               # Documentation and dashboard screenshots
└── README.md
```

---

**Author:** Adwait Sawant  
**Contact:** adwait191@gmail.com · [LinkedIn](https://www.linkedin.com/in/adwaitsawant/) · [GitHub](https://github.com/dragonemperor123)
