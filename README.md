# **MechaCar_Statistical_Analysis**

## Overview of the analysis: 

AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has requested a revision of the production data for insights that may help the manufacturing team. Basic Project Plan:
 1. Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
 2. Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
 3. Run t-tests to determine if the manufacturing lots are statistically different from the mean population
 4. Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

### Software: RStudio 

### Results: 

## Linear Regression to Predict MPG. 

We begin this project performing a linear regression to predict the Miles Per Gallon (MPG). The code can be found here: [MechaCarChallenge.RScript](https://github.com/chocoplace/MechaCar_Statistical_Analysis/blob/main/MechaCarChallenge.RScript). From the analysis we can share following: 
 1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset? Vehicle_length and ground_clearance are the variables that provided a non-random amount of variance on the model.  
 
 2. Is the slope of the linear model considered to be zero? Why or why not? The P-value of our linear regression analysis is 5.35e-11, which is much smaller than our assumed significance level of 0.05%. Therefore, we can state that there is sufficient evidence to reject our null hypothesis, which means that the slope of our linear model is not zero.
 
 3. Does this linear model predict the mpg of MechaCar prototypes effectively? Why or why not? In a simple linear regression model, the higher the correlation is between two variables, the more that one variable can explain/predict the value of the other. The model has an R-squared value of 0.7149 which means that roughly 71.49% of the variability of our dependent variable (mpg predictions) is explained using this linear model.

![Deliverable1](https://github.com/chocoplace/MechaCar_Statistical_Analysis/blob/main/Resources/D1.png)

## Summary Statistics on Suspension Coils
Proceed the analysis by collecting summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots. According to the background of the data, the design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. The results help us answer the questions: 
  1. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not? No, the current mannufacturing data doesn't meet the design specifications. The variance for the general suspension coil is 62.29356, which stays within the 100 variance. However, when analyzing each lot we see Lot3 with a variance over the limit of 170.2861224.

![total_summary](https://github.com/chocoplace/MechaCar_Statistical_Analysis/blob/main/Resources/D2_total_summary.png)

![Lot_summary](https://github.com/chocoplace/MechaCar_Statistical_Analysis/blob/main/Resources/D2_lot_summary.png)

## T-Tests on Suspension Coils
After, the task was to run t-tests to determine if the manufacturing lots are statistically different from the mean population. From the results we can determine there is not statistically difference on Lot1 and Lot 2, and there is a significant difference in Lot3 with a P-value of 0.04168. The P-value of Lot3 is lower than the assumed significance level, therefore, we would state that there is enough evidence to reject the null hypothesis. 

![Deliverable3](https://github.com/chocoplace/MechaCar_Statistical_Analysis/blob/main/Resources/D3.png)


## Study Design: MechaCar vs Competition
And lastly, the project requieres to design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.

The most straightforward way to do this is to use the analysis of variance (ANOVA) test, which is used to compare the means of a continuous numerical variable across a number of groups (or factors in R). Depending on your dataset and questions you wish to answer, an ANOVA can be used in multiple ways. 

Therefore, the model will use: 
 - What metric or metrics are you going to test? MPG, vehicle model, maintenance, vehicle_waight, fuel efficiency. 
 - What is the null hypothesis or alternative hypothesis? Regardless of whichever type of ANOVA test we use, the statistical hypotheses of an ANOVA test are the same:
 - H0 : The means of all groups are equal, or µ1 = µ2 = … = µn.
 - Ha : At least one of the means is different from all other groups.
 - What statistical test would you use to test the hypothesis? And why? A one-way ANOVA is used to test the means of a single dependent variable across a single independent variable with multiple groups. (e.g., fuel efficiency of different cars based on vehicle class).
 - What data is needed to run the statistical test? The input data that must be validated prior to using the statistical test:
    - The dependent variable is numerical and continuous, and the independent variables are categorical.
    - The dependent variable is considered to be normally distributed.
    - The variance among each group should be very similar.

--
End
