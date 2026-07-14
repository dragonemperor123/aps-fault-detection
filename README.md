# APS Truck Sensor Fault Detection

Binary classification project predicting Air Pressure System (APS) component
failures in heavy-duty trucks from sensor data, with a Power BI layer added
on top of the model to visualise predictions and failure risk.

## Overview

The core problem: given ~171 anonymised sensor readings per truck, predict
whether a component failure is caused by the APS system or something else.
The dataset is highly imbalanced (positive class is a small minority) and
has heavy missingness across many columns, making this a good exercise in
imbalanced classification and cost-sensitive evaluation — false negatives
(missed failures) are far more costly than false positives (unnecessary
checks).

## Components

1. **Predictive model** — XGBoost classifier trained on the Scania truck
   APS sensor dataset, tuned to handle severe class imbalance
2. **Power BI dashboard** — visualises the model's outputs: predictions,
   failure rates, and feature importance, to make the model's behaviour
   interpretable at a glance

## Model

- XGBoost classifier with hyperparameter tuning on high-dimensional,
  highly imbalanced sensor data
- Evaluation accounts for asymmetric misclassification costs (missed
  failures cost significantly more than false alarms)
- Handles substantial missing data across sensor readings

## Power BI Dashboard

- Visualises model predictions and predicted failure rates
- Feature importance view showing which sensor readings drive the model's
  decisions
- Built as a lightweight interpretability layer on top of the model output,
  not a production monitoring system

## Technology Stack

| Component | Technology |
|-----------|-----------|
| Predictive modelling | Python, XGBoost, Scikit-learn |
| Data processing | Pandas, NumPy |
| Visualisation | Power BI |
| Environment | Jupyter Notebook |

## Dataset

Scania truck APS sensor dataset (static, single training/test split —
not a live or monthly-updating data source). Anonymised sensor columns,
severe class imbalance, substantial missing values.

## Repository Structure

```
├── notebooks/          # EDA and model development
├── src/                # Data processing and model training code
├── data/                # Sample sensor data (anonymised)
├── docs/                # Dashboard screenshots
└── README.md
```

## Notes

This project started from a well-known public APS fault detection template
and was extended with a Power BI visualisation layer for model
interpretability. It's a learning/portfolio project, not a production
system.

---
**Author:** Adwait Sawant
**Contact:** adwait191@gmail.com
