# Project: Airport Taxi Demand Forecasting

## Project Description

In this project, I developed a model to predict the number of taxi orders in airports for the next hour. The task was provided by the company "Chetkoe Taxi," which aims to attract more drivers during peak hours by forecasting demand. The goal was to create a model that could accurately predict the number of taxi orders, ensuring the RMSE on the test set does not exceed 48.

### Research Objectives:

* Develop a model to predict the number of taxi orders in the next hour.
* Ensure the model's RMSE on the test set is no higher than 48.
* Analyze and preprocess the data to improve model performance.
* Evaluate different models and hyperparameters to find the best solution.

### Steps Taken

1. **Data Loading and Resampling**
    - Loaded the dataset from the file `/datasets/taxi.csv`.
    - Resampled the data by one hour to align with the task requirements.

2. **Data Analysis**
    - Conducted exploratory data analysis to understand trends, seasonality, and patterns in the data.
    - Visualized the data to identify potential outliers or anomalies.

3. **Model Training**
    - Trained various models with different hyperparameters to predict the number of taxi orders.
    - Split the data into training and test sets, ensuring the test set size was 10% of the original data.
    - Evaluated the performance of each model on the test set.

4. **Model Evaluation**
    - Assessed the models using the RMSE metric, ensuring it remained below the threshold of 48.
    - Compared the performance of different models and hyperparameter configurations.

5. **Conclusion**
    - Summarized the results, highlighting the best-performing model.
    - Provided recommendations for potential improvements or further research.

## Dataset Description

The dataset used in this project includes historical data on taxi orders in airports. The key feature in the dataset is:

- **num_orders**: The number of taxi orders.
