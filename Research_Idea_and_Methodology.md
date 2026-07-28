# Clearly Defined Research Idea

## Title

**Beyond Accuracy: Comparing Interpretable and Machine-Learning Credit-Scoring Models under Cost, Calibration, and Fairness Constraints**

## Central research question

Do more complex machine-learning models provide a practically meaningful advantage over an interpretable logistic credit-score model once four dimensions are considered together: discrimination, probability calibration, asymmetric lending cost, and subgroup fairness?

## Motivation

Credit scores influence loan approvals, interest rates, credit limits, and financial inclusion. A model with high raw accuracy can still be unsuitable if it underestimates default probabilities, creates excessive false approvals, or performs very differently across demographic groups. Financial institutions therefore need models that are not merely predictive, but also calibrated, interpretable, cost-aware, stable, and auditable.

## Objectives

1. Explain traditional bureau scores and application-scoring systems.
2. Build four supervised-learning models on a public credit-risk dataset.
3. Compare ranking ability using ROC-AUC and the KS statistic.
4. compare probability quality using Brier score and calibration curves.
5. Select a lending threshold using the dataset's asymmetric cost matrix.
6. Examine subgroup error rates as exploratory fairness diagnostics.
7. discuss the accuracy-versus-interpretability trade-off for regulated lending.

## Dataset

The UCI Statlog German Credit dataset contains 1,000 applicants, 20 predictor variables, and a binary good/bad credit-risk outcome. The original dataset specifies that misclassifying a bad applicant as good costs five units, while rejecting a good applicant costs one unit. Its age and personal-status variables permit limited subgroup diagnostics.

## Models

- Logistic Regression: interpretable statistical baseline
- Decision Tree: transparent nonlinear rules
- Random Forest: bagged nonlinear ensemble
- Gradient Boosting: sequential ensemble

## Evaluation framework

| Dimension | Measures |
|---|---|
| Discrimination | ROC-AUC, KS statistic |
| Classification | Precision, recall, F1, confusion matrix |
| Calibration | Brier score, calibration curve |
| Lending economics | Expected asymmetric misclassification cost |
| Fairness diagnostics | Approval rate, TPR, FPR and adverse-impact ratio by subgroup |
| Explainability | Logistic coefficients and permutation importance |

## Expected contribution

The project demonstrates why a lender should not select a scoring algorithm from accuracy alone. It provides a compact, reproducible framework for choosing a model and decision threshold while acknowledging economic consequences, governance, interpretability, and fairness.

## Scope limitations

This is an educational benchmarking study. The historical German sample is small and is not representative of modern India. Sensitive-attribute analysis is constrained by dataset coding. No model in this project should be deployed for real lending decisions without local data, legal review, stability testing, monitoring, and human oversight.
