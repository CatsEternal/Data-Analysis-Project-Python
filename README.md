# Analysis of Language Isolation and Median Income in Dallas County

## Project Overview

This project analyzes the impact of language isolation on median household income in Dallas County. The data used in this project is sourced from the American Community Survey (ACS) 2019 and includes variables such as linguistically isolated households, educational attainment, and employment rates.

## Data Sources

- **American Community Survey (ACS) 2019**
- **Census Tracts Shapefile (2019)** from the U.S. Census Bureau

## Project Structure

The project is structured as follows:

- **data/**: Contains the raw and processed data files.
- **notebooks/**: Jupyter notebooks used for data analysis and visualization.
- **scripts/**: Python scripts for data processing and analysis.
- **plots/**: Generated plots and visualizations.
- **README.md**: Project overview and instructions.

## Installation

To run the project, you need to have Python installed along with the following libraries:

- pandas
- geopandas
- matplotlib
- seaborn
- statsmodels
- numpy

You can install the required libraries using `pip`:

```bash
pip install pandas geopandas matplotlib seaborn statsmodels numpy

# Data Processing

### Fetch Data
- Data is fetched from the ACS API and Census Bureau.

### Clean Data
- Data cleaning includes handling missing values and replacing erroneous data.

### Merge Data
- Data is merged with the Census Tracts shapefile for geographic analysis.

### Calculate Variables
- New variables such as percentages of linguistically isolated households and education levels are calculated.

# Analysis

### Correlation Analysis
- Correlation analysis measures the direct relationship between two variables without controlling for others. It provides a simple measure of association.

### Regression Analysis
- Regression analysis controls for multiple variables, isolating the effect of each independent variable on the dependent variable (median income). This helps in understanding the nuanced impact of each factor on median income.

# Key Findings

### Negative Impact
- **Pct_Indo_European_Linguistically_Isolated**: -5073.82, p-value = 0.000
- **Pct_Other_Languages_Linguistically_Isolated**: -3315.26, p-value = 0.014

### Positive Impact
- **Pct_Bachelors_Degree**: 1059.24, p-value = 0.000
- **Pct_Masters_Degree**: 2141.37, p-value = 0.000
- **Employment_Rate**: 509.77, p-value = 0.028

# Discrepancy between Correlation and Regression
- Correlation provides an initial understanding of relationships.
- Regression offers a detailed view by controlling for multiple variables.

# Interpretation of Results

- **Pct_Spanish_Linguistically_Isolated**: Shows a moderate negative correlation with median income. However, in the regression analysis, it has a positive coefficient but is not statistically significant (p-value 0.841). This indicates that when controlling for other factors, the direct effect of this variable on median income is not significant.
- **Pct_Indo_European_Linguistically_Isolated**: Shows a weak negative correlation and a significant negative effect in regression. This consistency suggests a robust negative impact on median income.
- **Pct_Bachelors_Degree** and **Pct_Masters_Degree**: Show strong positive correlations and significant positive effects in regression, confirming their positive impact on median income.
- **Pct_Asian_Pacific_Island_Linguistically_Isolated** and **Pct_Other_Languages_Linguistically_Isolated**: Have weak or moderate correlations and varying significance in regression, indicating their effects might be more nuanced when controlling for other factors.

# Conclusion
- Your analysis does not indicate any methodological errors, but it highlights the importance of using both correlation and regression analysis:
  - **Correlation Analysis**: Provides an initial understanding of the relationships between variables.
  - **Regression Analysis**: Offers a more detailed understanding by controlling for multiple variables simultaneously.

### Significant Findings from Regression Analysis
- **Negative Impact**: Pct_Indo_European_Linguistically_Isolated and Pct_Other_Languages_Linguistically_Isolated.
- **Positive Impact**: Pct_Bachelors_Degree, Pct_Masters_Degree, and Employment_Rate.

These results suggest that certain types of linguistic isolation negatively impact median income, while higher education levels and employment positively impact it. The correlation analysis complements this by showing overall trends, but regression provides a more nuanced view by controlling for confounding variables.
