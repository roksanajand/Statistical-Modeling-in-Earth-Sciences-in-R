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

## Exercise 5
### Multiple Linear Regression for Air Temperature Prediction

This task analyzes air pollution data to build a multiple linear regression model predicting air temperature (TEMP) using atmospheric aerosol concentrations. The steps include:

- **Data Preparation**: Missing rows are removed, and only relevant variables (SO2, NO2, CO, O3, and TEMP) are retained. Highly correlated variables (PM2.5 and PM10) are excluded based on the correlation matrix.
- **Linear Regression Model**: A linear regression model is created to evaluate the influence of SO2, NO2, CO, and O3 on air temperature. The model coefficients, Residual Sum of Squares (RSS), Residual Standard Error (RSE), and R-squared (R²) values are calculated to assess the model's fit.
- **Temperature Prediction**: The model predicts air temperature based on hypothetical pollutant concentrations, resulting in a temperature of **16.53°C**.

## Exercise 6
### Variable Selection and Correlation Analysis for Rainfall Prediction
This task focuses on refining the dataset for predictive modeling of average annual rainfall by filtering variables with a correlation coefficient |r| ≥ 0.5 relative to the target variable (MEAN.ANNUAL.RAINFALL). Variables meeting the threshold are selected for further analysis. A pairwise scatter plot matrix is then generated using the ggpairs() function to visually explore relationships among the selected variables, providing insights into potential predictors for the regression model.

## Exercise 7

### Baseline Model for Annual Rainfall Prediction
A baseline model was created to predict mean annual rainfall without any explanatory variables. It predicts the same average value for all observations. The Root Mean Square Error (RMSE) for the training set was calculated as 237.87, and for the testing set as 216.24.

### Linear Regression Model Using Correlation
A linear regression model was created using the variable with the highest Pearson correlation (approximately 0.76) relative to mean annual rainfall. The RMSE for this model was 154.72 on the training set and 289.46 on the testing set.

### Linear Regression Model Using Maximum Rainfall
A linear regression model was built using `MAX.RAINFALL` as the explanatory variable. The RMSE for this model was 112.22 on the training set and 133.90 on the testing set.

### Multiple Linear Regression Model
A multiple linear regression model was constructed using `ALTITUDE`, `MAX.RAINFALL`, and `MEAN.ANNUAL.AIR.TEMP` as explanatory variables. The R² value was 0.795, indicating that 79.5% of the variance in mean annual rainfall was explained by the model. The RMSE for this model was 107.61 on the training set and 130.76 on the testing set.

### RMSE Comparison Across Models
An RMSE comparison was visualized for all models across training and testing sets. The multiple regression model performed the best, achieving the lowest RMSE values in both training and testing datasets.


## Exercise 8
 Stepwise Selection and Model Evaluation for Annual Rainfall Prediction

### Description:
This task involves building and evaluating regression models for predicting mean annual rainfall using stepwise selection methods. The following steps are performed:

1. **Nonlinear Models**:  
   Models are created to predict mean annual rainfall using features derived from altitude and maximum rainfall. Polynomial transformations (logarithm and squared terms) of these features are used to capture non-linear relationships. The RMSE (Root Mean Square Error) is calculated to assess the model fit for both the training and test datasets.

2. **Forward Selection**:  
   The forward selection method is applied using the `step()` function with the AIC (Akaike Information Criterion) as the selection criterion. A baseline model is created, and additional variables (ALTITUDE, MAX.RAINFALL, MEAN.CLOUD.COVER, and MEAN.ANNUAL.AIR.TEMP) are added iteratively. The model's summary, including the coefficients and AIC values, is displayed, and the final model is evaluated for RMSE on both training and test datasets.

3. **Backward Selection**:  
   Backward selection is applied to reduce the model by removing variables with the least significant impact on the dependent variable (mean annual rainfall). The AIC is used again for model selection, and the final model is tested for accuracy using the RMSE metric on the test dataset.

