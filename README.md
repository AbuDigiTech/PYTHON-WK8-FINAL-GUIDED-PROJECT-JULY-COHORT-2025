# PYTHON-WK8-FINAL-GUIDED-PROJECT-JULY-COHORT-2025

import matplotlib.pyplot as plt
import seaborn as sns

# Plot total cases over time for selected countries
plt.figure(figsize=(10, 6))
for country in countries:
    country_df = df[df['location'] == country]
    plt.plot(country_df['date'], country_df['total_cases'], label=country)
plt.title('Total Cases Over Time')
plt.xlabel('Date')
plt.ylabel('Total Cases')
plt.legend()
plt.show()

# Plot total deaths over time
plt.figure(figsize=(10, 6))
for country in countries:
    country_df = df[df['location'] == country]
    plt.plot(country_df['date'], country_df['total_deaths'], label=country)
plt.title('Total Deaths Over Time')
plt.xlabel('Date')
plt.ylabel('Total Deaths')
plt.legend()
plt.show()

# Calculate death rate
df['death_rate'] = df['total_deaths'] / df['total_cases']
