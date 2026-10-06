# Freight Rate Prediction Challenge

See `Freight_Rate_ML_Assessment.pdf` for the assessment instructions.

## Task

1. Train and validate your model using `data/train_test.csv`.
2. Predict every load in `data/validation.csv`. Each load has a unique `load_id`.
3. Fill the matching `predicted_rate` values in `data/validation_predictions_template.csv` and save it as `validation_predictions.csv`.
4. Predict every row in `data/december_chart_inputs.csv` by filling its `predicted_rate` column.
5. The scorer validates both files and creates `scorer_results/candidate_december.png`.

## Launch

### 1. Create and activate the virtual environment

From the project root:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 2. Install dependencies
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 3. Pipeline (`pipeline.ipynb`)

Notebook containing the full solution pipeline: data loading and cleaning, feature engineering, validation, model training, and prediction generation.

### How to run
Activate the venv, install dependencies from `requirements.txt`, open `pipeline.ipynb`, and Run All.

### 3. Make final report

```bash
python3 score.py --predictions validation_predictions.csv --december-predictions data/december_chart_inputs.csv
```
