# OptiCrop: Smart Agricultural Production Optimization Engine

OptiCrop is a Flask and Machine Learning web application that recommends suitable crops using soil nutrients and environmental conditions.

## Features

- Crop recommendation using N, P, K, temperature, humidity, pH, and rainfall
- Crop suitability assessment for selected crops
- Agricultural analytics dashboard with interactive charts
- Model comparison using KNN, Logistic Regression, Decision Tree, Random Forest, and K-Means clustering
- SQLite database with users, crops, crop tips, predictions, suitability analyses, prediction history, and feedback
- Feedback form, CSV export, responsive UI, input validation, and refresh-to-home behavior

## Project Flow

1. Clean dataset and remove duplicates/missing values
2. Train and compare machine learning models
3. Save the best model as `models/crop_model.pkl`
4. Run Flask backend and render frontend pages
5. Store predictions, suitability results, history, and feedback in SQLite

## Installation

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python train_model.py
python app.py
```

Open:

```text
http://127.0.0.1:5000
```

## Dataset Columns

- `N`
- `P`
- `K`
- `temperature`
- `humidity`
- `ph`
- `rainfall`
- `label`

## API Endpoints

- `GET /api/status`
- `POST /api/predict`
- `GET /api/crops`
- `GET /api/dashboard`
- `POST /api/suitability`

