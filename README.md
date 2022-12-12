# MechaCar_Statistical_Analysis

## Overview
The purpose of this analysis was to use R to compute various statistical analyses based on car data for "AutoRUs." The goal of this project is to perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes, collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots, run t-tests to determine if the manufacturing lots are statistically different from the mean population, and design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.

## Linear Regression to Predict MPG
<img width="638" alt="Screen Shot 2022-12-11 at 8 14 19 PM" src="https://user-images.githubusercontent.com/107594280/206959302-1371ccc0-041b-4e34-9af5-bdb6ccdd8a94.png">

### Summary

1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

The variables that provided a non-random amount of variance to the values are vehicle length and ground clearance. As we can see from the Pr(>|t|) values, both variables have p-values of 2.6x10-12 and 5.21x10-8, respectively. Therefore, there are deemed have a significant impact on the data, especially in comparison to the other variables.

2. Is the slope of the linear model considered to be zero? Why or why not?

The slope of the linear model is not considered to be zero due to the the p-values of not only the variables but the overall model, which stands at 5.35e-11. Since this is smaller than our significance level of .05%, we would reject our null hypothesis.

3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

This linear model does predict mpg of MechaCar prototypes effectively as seen from the r-squared value. Since this model's r-squared is 0.7149, this means that about 70% of the variablilty of our dependent variable can be explained using this linear model.


## Summary Statistics on Suspension Coils

### Total Summary
<img width="307" alt="Screen Shot 2022-12-11 at 8 41 52 PM" src="https://user-images.githubusercontent.com/107594280/206962257-1314cc36-4d76-460d-86ce-f79a1528e9b4.png">

### Lot Summary
<img width="483" alt="Screen Shot 2022-12-11 at 8 42 36 PM" src="https://user-images.githubusercontent.com/107594280/206962322-45dba828-d99a-4437-9555-df4b4c7b5b25.png">

### Summary
1. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

Based on the total summary, current manufacturing data does meet this design specification, based on the variance at 62.29 PSI, which is within the 100 PSI variance requirement. However, if we look at the variance for each individual lot, we can see that Lot 3 is way over the 100 PSI limit at 170.29 PSI.

## T-Tests on Suspension Coils
<img width="680" alt="Screen Shot 2022-12-11 at 9 23 12 PM" src="https://user-images.githubusercontent.com/107594280/206966805-5e16070a-5773-42de-b549-d2d6bb67311d.png">
<img width="680" alt="Screen Shot 2022-12-11 at 9 23 53 PM" src="https://user-images.githubusercontent.com/107594280/206966873-a5afa44b-d776-4885-b37d-2154597cc07b.png">


### Summary
- The metrics for the all manufactoring lots reveal a p-value of 0.6028. This is not statistically significant and therefore we cannot reject the null hypothesis. 
- The t-test for lot 1 reveals a p-value of 1, meaning that the results are not statistically significant we fail to reject the null hypothesis. 
- The t-test for lot 2 reveals a p-value of 0.6072, meaning that the restults are not statistically significant and we fail to reject the null hypothesis. 
- The t-test for lot 3 reveals a p-value of 0.04168, meaning that the results are statistically significant and we can reject the null hypothesis.

## Study Design: MechaCar vs Competition
When buying a car, it is important to know what else is in the market and make sure you are getting all your needs met. When designing a sttistical study to compare ourselves to the competition, I would look at safety rating between vehices.

The null hypothesis would be:
  - There is no statistical difference between the competition's mpg safety rating and MechaCar's safety rating

The alternative hypothesis would be:
  - There is a statistical difference between the competition's mpg safety rating and MechaCar's safety rating
 
I would use the two sample t-test to test my hypothesis because it allows for the comparison of two sample means rather than comparing a sample to the population mean. The data I would need to run this test incudes safety rating data from the MechaCar as well as the MechaCar's competitors. The data would also need to be/assumed to be numerical and continuous, randomly selected, normally distributed, large, and the variances should be similar.
