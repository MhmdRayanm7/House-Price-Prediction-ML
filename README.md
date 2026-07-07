# House Price Prediction using Machine Learning

This project analyzes a house price dataset and builds machine learning models to predict whether a house belongs to a low-price or high-price category.

## Project Goal

The goal of this project is to study how house features such as living area, number of bathrooms, number of bedrooms, floors, view, and condition affect the price level of a house.

The original problem is a regression problem because the `price` column contains continuous numeric values.

For this project, the problem was converted into a classification problem by creating a new target column called `Price_Level`.

- `0` = Low price
- `1` = High price

## Dataset

The dataset file is stored in:

`data/data_House.csv`

Each row represents one house, and each column represents a house feature.

The following columns were removed because they were not used in the model:

- `date`
- `street`
- `city`
- `statezip`
- `country`

## Project Structure

```text
House-Price-Prediction-ML/
├── assets/
│   ├── cover.png
│   └── Handasim.png
├── data/
│   └── data_House.csv
├── notebooks/
│   └── House_Price_Project.ipynb
├── reports/
├── README.md
├── requirements.txt
└── .gitignore
```

## Main Steps

1. Data loading
2. Data description
3. Exploratory Data Analysis
4. Data visualization
5. Data cleaning
6. Feature engineering
7. Data correlation
8. Train and test split
9. Data normalization
10. KNN model training and evaluation
11. ANN model training and evaluation
12. Model comparison
13. Final conclusions and reflection

## Models Used

### KNN

The KNN model was trained using different values of `K`, and the best value was selected according to the test accuracy.

The model was evaluated using:

- Accuracy
- Confusion Matrix
- Classification Report
- Precision
- Recall
- F1-score

### ANN

The ANN model was implemented using `MLPClassifier` from Scikit-learn.

The model was evaluated using:

- Accuracy
- Loss curve
- Validation accuracy
- Classification Report

## How to Run the Project

1. Clone the repository:

```bash
git clone https://github.com/MhmdRayanM7/House-Price-Prediction-ML.git
```

2. Open the project folder:

```bash
cd House-Price-Prediction-ML
```

3. Create a virtual environment:

```bash
python -m venv .venv
```

4. Activate the virtual environment:

For Git Bash on Windows:

```bash
source .venv/Scripts/activate
```

For PowerShell on Windows:

```powershell
.venv\Scripts\Activate
```

5. Install the required libraries:

```bash
python -m pip install -r requirements.txt
```

6. Open the notebook:

```text
notebooks/House_Price_Project.ipynb
```

7. Run all cells.

## Requirements

The main libraries used in this project are:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- notebook
- ipykernel

## Conclusion

The project shows that physical house features such as living area, number of bathrooms, number of bedrooms, and house condition can help predict whether a house belongs to a low-price or high-price category.

Both KNN and ANN models were trained and evaluated, and their results were compared using accuracy and other performance metrics.
