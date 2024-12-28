# Statistical-Modeling-in-Earth-Sciences-in-R
## Exercise 1
### Statistical Analysis and Data Processing in R

This repository showcases various statistical and data analysis exercises in R, including:

- **Vector Operations:** Creating vectors, performing operations like summation.
- **Descriptive Statistics and Visualization:** Analyzing North American river lengths, calculating key statistics (e.g., mean, median, variance), and visualizing the data with histograms.
- **Gravity Data Analysis:** Importing, renaming, and visualizing measured and modeled gravity data using `ggplot2`.
- **Custom Functions:** Creating a function to compute powers (`x^y`) with demonstrations.
- **Soil Acidity Analysis:** Processing soil pH data from Canada, calculating statistical measures (range, mean, median, standard deviation, interquartile range), and visualizing the distribution with boxplots highlighting outliers.

## Exercise 2
### Earthquake Data Analysis and Linear Regression

This section of the project focuses on analyzing earthquake data in the Fiji region using the built-in `quakes` dataset. Key tasks include:

- **Visualization of Earthquake Epicenters:** Created a map of earthquake epicenters using latitude and longitude data.
- **Relationship Between Magnitude and Station Count:** Explored the relationship between earthquake magnitude and the number of recording stations using scatter plots, with added random noise for better data visualization.
- **Statistical Analysis of Magnitudes:** Calculated summary statistics (mean, median, variance, etc.) and visualized magnitudes using a boxplot. Computed covariance and correlation between magnitude and station counts.
- **Linear Regression Analysis:** Built a linear regression model to study the relationship between earthquake magnitude and station count, visualized with a regression line.
- **Model Evaluation:** Evaluated the linear regression model using key metrics such as Residual Sum of Squares (RSS), Residual Standard Error (RSE), Proximity Coefficient (φ²), and Coefficient of Determination (R²).

## Exercise 3
### Creating Statistical Models

- **Data Preparation for Statistical Modeling**  
  This section includes loading the `airquality` dataset, identifying missing values, creating a cleaned dataset by removing rows with missing data, and inspecting the structure of the cleaned dataset to ensure readiness for statistical analysis.

- **Ozone Levels Analysis by Wind Speed**  
  Visualizes ozone levels with a boxplot excluding outliers, calculates average ozone levels for different wind speeds using both the `mosaic` package and the `aggregate()` function, and displays results as a line chart with points showing averages.

- **Linear Regression Models by Month**  
  Creates linear regression models for each month where ozone levels predict temperature (converted to Celsius). Calculates and stores regression coefficients (intercept and slope) and the coefficient of determination (R²) for each model in a summarized data frame.

## Exercise 4
### Polynomial Regression Models

- **Linear Regression Model:** A simple linear regression model is built to predict parameter Y based on parameter X. Model evaluation includes calculating the Mean Squared Error (MSE), Root Mean Squared Error (RMSE), regression coefficients (intercept and slope), and the coefficient of determination (R²). The results demonstrate the model's goodness of fit, with visualizations of the regression line over the data.

- **Polynomial Regression Models:** Polynomial regression models of degrees 2 to 10 are fitted to the data. The polynomial curves are visualized alongside the measured data points to assess the models' fit. 

- **Model Metrics Comparison:** For each polynomial degree, regression coefficients, Residual Sum of Squares (RSS), and the coefficient of determination (R²) are calculated and compared. The results are summarized in a table to evaluate the performance of different polynomial models and to identify the most suitable degree for the given dataset.
