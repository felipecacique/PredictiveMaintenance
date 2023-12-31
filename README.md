# Predictive Maintenance - Remaining Useful Life of Mining Machines

## A brief overview 

This work focuses on the application of machine learning in the analysis of engine oil degradation data with the goal of predicting the optimal time for oil replacement. The study aims to assess the feasibility of extending oil change intervals by considering the actual properties of lubricants and their degradation limits, rather than relying solely on manufacturer-recommended operating hours. This approach could lead to reduced maintenance costs, improved asset productivity, and reduced environmental impact due to fewer oil changes.

The study emphasizes the use of data analysis and data science techniques to achieve these goals. The authors collected and analyzed oil samples from two mining equipment engines, TE8037 and TE8038. They monitored various oil properties such as viscosity, total base number (TBN), oxidation, soot content, sulfation, and nitration over time to assess oil degradation. By studying these parameters, they aimed to predict the optimal time for oil replacement and determine if the engines could operate effectively beyond the manufacturer-recommended intervals.

Machine learning, particularly Support Vector Regression (SVR), was employed to model the degradation patterns of these parameters. The authors compared the performance of linear and polynomial models in predicting the parameter values over time. They used the Mean Absolute Error (MAE) as a metric to evaluate the accuracy of their models.

To serve as an example, the image below shows the training and testing samples for the element TBN of the TE8038 motor, and the projection line using the SVR. The critical point for oil replacement, in this case, would be in 729 hours, which is the intersection point between the projection line and the degradation limit (threshold).

<img src="https://github.com/felipecacique/PredictiveMaintenance/blob/main/graphs/motor_TE8038__carga_32__element_TBN__model_svm_linear__train_size_20__valid_size_14.png" />

Key findings and conclusions of the study include:

- Benefits of Extended Oil Change Intervals: The study demonstrates the potential to extend oil change intervals by up to 50% without compromising engine performance. This extension could lead to increased availability, reduced maintenance costs, and decreased environmental impact.

- Importance of Parameter Monitoring: Monitoring oil parameters such as viscosity, TBN, oxidation, and others provides insights into the health of the engine and the state of the lubricant. These parameters can be used to predict the optimal time for oil replacement.

- Machine Learning for Predictive Analysis: Machine learning models, particularly SVR, can accurately predict the degradation patterns of various oil parameters. Linear models generally showed better adherence to the data compared to polynomial models.

- Application of Data Science: The study demonstrates how data analysis and data science techniques can support decision-making in the context of oil management, replacement, and degradation monitoring. These techniques provide insights that aid in optimizing fleet performance and minimizing environmental impact.

In summary, the work emphasizes the use of machine learning and data analysis to predict the optimal time for engine oil replacement. By monitoring various oil parameters and employing SVR models, the authors demonstrate the feasibility of extending oil change intervals while maintaining engine performance and minimizing environmental consequences.


## Code details

This project estimates the **remaining useful life of mining machines** by training and evaluating **machine learning models** on various **oil compound properties**. Here's a breakdown of the [code](https://github.com/felipecacique/PredictiveMaintenance/blob/main/remaining_useful_life.ipynb) and its functionality:

- Importing Libraries:
  - The code begins by importing necessary libraries such as **numpy**, **pandas**, **matplotlib.pyplot**, and **seaborn**.

- Reading Motor's Dataset:
  - Loads the dataset containing information about **mining machines' oil properties** (e.g., TBN, OXI, V100, etc.).
  - Displays the first few rows of the dataset to get an overview of the data.

- Defining Thresholds:
  - Sets the **acceptable threshold ranges** for each oil compound property. These thresholds are used to determine whether a machine is operating normally or needs maintenance.

- Plotting Data Points for Each Element of Each Motor:
  - Plots scatter plots for each oil compound property against the "Horas Oleo" (oil hours) column for each motor. This visualization provides **insights** into the relationship between oil properties and operating hours.

- Defining Parameters and Functions for Model Training:
  - Defines a function (generate_models_2) to generate and evaluate **machine learning models** for each oil compound property and different machine learning algorithms (e.g., linear regression, support vector machines).

- Automating Model Training and Evaluation:
  - Automates the process of training and evaluating models for each oil compound property and different machine learning algorithms.
  - Stores the results (MAE, estimated maintenance hour) in dataframes for analysis and comparison.

- Printing Results:
  - Prints the **cross-validation mean absolute error (MAE)**, **validation MAE**, and **estimated maintenance hour for each oil compound property and machine learning algorithm combination**.

This code serves as an example of **how to estimate the remaining useful life** of mining machines using machine learning techniques and provides insights into the **performance of different algorithms on predicting failure points**.


This code was written in partnership with **Cid Clay Quirino** and **Felipe Duarte Pedra**, for the purpose of contributing to a **[paper](https://github.com/felipecacique/PredictiveMaintenance/blob/main/MACHINE%20LEARNING%20NA%20PREVIS%C3%83O%20DE%20HORAS%20DE%20SUBSTITUI%C3%87%C3%83O%20DE%20%C3%93LEO%20DO%20MOTOR%20-%20FOCO%20EM%20IMPACTO%20AMBIENTAL.pdf)** entitled **"MACHINE LEARNING NA PREVISÃO DE HORAS DE SUBSTITUIÇÃO DE ÓLEO DO MOTOR_ FOCO EM IMPACTO AMBIENTAL"**. The **paper was published** in the **36º Brazilian Maintenance Congress** in 2021.

