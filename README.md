# PYTHON-WK8-FINAL-GUIDED-PROJECT-JULY-COHORT-2025

Plot cumulative vaccinations over time for selected countries

Plotfigure(figsize=(10, 6))
for country in countries:
    country_df = df[df['location'] == country]
    plt.plot(country_df['date'], country_df['total_vaccinations'], label=country)
plt.title('Cumulative Vaccinations Over Time')
plt.xlabel('Date')
plt.ylabel('Total Vaccinations')
plt.legend()
plt.show()

