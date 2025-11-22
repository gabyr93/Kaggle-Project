# Home Credit Default Risk — Individual Portfolio (Gaby Rodriguez)
Business Problem & Objective

**Home Credit** provides loans to customers who often don’t have long or traditional credit histories. The business challenge is to identify which applicants are likely to default without rejecting reliable borrowers just because they have limited credit records.

Our objective was to predict each applicant’s probability of default so the company can make smarter, lower-risk lending decisions while still expanding access to credit.

**Group Solution**

Our team built an end-to-end modeling pipeline using multiple data sources tied to each applicant:

- Application data: income, employment, demographics, living situation
- Bureau data: existing loans and credit exposure with other lenders
- Installment payments: repayment behavior over time (on-time vs late patterns)
- POS/Cash loan history: short-term loan usage and repayment timing

We engineered aggregated behavioral features (e.g., total existing debt, credit utilization, counts of late payments, and consistency of repayment). We tested several models including baseline logistic regression, random forest, and gradient boosting, and selected the best model based on cross-validated performance.

## My Individual Contributions

My personal work on the project included:

- EDA & cleaning: explored distributions, missingness, outliers, and the default imbalance; documented key patterns and data-quality issues.
- Feature engineering: created and validated aggregated features across tables (ex: bureau/installments/POS summaries).
- Modeling support: Linear Regression and Lasso Rgression
- Communication: supported the business framing and interpretation of results for the final deliverables.

You can find my individual notebooks in the /portfolio folder.

**Business Value**

The final model helps Home Credit:

- flag high-risk applicants earlier,
- reduce expected default losses,
- and continue approving trustworthy borrowers with limited credit history.

Overall, this supports more consistent approval decisions and better risk management.

**Difficulties We Encountered**
Key challenges in this project included:

- heavy missingness and inconsistent reporting across tables,
- strong class imbalance (defaults are rare),
- leakage-safe aggregation across time-based behavior,
- and managing a high-dimensional engineered feature space.

**What I Learned**

This project strengthened my ability to:

- engineer features from multiple relational tables,
- handle missing data and class imbalance responsibly,
- validate models without leakage,
- and translate ML results into business decisions.

Notebooks Included

EDA notebook: /portfolio/EDA_HOMECREDIT.qmd

(More individual notebooks will be added here as I upload them.)
