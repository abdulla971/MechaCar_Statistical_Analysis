# MechaCar_Statistical_Analysis

## Overview
Statistical analysis is conducted to identify key variables that predict the mpg of a new prototype; the following summary statistics were used: multiple linear regression metrics, p-value, r-squared value and T-tests.

### Purpose
The purpose of this project is to:
* Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
* Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
* Run t-tests to determine if the manufacturing lots are statistically different from the mean population
* Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## Analysis
Data Source: 
* [MechaCar MPG Data Set](Resources/MechaCar_mpg.csv)
* [MechaCar Suspension Coil Data Set](Resources/Suspension_Coil.csv)

Software used: R, R dplyr library, RStudio
Analysis Code: [MechaCar Challenge](MechaCarChallenge.R)

## Results

## Using linear Regression to Predict the MPG

After loading the miles per gallon dataset, multiple linear regression linear regression operations were performed to check if it could predict the miles per gallon (mpg) dependent variable by using the vehicle length, vehicle weight, spoiler angle, ground clearance, and all wheel drive (AWD) independent variables. This was done to find the answers to the following questions:

1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
2. Is the slope of the linear model considered to be zero? Why or why not?
3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

The questions answers are:

1. Two variables gave a non-random amount of variance; the vehicle length and the ground_clearance. They both got small p-value which means they had a high level of significance. The other observation is that the the intercept also had a high significance which means we must examine other factors that might contribute to the variance in mpg.

2. The slope of the linear module is not zero, this is due to the fact that some independent variables had a significant effect on the dependent variable. If the case is different and none of the independent variables had an effect then the slope would be zero for the linear regression.

3. The most important indicator to check if the linear model predicts the mpg is the r-squared value. In our case it is at 0.7149 mean that out of 100 instances, therefore this means that the model will have correct prediction 71 times; which means that the model is considered effective.

Here are the summary results from the linear regression.

### Miles Per Gallon Linear Regression

![mpg_linear_regression](https://github.com/Wall-E28/mecha_car_statistical_analysis/blob/main/visualizations/mpg_linear_regression.png)

## Summary Statistics on Suspension Coils


After loading the suspension coils dataset; the data was comprised of 150 different vehicles ID, 3 different lot numbers, and corresponding PSI levels for each vehicle. I created two summary tables to determine the mean, median, variance, and standard deviation of the data. The first table was the general data, while the second table covered the specific three lots. These are the two tables:

