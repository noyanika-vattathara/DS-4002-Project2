# DS-4002-Project2
Predicting Fossil Fuel Consumption and Production. Class Project #2

## H2
This repository has 5 folders. The README.md file contains all of the information someone would need to replicate our project. The LICENSE file talks about the licensing and how to cite our project. The Scripts folder contains the code to show how we got our results. The Data file contains information about the data (Data_Overview), the original data (Table 01.01.xslx), and the final table that we use for our model (data_final). Lastly, the output file shows the output of our VARIMAX and XGBoost models. 

# Section 1
We used Google Colab (Python) for this project. The packages we installed to use our code were pandas, matplotlib, numpy, sklearn, statsmodels, and xgboost. Our project was performed on Windows laptops. 

===========================

# Section 2
```bash
├── Data
│   ├── Data_Overview.md
    ├── Table 01.01.xlsx
    ├── data_final.csv
├── LICENSE
├── Outputs
│   ├── Output.md
├── README.md
├── Scripts
│   ├── Predicting_FF_Cons/Prod.ipynb
```

# Section 3
1. The first step to reproduce our project is to download the data. The csv file is in the Data folder, "Table.01.01.xlsx"
2. Navigate to the Predicting_FF_Cons/Prod.ipynb in the Scripts folder. Open our notebook in Google Colab. Uplaod the downloaded Excel file to your Google Colab environment so it is available while running the notebook.
3. Run the notebook: execute initial cells in order for preliminary data processing. These cells will load the dataset into a dataframe, select and rename relevant columns, and converting the date column to a datetime data type.
4. Reproduce the exploratory data analysis by running the EDA cells. These will produce a line chart depicting the RE and Fossil Fuel Consumption and Production over time and a boxplot showing the distribtuions (and different scales) for the 4 variables.
5. After EDA, we trained and tested our 2 Machine Learning models (VARMAX and XGBoost) to forecast fossil fuel production and consumption based on the renewable energy trends. The VARMAX model captured temporal dependencies and cross-variable interactions. In parallel, the XGBoost model leveraged lagged renewable energy variables as features to capture nonlinear patterns and variable importance. Model performance was compared across both approaches using consistent train/test (80/20) splits and error metrics (RMSE and MAE).

6.  Model Performance should be close to:-
  VARMAX- RMSE (Production) = 0.23, MAE (Production) = 0.1693
  VARMAX- RMSE (Consumption) = 0.4952, MAE (Consumption) = 0.3896

  XGBoost- RMSE (Change in Production) = 0.2165, MAE (Change in Production) = 0.1432
  XGBoost - RMSE (Change in Consumption) = 0.3482, MAE (Change in Consumption) = 0.2556

A small variation may occur due to randomness in the train/test splitting. 

# References

[1] M. George, “Handling Missing Data in Time Series: 5 Methods,” Growth-onomics, April 2, 2025. [Online]. Available: https://growth-onomics.com/handling-missing-data-in-time-series-5-methods/. [Accessed: Oct. 17, 2025]

[2] “Data Normalization with Pandas”, GeeksforGeeks, July 23, 2025. [Online]. Available:
https://www.geeksforgeeks.org/python/data-normalization-with-pandas/. [Accessed: Oct. 17, 2025]

[3] “Common Evaluation Metrics (MAE, MSE, RMSE, MAPE)”, ApX, [Online]. Available: https://apxml.com/courses/time-series-analysis-forecasting/chapter-6-model-evaluation-selection/evaluation-metrics-mae-mse-rmse?utm_source=chatgpt.com [Accessed: Oct 24, 2025]



