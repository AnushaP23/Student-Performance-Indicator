# Student Performance Indicator

Predicts a student's **[math score]** from demographic and study-related features, as an end-to-end ML pipeline from raw data to a deployed web app.

## Result
Best model: **[e.g. Linear Regression / CatBoost]**, R² = **[0.xx]** on the held-out test set, compared against [N] other regressors.

## Pipeline
`data ingestion → transformation (encoding, scaling) → model training & selection → Flask app`

- `src/components/`: ingestion, transformation, trainer
- `src/pipeline/`: prediction pipeline used by the app
- `notebook/`: EDA and model experiments
- `.ebextensions/`: AWS Elastic Beanstalk deployment config

## Run locally
    pip install -r requirements.txt
    python app.py

## What I learned
- [one honest line, e.g. "structuring an ML project as a package instead of one notebook"]
- [one more]

**Dataset:** [name + link]
