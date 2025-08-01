# Pipelines

This directory contains Jupyter notebooks demonstrating end-to-end machine learning workflows using scikit-learn pipelines, plus a `models/` subfolder for serialized pipeline objects.

## Contents

### models/
Serialized pipeline and model artifacts produced by the notebooks (e.g., `.pkl` files). Use these for inference without re-training.

### predict_using_pipeline1.ipynb
Builds a scikit-learn pipeline (Pipeline 1) that chains preprocessing steps (e.g., imputation, scaling, encoding) with a classifier. Trains the pipeline on the Titanic dataset and shows how to call `pipeline.predict()` for new data.

### predict_using_pipeline2.ipynb
Demonstrates a second pipeline variant (Pipeline 2) with alternate preprocessing (e.g., feature engineering using `ColumnTransformer`) and a different classifier. Includes comparison of performance to Pipeline 1.

### predict_without_pipeline2.ipynb
Implements the same preprocessing and modeling steps as in Pipeline 2 manually—without using `Pipeline`—to highlight the convenience and reproducibility benefits of pipeline abstractions.

### titanic_without_using_pipeline1.ipynb
Mirrors the workflow of `predict_using_pipeline1.ipynb` but performs each preprocessing and modeling step manually for educational purposes.

## Notes

- The notebooks use the Titanic dataset for classification tasks.
- All preprocessing and model training is reproducible via scikit-learn’s `Pipeline` and `ColumnTransformer`.
- Compare manual vs. pipeline-based workflows to appreciate code modularity and maintainability.
