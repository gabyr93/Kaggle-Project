# Home Credit Default Risk — Individual Portfolio 

## 1. Business Problem & Objective

Home Credit provides loans to customers who often don’t have long or traditional credit histories.  
The challenge is to identify which applicants are likely to default **without** rejecting reliable borrowers just because they lack standard credit records.

Our objective in this project was to predict each applicant’s probability of default so the company can make smarter, lower-risk lending decisions while still expanding access to credit.


## 2. Our Group’s Solution

As a team, we built an end-to-end modeling pipeline using multiple data sources tied to each applicant:

- **Application data** – income, employment, demographics, living situation  
- **Bureau data** – existing loans and credit exposure with other lenders  
- **Installment payments** – repayment behavior over time (on-time vs late patterns)  
- **POS / cash loans** – short-term loan usage and repayment timing  

From these tables we engineered aggregated behavioral features, such as:

- Total existing debt and credit utilization  
- Number and share of late payments  
- Consistency of repayment behavior over time  

We compared several models, including a **baseline logistic regression**, **regularized linear models**, and **tree-based approaches**.  
Models were evaluated using cross-validation and holdout performance (e.g., ROC–AUC and related metrics), and we selected the model that offered the best balance of accuracy and stability for risk scoring.



## 3. My Individual Contributions

My personal work on the project included:

- **EDA & cleaning** – explored distributions, missingness, outliers, and the class imbalance in defaults; documented key patterns and data-quality issues.  
- **Feature engineering** – created and validated aggregated features across bureau, installment, and POS tables.  
- **Modeling** – built and evaluated **baseline logistic regression** and **LASSO regression** models as part of the model comparison.  
- **Communication** – helped with the business framing and interpretation of the modeling results for our final write-up and presentation.

My individual notebooks are in the `/portfolio` folder of this repo.



## 4. Business Value

The final modeling pipeline helps Home Credit:

- Flag **high-risk applicants** before approval,  
- Reduce **expected default losses**, and  
- Continue approving **trustworthy borrowers** who lack traditional credit history.

Used in production, these risk scores would support more consistent approval decisions, healthier loan portfolios, and more inclusive access to credit.



## 5. Difficulties We Encountered

Some of the main challenges our group faced were:

- **Heavy missingness** and inconsistent reporting across tables.  
- **Strong class imbalance**, since true defaults are rare.  
- Designing **leakage-safe feature aggregation** using time-ordered behavior.  
- Managing a **high-dimensional feature space** after engineering many summarized variables.  

We iterated on our data processing pipeline several times to keep it reproducible and avoid leakage.



## 6. What I Learned

Through this project I strengthened my ability to:

- Work with large, relational data and engineer features across multiple tables,  
- Handle missing data and class imbalance in a principled way,  
- Compare baseline and regularized models while guarding against leakage, and  
- Translate model outputs into business actions and talking points for stakeholders.



## 7. Notebooks Included (Individual Work)

- **`EDA_HomeCredit.qmd`** – exploratory data analysis, missingness, imbalance, and key data patterns.  
- **`Baseline_Model.qmd`** – baseline logistic regression model setup, training, and evaluation.  
- **`Lasso.rmarkdown`** – LASSO regression modeling and comparison to the baseline.

