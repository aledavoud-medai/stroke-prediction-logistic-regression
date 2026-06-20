# Stroke Prediction Using Logistic Regression

This project is an exploratory clinical machine learning analysis using a publicly available stroke prediction dataset.

## Objective

The objective of this project is to build and evaluate logistic regression models for stroke prediction using routinely available clinical variables. The main focus is not only model training, but also understanding class imbalance, clinical interpretation, and the limitations of medical machine learning models.

## Dataset

The project uses a publicly available stroke prediction dataset. The dataset includes variables such as:

- Age
- Gender
- Hypertension
- Heart disease
- Average glucose level
- BMI
- Smoking status
- Work type
- Residence type
- Stroke outcome

The target variable is:

- `stroke`: 0 = no stroke, 1 = stroke

## Project Workflow

The notebook includes the following steps:

1. Project objective
2. Importing libraries
3. Loading the dataset and basic overview
4. Exploratory data analysis
5. Data cleaning
6. Preprocessing
7. Train-test split
8. Model development
9. Model evaluation
10. Threshold tuning
11. Coefficient interpretation
12. Limitations
13. Conclusion
14. What I learned

## Key Findings

The standard logistic regression model achieved high accuracy but showed very poor sensitivity for stroke detection. This demonstrated that accuracy alone can be misleading in imbalanced medical datasets.

Balanced logistic regression improved sensitivity and reduced false negatives, but this came at the cost of increased false-positive predictions.

Threshold tuning showed the trade-off between sensitivity and specificity. Lower thresholds increased sensitivity but also increased false positives.

After scaling numerical variables, age appeared as the most clinically meaningful coefficient. Some categorical coefficients, such as `work_type_children`, were interpreted cautiously because of reference-category coding, class weighting, correlation with age, and small subgroup size.

## Clinical Interpretation

This project highlights an important principle in clinical machine learning:

> In imbalanced medical datasets, a model with high accuracy may still perform poorly for detecting the clinically important minority class.

For stroke prediction, missing true stroke cases is clinically important. Therefore, sensitivity/recall, false negatives, specificity, and threshold selection should be considered alongside accuracy.

## Limitations

- This is an educational and exploratory project.
- The dataset is publicly available and has limited information about sampling and data collection methods.
- The outcome is highly imbalanced, with relatively few stroke cases.
- No external validation was performed.
- Important clinical variables such as atrial fibrillation, medications, imaging findings, previous stroke/TIA history, laboratory data, and neurological severity scores were not available.
- The model should not be used as a clinical diagnostic tool.

## Conclusion

This project demonstrates a basic clinical machine learning workflow for an imbalanced binary classification problem. It emphasizes exploratory data analysis, preprocessing, logistic regression modeling, evaluation beyond accuracy, threshold tuning, and cautious clinical interpretation.

## Requirements

Install the required packages using:

```bash
pip install -r requirements.txt