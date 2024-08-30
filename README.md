# Building-a-demand-forecasting-model-using-PySpark
Predict e-commerce product demand using PySpark to answer business questions regarding supply chain efficiency.

# Project Overview
This project aims to analyze the sales data from the `Online Retail.csv` dataset and build a forecasting model to predict the 'Quantity' of products sold. Utilizing `PySpark`, the project efficiently processes large-scale data, making it scalable for distributed computing environments. The model is evaluated based on the Mean Absolute Error (MAE) on a test set, and specific quantities are predicted for particular weeks in 2011.

# Files
* `notebook.ipynb`: The Jupyter notebook contains all code for data processing, model training, evaluation, and prediction.
* `Online Retail.csv`: The dataset used for analysis and forecasting (not provided here).

# Key Steps
1. Data Splitting
The data is split into training and test sets based on the date "2011-09-25".
  * All data up to and including this date forms the training set.
  * Data after this date forms the test set.

2. Data Preprocessing
The following steps are performed:
  * Extracted relevant columns: "Country", "StockCode", "InvoiceDate", and "Quantity".
  * Derived additional features such as "Year", "Month", "Day", "Week", and "DayOfWeek".
3. Forecasting Model
  * A time series forecasting model was built using the training data to predict future quantities sold.
  * The model's performance was evaluated using the MAE metric on the test set.
4. Evaluation
  * The Mean Absolute Error (MAE) for the forecast on the test set was calculated.
5. Quantity Prediction
  * Predicted the total quantity of products expected to be sold during Week 39 of 2011.

# Results
* Mean Absolute Error (MAE): 9.04
* Quantity sold during Week 39 of 2011: 86,239 units

# Requirements
The following Python packages are required to run the notebook:
* pandas
* pyspark (if using a Spark environment for distributed processing)

# Usage
* Clone the repository.
* Place the "Online Retail.csv" dataset in the same directory as the notebook.
* Run the notebook (notebook.ipynb) to replicate the analysis and model building process.
* Review the output cells to see the model performance and predictions.

# Conclusion
This project successfully demonstrates how to build a time series forecasting model to predict sales quantities and evaluate performance. The use of `PySpark` enabled efficient handling and processing of the large dataset, ensuring scalability and performance in a distributed computing environment. The model can be further tuned or expanded to predict other metrics, handle more complex datasets, or be deployed in a real-time forecasting system.
