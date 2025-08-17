# PYTHON-WK8-FINAL-GUIDED-PROJECT-JULY-COHORT-2025

# Filter countries of interest
countries = ['Kenya', 'United States', 'India']
df = df[df['location'].isin(countries)]

# Drop rows with missing dates/critical values
df.dropna(subset=['date', 'total_cases', 'total_deaths'], inplace=True)

# Convert date column to datetime
df['date'] = pd.to_datetime(df['date'])

# Handle missing numeric values
df['total_vaccinations'].fillna(0, inplace=True)
