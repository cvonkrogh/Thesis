# ESRS-Disclosure Depth E

This repo holds a self-contained notebook that links the ESRS tables we scraped from 100 EU annual reports with firm fundamentals from Yahoo Finance and then asks **what drives variation in ESG disclosure depth** in the first CSRD year.

| File | What it does |
|------|--------------|
| **Subquestion_regression_model.ipynb** | loads the ESRS × company matrix, merges fundamentals, and estimates all regressions |
| **output/** | CSV files |

## Models produced in the notebook / output

| Label | Dependent var(s) | Model | Key controls |
|-------|------------------|-------|--------------|
| *Logit-ESRS-<code>* | Single ESRS item (binary) | Logistic | Size, ROA, leverage, liquidity, m-cap, country FE, sector FE |
| **A** | ESG_count + E/S/G pillar counts | Neg-binomial | Fundamentals + **country** FE |
| **B** | same | Neg-binomial | Fundamentals + **sector** FE |
| **C** | same | Neg-binomial | Fundamentals + country + sector FE |
| **D** | same | Neg-binomial | High-emit dummy, Hofstede “femininity”, + country FE |

Open the notebook and hit **Run All** to reproduce every table and figure.















