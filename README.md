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

### Total Summary Table

![total_sum_sus_coils](https://github.com/Wall-E28/mecha_car_statistical_analysis/blob/main/visualizations/total_sum_sus_coils.png)

### Lot Summary Table

![lot_sum_sus_coils](https://github.com/Wall-E28/mecha_car_statistical_analysis/blob/main/visualizations/lot_sum_sus_coils.png)


After completing this analysis I was able to answer the following question:

1. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

And this is the answer I found:

1. Examining the summary, the current variance is approximately 76.23 PSI which indicates that it does meet the design specification. And, by examining the lot variance, the first two lots pass the design specification with a variance of approximately 1.14 PSI and 10.13 PSI respectfully. However the third lot does not meet the specifications, as an approximately 220.01 PSI variance which exceeds the design specification by more than the double allocated amount. Therefore the team should focus and work with cars from lots 1 and 2, and ignore 3.

## T-Tests on Suspension Coils


I examined if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 PSI. To do this R's t.test() function were used to find four different p-values.

I did this to answer the following question:

1. Do any of the four groups have a statistically different mean from the population mena of 1,500 PSI?


The answer I found:

1. Using 95% significance level, which means that 95% of the time this tests results would be true, after running the tests to check if there is a statistical difference from the mean of 1,500 PSI all four p-values where much greater than .05 which means I would reject that there is a statistical difference between the four groups and the population mean.


Here is a breakdown of each of the four tests:

### All Three Lots Combined Test

![total_pop_test](https://github.com/Wall-E28/mecha_car_statistical_analysis/blob/main/visualizations/total_pop_test.png)

### Lot 1 Test

![1_pop_test](https://github.com/Wall-E28/mecha_car_statistical_analysis/blob/main/visualizations/1_pop_test.png)

### Lot 2 Test

![2_pop_test](https://github.com/Wall-E28/mecha_car_statistical_analysis/blob/main/visualizations/2_pop_test.png)

### Lot 3 Test

![3_pop_test](https://github.com/Wall-E28/mecha_car_statistical_analysis/blob/main/visualizations/3_pop_test.png)

## Summary
A statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

### Study Design: MechaCar vs Competition

### Metric to Measure

Thinking with a consumer mindset, the city and highway fuel efficiency is of high interest. The companies in competition are pushing to bring diesel like fuel efficiency to gasoline engines. To have a chance MechaCar is going to have to join in the competition to improve the fuel efficiency. To determine how MechaCar performs against competition, we can determine if a correlation exists between the type of automatic transmission and fuel efficiency. 

### Hypothesis

    * Null Hypothesis: The mean of fuel efficiencies for the different types of automatic transmission is the same across all types. 

    * Alternative Hypothesis: The mean of fuel efficiencies for the different types of automatic transmission is not the same across all types. 

### Statistical Test

A one-way ANOVA is used to test the means of a single continuous dependent variable across a single independent variable with multiple groups, similar to categorical data. In this analysis our independent variable is the type of automatic transmission, which is categorical data type and our dependent variable is fuel efficiency, which is a numerical and continuous data type.

### Data Required

Data on cars with different types of automatic transmission engines is required to run the test.

In a perfect example, other factors that might impact fuel efficiency should be ignored. This is however not the case as in real life we don’t have ideal conditions and assuming that would be wrong, multiple statistical tests would be required to find the "sweet spot" that determines which type of transmission delivers the best fuel efficiency, factors such as ground clearance and drive type etc.
