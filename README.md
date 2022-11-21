# MechaCar_Statistical_Analysis
## Overview
This project involves the use of statistics and hypothesis testing to analyze a series of datasets from the automotive industry.
The following tests have been performed in this project

- multiple linear regression analysis to identify variables that predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Conduct t-tests to determine statistical variation between the manufacturing lots and the mean population
- Also, design statistical study to benchmark vehicle performance of the MechaCar with other manufacturers
## Results
### Linear Regression to Predict MPG
![lin](https://user-images.githubusercontent.com/109990578/202953145-5d41e242-9a83-4e26-89d4-3571c284fcca.png)
- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
From the summary output, each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model. Based on the results, vehicle length and ground clearance (and Intercept) provide a non-random amount of variance to the linear model of mpg.
- Is the slope of the linear model considered to be zero? Why or why not?
The p-value = 5.35 x 10(-11) which is much smaller than the significance level of 0.05. This provides sufficient evidence to reject our null hypothesis, which means that the slope of our linear model is not zero.
- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
R-square is 0.71 so 71% of the variations in mpg can be explained by changes in the vehicle length, the vehicle weight, the spoiler angle, the drivetrain and the ground clearance. We can consider this linear model as fairly efficient to predict mpg of MechaCar prototypes.
## Summary Statistics on Suspension Coils
- The suspension coil’s PSI continuous variable across all manufacturing lots

![all man](https://user-images.githubusercontent.com/109990578/202954748-6ff393be-5c5e-4b3d-a5c7-79201681fbe5.png)

- The following PSI metrics for each lot: mean, median, variance, and standard deviation.

![by each manuf](https://user-images.githubusercontent.com/109990578/202954750-b119e78f-e30c-44b8-a621-072a3a089fc7.png)

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.
The design specs are respected for all manufacturing lots in total with a global variance of 62.3 psi.
On the lot level, Lot 1 and Lot 2 are into specs with respectively variances of 0.98 and 7.5 psi. The Lot 3 is out of specs with a variance of 170.3 psi.
## T-Tests on Suspension Coils
- T-Test all manufacturing lots against the population mean

![tallm](https://user-images.githubusercontent.com/109990578/202955184-3f1df276-0207-425a-8237-e6f0759a2f18.png)

This shows that p-value = 0.3724 > 0.05 (significance value). Thus no sufficient evidence to reject the null hypothesis, which implies that all manufacturing lots are statistically similar to the population mean of 1,500 pounds per square inch.

- T-Tests each manufacturing lot against the population mean
Lot 1

![lot1](https://user-images.githubusercontent.com/109990578/202955658-162caa22-065f-4535-8939-2def605ee2fc.png)

Here the p-value 2.04 X10^(-8) is above the significance value of 0.05 percent, so not enough evidence to reject the null hypothesis and conclude that Lot 1 is statistically similar to the population mean of 1,500 pounds per square inch.

Lot 2

![lot2](https://user-images.githubusercontent.com/109990578/202957173-17a09d92-397c-4342-bfd4-3393f11d31c4.png)

shows that p-value = 0.002139 < 0.05 (significance value). That means we have sufficient evidence to reject the null hypothesis, and we would state that lot2 is statistically not similar to the population mean of 1,500 pounds per square inch.

Lot 3

![lot 3](https://user-images.githubusercontent.com/109990578/202957359-3406add7-dbd7-44f4-a8c3-36a550dfb0f6.png)

shows that p-value = 0.02089 < 0.05 (significance value). That means we have sufficient evidence to reject the null hypothesis, and we would state that lot2 is statistically different to the population mean of 1,500 pounds per square inch.


## Study Design: MechaCar vs Competition
To compare the performance of the MechaCar prototype against the vehicles from the competition, we will perform a statistical analysis based on the following metrics: the "0 to 60 mph" time, the braking distance, the fuel economy (mpg), the Power, and the safety rating.

In our case the null hypothesis would be: 
Each performance metrics is statistically similar between the MechaCar prototype and all vehicle from the other manufacturers.

We would use a one-way ANOVA test to compare the means of a continuous numerical variable across a number of groups.
This is a suitable test for this analysis because we would compare the means for each metric across the different manufacturers.

To perform the test, we would need data of MechaCar vehicles and its competition, all gathered in a single dataframe where each metric is a column.
The data could be scraped from vehicle data website using vehicle data API.



