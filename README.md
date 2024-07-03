### About the Dataset

The PJM Hourly Energy Consumption Data is sourced from PJM Interconnection LLC, a regional transmission organization operating in the Eastern Interconnection grid. The dataset provides hourly power consumption data in megawatts (MW) across various regions served by PJM.


### Steps
### Data Import and Inspection:

- Import necessary packages (matplotlib, pandas, plotly, seaborn).
- Load the dataset containing hourly energy consumption data (AEP_hourly.csv).
- Display the first few rows, check data shape, and examine data types.

### Data Wrangling:

- Convert Datetime column to datetime format and set it as the index for time series analysis.
- Resample hourly data to daily averages, handling missing values by forward filling.

### Exploratory Data Analysis (EDA):

- Visualize the daily power consumption time series using matplotlib.
- Analyze weekly rolling averages to identify trends and seasonality.
- Review the distribution of daily power consumption using box plots.

### Regression Model Setup:

- Create lag variables (AEP_MW_1) to capture temporal dependencies.
- Drop NA values and compute correlations between features using seaborn's heatmap.

### Model Building:

- Split the data into feature matrix (X) and target vector (y).
- Partition the dataset into training and testing sets using an 80% training boundary.
- Calculate the mean absolute error (MAE) for a baseline model predicting the mean of y_train.
- Instantiate and fit a LinearRegression model using scikit-learn.
- Evaluate model performance using MAE for both training and testing data.

### Model Interpretation and Prediction:

- Extract and interpret model coefficients and intercept.
- Predict y_test values using trained model and visualize predictions against actual values using plotly (px.line).
