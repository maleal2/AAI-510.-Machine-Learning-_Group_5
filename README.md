# Developing a Machine Learning Model to Assist Home Credit Services in Loan Decisions for Unbanked Populations
Final Project Group 5: Developing a Machine Learning Model to Assist Home Credit Services in Loan Decisions for Unbanked Populations - USD

#  Dataset. 
This project is a part of the AAI-510 course in the Applied Artificial Intelligence Program at the University of San Diego (USD). 
Project Status: [Completed]

## Installation
To use this project, first clone the repo on your device using the below command:
git clone [https://github.com/maleal2/Fitness_Tracker_wearable_device_project_Group_1](https://github.com/maleal2/AAI-510.-Machine-Learning-_Group_5.git)

## Project Introduction
  
  This code presents the design and implementation of a machine learning model aimed at assisting Home Credit Services in making loan decisions for unbanked populations. The data includes current loan applications and previous bureau records provided by Home Credit. The current loan application data contains valuable information such as annual income, total loan amount, date of birth, type of work, type of education, living and working locations, and more. The bureau data represents external financial information where the same applicants have also applied for loans.

First, we start with data importation and inspection of both datasets, confirming the highly uneven distribution of the target variable (0 and 1). There are more data points for 0 (repayable loans) than for 1 (non-repayable loans).

Next, we proceed to calculate new features derived from the bureau dataset. These new features include the mean, median, maximum, and minimum values for data such as credit amount, annual income, type of credit, credit account status, and others. This step ensures we do not discard potentially meaningful data that could improve the model's predictions.

After generating new features, we calculate the correlation of these new variables with the "TARGET" variable. The results are saved in a dataset called train_data_agg_new. We then identify and remove highly correlated variables to prevent overfitting, saving the results in a variable called cols_to_remove. This step is crucial as using highly correlated variables can lead to biased predictions.

Finally, we integrate the original train_data dataset with train_data_agg_new, obtained from the aggregated statistics of the bureau data. We apply the Light Gradient Boosting Machine (LightGBM) as Model 1, utilizing One-Hot Encoding and cubic interpolation for data processing, and employ cross-validation to handle the high-dimensional scenario. We present the results and conclusions from this model. For comparison, we also train Model 2 using the dataset with all highly correlated features to evaluate its performance.

## Contributors

1. Maria Leal Cardenas
2. Mayank Bhatt
3. Vanessa Dyan Laxamana

## Methods Used

1. Basic Data cleaning inspection.
2. Light Boost Machine Learning. 
3. Cross-Validation technique.
4. Cubic interpolation.
5. One Hot Encoding.
6. KDE Density Estimate Plots Function.

## Technologies
   Python

## Project Description

•	Source of the datasets: https://www.kaggle.com/competitions/home-credit-default-risk

•	Dataset: train_data.csv

•	Number of datapoints: 153,755

•	Number of variables: 122

•	Dataset: bureau_data.csv

•	Number of datapoints: 733,097

•	Number of variables: 17

Number of variables: 18

Size of the dataset:  943


## Acknowledgments
Thank you Professor Wesley Pasfield for all your support during this class. 


