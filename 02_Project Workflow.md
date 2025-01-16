# Biomarker Data Analysis and Predictive Modeling

This project explores the relationship between Alzheimer's disease biomarkers and various predictors using advanced statistical and machine learning techniques. The workflow encompasses data cleaning, statistical modeling, and hyperparameter optimization, resulting in robust insights and predictive models.

---

## Project Workflow

### 1. **Data Cleaning and Preparation**
- Imported biomarker and UDS data from the `NACCdata` package.
- Standardized and merged datasets to include first valid visits for each patient.
- Addressed missing data and encoded categorical variables:
  - Recoded unknown and non-collected values as `NA`.
  - Converted variables to binary or factors as appropriate.
- Final dataset: `df` with cleaned and structured variables.

---

### 2. **Linearity Assumption Validation**
- Checked linearity of log-odds for continuous variables using **partial residual plots**.
- Generated visualizations for all predictors, ensuring linear relationships.
- Saved plots in a PDF: `partial_residuals_plots.pdf`.

---

### 3. **Logistic Regression with LASSO**
- Built a LASSO logistic regression model to handle multicollinearity and select important predictors.
- Tuned the penalty parameter (`lambda`) with 10-fold cross-validation using a grid search.
- Identified the optimal model based on ROC-AUC.
- Bootstrapped the LASSO model:
  - Created 1,000 bootstrap samples.
  - Extracted bootstrapped coefficient estimates for confidence interval construction.
- Visualized coefficient distributions and calculated normal-theory confidence intervals.

---

### 4. **Neural Network Modeling**
- Used **H2O** to train deep learning models with a hyperparameter grid search:
  - Explored various architectures (hidden layers, learning rates, regularization, dropout).
  - Optimized using a random discrete search strategy.
- Evaluated models on a validation set:
  - Selected the best-performing model based on accuracy and F1-score.
  - Threshold optimized for best classification accuracy.
- Achieved a final accuracy of **X%** (replace with actual metric).

---

## Key Findings
1. **Predictive Biomarkers**: Variables such as `CSFTTAU`, `CSFABETA`, and demographic factors (age, education, and sex) significantly contributed to Alzheimer's disease predictions.
2. **Model Interpretability**: Bootstrapped LASSO coefficients revealed robust confidence intervals, highlighting key predictors.
3. **Performance**: Neural network models demonstrated strong classification performance, optimizing F1-score thresholds.

---
   git clone <repository_url>
