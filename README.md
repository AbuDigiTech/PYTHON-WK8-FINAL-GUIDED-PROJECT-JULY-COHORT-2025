# PYTHON-WK8-FINAL-GUIDED-PROJECT-JULY-COHORT-2025

import plotly.express as px

# Prepare a dataframe with iso_code and total_cases for the latest date
latest_date = df['date'].max()
latest_df = df[df['date'] == latest_date]

# Plot a choropleth showing case density
fig = px.choropleth(latest_df, locations='iso_code', color='total_cases', hover_name='location')
fig.update_layout(title='Total Cases by Country')
fig.show()


 
