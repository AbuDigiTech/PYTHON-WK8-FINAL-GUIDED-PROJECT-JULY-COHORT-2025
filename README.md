# PYTHON-WK8-FINAL-GUIDED-PROJECT-JULY-COHORT-2025

import pandas as pd

# Load the dataset
df = pd.read_csv('owid-covid-data.csv')

# Preview the first few rows
print(df.head())

# Check columns
print(df.columns)

# Identify missing values
print(df.isnull().sum())

