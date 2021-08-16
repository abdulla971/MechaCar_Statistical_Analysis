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
