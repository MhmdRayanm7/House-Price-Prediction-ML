# House Price Prediction ML

A simple machine learning project that predicts if a house is in a low price group or a high price group.

The project uses a house dataset, cleans it, explores the data, creates graphs, and trains two models:

- KNN
- ANN

## Project Question

Can we predict if a house is low price or high price based on physical house features?

Examples of features:

- bedrooms
- bathrooms
- living area
- lot area
- floors
- view
- condition
- year built

## Dataset

The dataset file is:

```text
data/data_House.csv
```

The original dataset has 4600 rows and 18 columns.

Each row represents one house.

## Data Cleaning

In this project, I removed columns that I did not use in the model:

- date
- street
- city
- statezip
- country

I also removed rows where the price was 0, because a house price cannot logically be 0.

After that, I created a new target column called:

```text
Price_Level
```

The target column was created using the median price:

- 0 = low price
- 1 = high price

After creating `Price_Level`, I removed the original `price` column so the model would not get the real answer directly.

## Project Steps

1. Load the dataset
2. Describe the columns
3. Check the data
4. Show descriptive statistics
5. Clean the data
6. Create `Price_Level`
7. Make graphs
8. Check correlation
9. Split the data into train and test
10. Normalize the data
11. Train KNN
12. Train ANN
13. Compare the results
14. Write conclusions and reflection

## Models

### KNN

KNN was trained with different values of K.

The best K was selected using test accuracy.

The model was evaluated with:

- accuracy
- confusion matrix
- classification report
- precision
- recall
- f1-score

### ANN

The ANN model was built using TensorFlow and Keras.

The model has:

- Dense layer with 64 neurons
- Dense layer with 32 neurons
- Output layer with 2 neurons

The ANN was evaluated using:

- accuracy
- loss
- classification report

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
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/MhmdRayanM7/House-Price-Prediction-ML.git
```

2. Open the folder:

```bash
cd House-Price-Prediction-ML
```

3. Create a virtual environment:

```bash
python -m venv .venv
```

4. Activate the virtual environment.

Git Bash:

```bash
source .venv/Scripts/activate
```

PowerShell:

```powershell
.venv\Scripts\Activate
```

5. Install the libraries:

```bash
python -m pip install -r requirements.txt
```

6. Open the notebook:

```text
notebooks/House_Price_Project.ipynb
```

7. Run all cells.

## Requirements

Main libraries used:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- tensorflow
- notebook
- ipykernel

## Conclusion

The project shows that house features like living area, number of bathrooms, number of bedrooms, and house size can help predict if a house is in a low price group or high price group.

The ANN model gave a slightly better result than KNN in this project.
