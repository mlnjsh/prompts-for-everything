# Data Science Prompts

> Prompts for EDA, feature engineering, modeling, visualization, and ML pipeline development.

**Best with:** ChatGPT (Code Interpreter), Claude, Jupyter AI

---

## Exploratory Data Analysis

### 1. Initial EDA
```
I have a dataset with these columns: [list columns with types].
Rows: [approximate count].
Goal: [what I want to predict/understand].

Perform a thorough EDA:
1. Summary statistics (mean, median, std, min, max, missing %)
2. Data quality issues (missing values, duplicates, outliers, inconsistencies)
3. Distribution analysis for each numerical column
4. Cardinality check for categorical columns
5. Correlation matrix and top correlated pairs
6. Target variable analysis (distribution, class balance)
7. Initial hypotheses about relationships in the data
8. Recommended visualizations to create

Write Python code using pandas and matplotlib/seaborn.
```

### 2. Missing Data Strategy
```
My dataset has missing values in these columns:
[list columns with % missing for each]

For each column:
1. Is the missingness random (MCAR), dependent on other variables (MAR),
   or dependent on the missing value itself (MNAR)?
2. Recommended imputation strategy and WHY
3. What NOT to do (common mistakes)
4. Python code to implement the imputation

Also: At what threshold should I drop a column entirely?
When should I drop rows vs impute?
```

### 3. Outlier Detection
```
Analyze outliers in my dataset for columns: [list numerical columns].

Apply multiple detection methods:
1. Z-score method (flag |z| > 3)
2. IQR method (below Q1-1.5*IQR or above Q3+1.5*IQR)
3. Isolation Forest
4. DBSCAN-based detection
5. Visual: box plots and scatter plots

For each detected outlier group:
- Are these real outliers or data errors?
- Should I remove, cap, or keep them?
- Impact on model if kept vs removed

Write Python code for all methods.
```

## Feature Engineering

### 4. Feature Engineering Ideas
```
My prediction task: [describe target variable and goal]
Available features: [list all features with types]
Domain: [industry/domain]

Suggest 15 engineered features:
1. Mathematical transformations (log, sqrt, polynomial)
2. Interaction features (A * B, A / B)
3. Aggregation features (group-by statistics)
4. Time-based features (if applicable)
5. Encoding strategies for categoricals
6. Domain-specific features

For each feature:
- Name and formula
- Intuition (why this should help)
- Python code to create it
- Potential issues to watch for
```

### 5. Feature Selection
```
I have [N] features for a [classification/regression] task.
Model: [algorithm being used]
Dataset size: [rows]

Perform feature selection using:
1. Correlation-based filtering (remove multicollinear features)
2. Mutual information scores
3. Recursive Feature Elimination (RFE)
4. L1 (Lasso) regularization coefficients
5. Feature importance from tree-based model
6. Permutation importance

Combine results into a ranking table. Recommend the final feature set
with justification. Write complete Python code.
```

## Modeling

### 6. Model Selection Guide
```
Help me choose the right ML model:

Task: [classification / regression / clustering / anomaly detection]
Dataset size: [rows x features]
Target: [describe target, class distribution if classification]
Constraints: [interpretability needed? real-time inference? GPU available?]
Baseline: [current performance if any]

Compare 5 candidate models:
- Pros and cons of each for my specific case
- Expected performance range
- Training time estimate
- Hyperparameter tuning strategy
- When each model would be the WRONG choice

Recommend a progression: start simple, add complexity if needed.
```

### 7. Hyperparameter Tuning
```
Tune hyperparameters for [model name] on my [task type] task:

Current performance: [metric = value]
Dataset: [size and description]

Provide:
1. Which hyperparameters matter most (ranked)
2. Recommended search ranges for each
3. Grid search vs random search vs Bayesian optimization — which to use
4. Cross-validation strategy (k-fold, stratified, time-series split)
5. Complete Python code using [sklearn / optuna / hyperopt]
6. How to know when you've tuned enough

Include early stopping criteria and overfitting checks.
```

### 8. Model Evaluation
```
Evaluate my [model type] model for [task]:

Predictions: [describe what you have — probabilities, classes, continuous values]
Ground truth: [what you're comparing against]

Compute and explain:
Classification: accuracy, precision, recall, F1, AUC-ROC, confusion matrix,
classification report, precision-recall curve, calibration plot

Regression: MAE, RMSE, R², MAPE, residual plots, predicted vs actual

For each metric:
- The value
- Whether it's good/bad for my use case
- What to do to improve it specifically

Write Python code to generate all evaluations and plots.
```

## Visualization

### 9. Dashboard Design
```
Design a data dashboard for [business/purpose]:

Available data: [describe metrics and dimensions]
Audience: [who will use this — executives, analysts, operations]
Key questions: [what should the dashboard answer]

Provide:
1. Dashboard layout (describe sections and placement)
2. Chart type for each metric and why
3. Filters and interactivity needed
4. Color scheme recommendations
5. KPI cards at the top (which metrics, how calculated)
6. Python code using [plotly / streamlit / dash] to build it

Follow data visualization best practices (no pie charts for >5 categories,
use consistent color coding, minimize chart junk).
```

### 10. Publication-Ready Plot
```
Create a publication-quality plot showing [what you want to visualize].

Data: [describe or provide data]

Requirements:
- Journal/conference style (Nature / IEEE / ACM format)
- Proper axis labels with units
- Legend positioned to not obstruct data
- Font size readable at column width
- Color-blind friendly palette
- Error bars / confidence intervals if applicable
- DPI: 300+

Write Python code using matplotlib with rcParams set for publication.
Save as both PNG and PDF/SVG.
```

## ML Pipeline

### 11. End-to-End Pipeline
```
Build a complete ML pipeline for [task description]:

Data source: [where data comes from]
Target: [what to predict]
Deployment: [batch / real-time / API]

Include:
1. Data ingestion and validation
2. Preprocessing (scaling, encoding, imputation)
3. Feature engineering
4. Train/validation/test split
5. Model training with cross-validation
6. Hyperparameter tuning
7. Model evaluation and selection
8. Model serialization (joblib/pickle)
9. Prediction function for new data
10. Logging and monitoring

Write production-ready Python code using sklearn Pipeline.
Include error handling and data validation checks.
```

### 12. A/B Test Analysis
```
Analyze this A/B test:

Control group: [N users, K conversions / mean metric value]
Treatment group: [N users, K conversions / mean metric value]
Test duration: [days]
Primary metric: [what you're measuring]

Compute:
1. Conversion rate / mean for each group
2. Relative lift (%)
3. Statistical significance (p-value, confidence interval)
4. Power analysis (was the sample size sufficient?)
5. Bayesian analysis (probability that B > A)
6. Recommendation: ship, iterate, or discard

Write Python code using scipy.stats and visualization.
Flag any issues (SRM, novelty effects, multiple testing).
```

---

*30+ data science prompts for EDA, modeling, visualization, and pipelines*
