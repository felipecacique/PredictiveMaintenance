# Predictive Maintenance - Remaining useful life of mining machines

This project estimates the **remaining useful life of mining machines** by training and evaluating **machine learning models** on various **oil compound properties**. Here's a breakdown of the code and its functionality:

- Importing Libraries:
  - The code begins by importing necessary libraries such as numpy, pandas, matplotlib.pyplot, and seaborn.

- Reading Motor's Dataset:
  - Loads the dataset containing information about mining machines' oil properties (e.g., TBN, OXI, V100, etc.).
  - Displays the first few rows of the dataset to get an overview of the data.

- Defining Thresholds:
  - Sets the acceptable threshold ranges for each oil compound property. These thresholds are used to determine whether a machine is operating normally or needs maintenance.

- Plotting Data Points for Each Element of Each Motor:
  - Plots scatter plots for each oil compound property against the "Horas Oleo" (oil hours) column for each motor. This visualization provides insights into the relationship between oil properties and operating hours.

- Defining Parameters and Functions for Model Training:
  - Defines a function (generate_models_2) to generate and evaluate machine learning models for each oil compound property and different machine learning algorithms (e.g., linear regression, support vector machines).

- Automating Model Training and Evaluation:
  - Automates the process of training and evaluating models for each oil compound property and different machine learning algorithms.
  - Stores the results (MAE, estimated touch hour) in dataframes for analysis and comparison.

- Printing Results:
  - Prints the cross-validation mean absolute error (MAE), validation MAE, and estimated touch hour for each oil compound property and machine learning algorithm combination.

This code serves as an example of how to estimate the remaining useful life of mining machines using machine learning techniques and provides insights into the performance of different algorithms on predicting oil properties and failure points.
