# Understanding the Job Market and Salary of Data Scientists Globally

This project provides an in-depth analysis of the job market and salary distribution for data scientists around the world. Using a dataset of 3,759 data scientist salaries, the project explores key factors influencing salary, applies various data transformations, and builds predictive models to estimate salaries based on multiple variables.

## Project Overview

The main objectives of this project are:

1. **Analyze the Distribution of Salaries**:
   - Understand the distribution of salaries and apply necessary transformations to correct skewness.
   - Perform exploratory data analysis (EDA) to identify key trends and relationships in the data.

2. **Correlation Analysis**:
   - Compute the correlation between salary and various factors such as experience level, employment type, and company size.
   - Identify the most significant variables affecting salary.

3. **Model Building**:
   - Develop multiple linear regression models to predict salary.
   - Address multicollinearity issues and refine models by selecting significant variables.
   - Evaluate model assumptions and perform residual analysis to ensure the model's accuracy.

4. **Predicting Salaries**:
   - Use the final model to predict salaries for new data points.
   - Interpret the results and provide insights into the most influential factors on salary.

## Key Findings

- The initial salary distribution was right-skewed (skewness: 1.659), which was corrected using a square root transformation (skewness reduced to 0.187).
- The final linear regression model achieved an R² value of 0.64, with variables such as experience level, salary currency, employee residence, and company size having the most significant impact on salary.
- Multicollinearity was addressed, with VIF values ranging from 1.03 to 2.46, ensuring the model's reliability.
- Residual analysis and influential point checks revealed 5 outliers that were carefully analyzed and documented.

## Project Structure

- `data/`: Contains the dataset (`ds_salaries.csv`) used for analysis.
- `scripts/`: Includes all R scripts used for data analysis, transformation, and modeling.

## Installation

To run this project locally, ensure you have R and the necessary packages installed. You can install the required packages by running:

```r
install.packages(c("ggplot2", "e1071", "car"))
```

## Usage

To replicate the analysis, follow these steps:

1. **Load the dataset**: `ds_salaries.csv`
2. **Run the exploratory data analysis (EDA)** to understand the data and visualize key relationships.
3. **Transform the data** to correct skewness and improve the normality of the salary distribution.
4. **Build regression models** using the provided scripts and refine them by removing non-significant variables.
5. **Predict salaries** for new data points and interpret the results using the final model.

## Results

- **Predicted Salaries**:
  - Experience Level 3, Salary Currency 9, Employee Residence 21, Company Size 2: **$66,911.85** (95% CI: $61,351.32 - $72,713.55)
  - Experience Level 4, Salary Currency 8, Employee Residence 33, Company Size 1: **$101,779** (95% CI: $91,537.32 - $112,563.7)
  - Experience Level 1, Salary Currency 17, Employee Residence 56, Company Size 3: **$72,779.83** (95% CI: $61,499.11 - $85,009.92)

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue.

## Acknowledgements

- The dataset used in this project was obtained from Kaggle.
- Special thanks to the R community and all the package developers.

