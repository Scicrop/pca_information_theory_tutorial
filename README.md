# PCA + Information Theory for Business: A Practical Mini‑Tutorial

**Goal.** Show how to use **Principal Component Analysis (PCA)** and **Information Theory** (Mutual Information and mRMR) to **reduce dimensionality** and **improve clarity** in predictive projects. The example predicts **life expectancy** from macro indicators (Gapminder).

**Why should business teams care?**
- **Faster, simpler models:** fewer inputs → quicker iteration, lower costs.
- **Less noise, less overfitting:** keep what matters; drop the rest.
- **Explainability:** know which inputs *actually* reduce uncertainty about the outcome.

## What you will learn
1. **Prepare features**: log‑transform skewed columns, one‑hot encode categoricals, standardize continuous features safely (train‑only).
2. **PCA (unsupervised):** compress continuous variables while keeping ≥95% of their variance; inspect which variables drive each PC.
3. **Mutual Information (supervised):** rank features by how much they reduce uncertainty in the target; visualize **redundancy** and the **mRMR** trade‑off.
4. **Compare strategies:** All features vs **Top‑k MI**, **Top‑k mRMR**, and **PCA95%+Dummies** using **R²** and **RMSE**.
5. **Interpretation toolkit** (plots you’ll see):
   - **Explained‑variance bar chart** per PC (with top contributing variables)
   - **PC1×PC2 heatmap** colored by the target
   - **MI ranking** (and *normalized* MI for classification)
   - **Redundancy heatmap** (I(Xi;Xj))
   - **Relevance×Redundancy scatter** (mRMR intuition)
   - **Cumulative information curve** (knee point)
   - **Information Diagram** (2‑variable “Venn in bits”)
   - **Entropy waterfall** (multi‑feature chain‑rule view)
   - **Predicted vs Actual** scatter and R² bars
