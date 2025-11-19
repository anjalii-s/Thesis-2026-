1. Data Loading & Preprocessing
Load German Credit dataset.

Apply OneHotEncoder for categorical features and StandardScaler for numeric features.

2. Model & Sampler Setup
Define models: Random Forest (RF), XGBoost (XGB), LightGBM (LGB).

Define imbalance handling: None, SMOTE, Borderline, ADASYN, SMOTEENN, SMOTETomek, Under, CostSensitive.

3. Training Loop
Train all model × sampler combinations across multiple seeds.

Collect AUC scores.

4. Explanation Methods
Implement SHAP (TreeExplainer).

Implement Banzhaf approximation (coalition sampling).

Implement Owen values (group‑aware coalitions).

5. Metrics Functions
Stability (CV).

Jaccard similarity of top‑k features.

Interpretability score 
𝐼
=
𝛽
(
1
−
𝐶
𝑉
)
+
(
1
−
𝛽
)
𝐽
.

Trade‑off score 
𝑇
(
𝛼
)
=
𝛼
⋅
𝐴
𝑈
𝐶
+
(
1
−
𝛼
)
⋅
𝐼
.

6. Collect Explanations
For each configuration, compute SHAP, Banzhaf, Owen explanations on subsampled test sets.

7. Compute Metrics
Aggregate AUC, CV, Jaccard, I, and T across seeds.

Store results in metrics_methods.

8. Plots
Average trade‑off by method.

Accuracy vs interpretability scatter.

Top configurations per method.

9. LaTeX Export
Export per‑method tables.

Export summary averages.
