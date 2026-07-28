# FinSearch '26 End-Term Project

## Understanding Credit Score Algorithms

**Research question:** Do interpretable credit-scoring models remain competitive with machine-learning models when predictive discrimination, probability calibration, fairness, and asymmetric lending costs are evaluated together?

### Project objective

This project develops and evaluates a reproducible credit-risk classification pipeline. It compares Logistic Regression, Decision Tree, Random Forest, and Gradient Boosting on the UCI Statlog German Credit dataset. The analysis does not treat accuracy as the only objective. It evaluates:

- ROC-AUC and KS statistic for risk ranking
- Precision, recall, F1-score, and confusion matrices
- Brier score and calibration for probability quality
- The UCI asymmetric cost matrix, where approving a bad borrower is five times as costly as rejecting a good borrower
- Subgroup diagnostics by age and personal-status/sex proxy, presented as exploratory fairness checks
- Model interpretability through coefficients, permutation importance, and score explanations

### Research hypothesis

Ensemble models may achieve slightly better discrimination, but a regularized Logistic Regression model can remain competitive after calibration and cost-sensitive threshold selection, while offering stronger interpretability and governance advantages.

### Repository structure

| File | Purpose |
|---|---|
| `Credit_Scoring_Algorithms_Analysis.ipynb` | Complete executable analysis |
| `FinSearch_End_Term_Report.pdf` | Submission-ready research report |
| `Research_Idea_and_Methodology.md` | Concise research definition |
| `requirements.txt` | Python dependencies |

### Running the notebook

1. Open the notebook in Google Colab or Jupyter.
2. Run all cells in order.
3. Internet is needed only for the first dataset download.
4. The notebook saves tables and figures to a local `outputs/` folder.

The dataset contains 1,000 historical German loan applicants and should be treated as an educational benchmark, not as a production lending dataset or evidence about present-day Indian borrowers.
