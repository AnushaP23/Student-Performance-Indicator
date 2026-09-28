# Student Performance Indicator

Predicts a student's **math score** from demographic and study-related features (1,000 students, 7 input features), as an end-to-end ML pipeline from raw data to a Flask web app.

## Result
**Ridge Regression: R² = 0.881** on the held-out test set (train 0.874, so no overfitting), selected from 8 regressors.

| Model | Test R² |
|---|---|
| Ridge | **0.881** |
| Linear Regression | 0.880 |
| Random Forest | 0.847 |
| XGBoost | 0.828 |
| Lasso | 0.825 |
| KNN | 0.784 |
| Decision Tree | 0.767 |

**Takeaway:** the linear models beat the tree ensembles. The relationship is close to linear, so extra model complexity added nothing. Simple baselines first.

## Pipeline
`data ingestion → transformation (OneHotEncoder + StandardScaler) → model training & selection → Flask app`

- `src/components/`: ingestion, transformation, trainer
- `src/pipeline/`: prediction pipeline used by the app
- `notebook/`: EDA and model experiments
- `.ebextensions/`: AWS Elastic Beanstalk deployment config

## Run locally
    pip install -r requirements.txt
    python app.py

*Built in 2024 while learning to structure ML projects as packages rather than single notebooks.*
