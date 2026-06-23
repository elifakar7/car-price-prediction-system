# Car Price Prediction System

A machine learning project that predicts used car selling prices based on features such as brand, manufacturing year, kilometers driven, and fuel type. Multiple regression models are trained and compared to find the best performer.

Dataset: [Car Price Dataset (Kaggle)](https://www.kaggle.com/code/mahmoudredagamail/car-price-dataset)

## Features

- Exploratory data analysis with summary statistics, heatmaps, boxplots, and a word cloud
- Feature engineering: brand extraction from car name, one-hot encoding, and feature scaling
- Hyperparameter tuning with GridSearchCV for each model
- Model comparison using MAE, RMSE, and R²

## Technologies

| Technology | Purpose |
|---|---|
| pandas / numpy | Data loading and manipulation |
| matplotlib / seaborn / wordcloud | Data visualization |
| scikit-learn | Preprocessing, model training, and evaluation |

## Models

| Model | Test MAE | Test RMSE | Test R² |
|---|---|---|---|
| Random Forest Regressor | 0.587 | 0.870 | 0.967 |
| Linear Regression | see notebook output | see notebook output | see notebook output |
| MLP Regressor | see notebook output | see notebook output | see notebook output |

Best Random Forest parameters: `max_depth=10`, `min_samples_split=2`, `n_estimators=100`.

## Project Structure

```text
.
├── carpricepredictionsfinal.ipynb   # Main notebook: EDA, preprocessing, modeling
├── car data.csv                      # Dataset (download from Kaggle, not included)
└── README.md
```

## Installation

### 1. Clone the repository
```bash
git clone <repo-url>
cd <repo-folder>
```

### 2. Create a virtual environment (recommended)
```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install pandas numpy scikit-learn matplotlib seaborn wordcloud tabulate scipy jupyter
```

### 4. Download the dataset
Download `car data.csv` from the [Kaggle dataset page](https://www.kaggle.com/code/mahmoudredagamail/car-price-dataset) and place it in the project folder, then update the file path in the notebook to match its location.

## Usage

```bash
jupyter notebook carpricepredictionsfinal.ipynb
```

Run the cells in order to:
1. Load and clean the dataset
2. Explore the data through visualizations
3. Engineer features (brand extraction, encoding, scaling)
4. Train and tune Random Forest, Linear Regression, and MLP Regressor models
5. Compare model performance and visualize predictions vs. actual prices

## Notes

- The dataset file path in the notebook is currently a local absolute path and should be updated before running.
- Results may vary slightly depending on the train/test split and random seed.
