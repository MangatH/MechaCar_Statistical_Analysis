# MechaCar_Statistical_Analysis

## Overview of the project:
AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

This challenge involves assisting Jeremy and the data analytics team do the following:
* Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.
* Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
* Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
* Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, write a summary interpretation of the findings.


## Linear Regression to Predict MPG:
The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. A linear model is designed that predicts the mpg of MechaCar prototypes using several variables from the MechaCar_mpg.csv file.
The regression analysis was performed using 0.05 level of significance.
<img width="568" alt="Screen Shot 2022-12-13 at 3 34 02 PM" src="https://user-images.githubusercontent.com/111387025/207521690-b6b7ae05-38e8-41e5-8b50-17ce231ac7e5.png">

## Summary of Linear Regression:
<img width="544" alt="Screen Shot 2022-12-14 at 11 48 51 AM" src="https://user-images.githubusercontent.com/111387025/207521127-c72beabf-b12c-4f51-aa6e-a89260ac9d72.png">
 
The summary indicates that the p-value is less than the significance level(0.05), indicating that a correlation exists. The residuals indicates that the min and max value is -19.4701 and 18.5849 respectively.

* Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset? <br/>
The level of significance taken is 0.05, there all the coefficients are compared to this value, to know the statistical significance. <br/>

Coefficients: <br/>
vehicle_length = 0 < 0.05, indicates non-random amount of variance. <br/>
vehicle_weight = 0.08 > 0.05, indicates random amount of variance. <br/>
spolier_angle = 0.31 > 0.05, indicates random amount of variance. <br/>
ground_clearance = 0 < 0.05, indicates non-random amount of variance. <br/>
AWD = 0.18 > 0.05, indicates random amount of variance. <br/>

The coefficients, vehicle length and ground clearance provided a non-random amount of variance to the mpg values in the dataset. <br/>

* Is the slope of the linear model considered to be zero? Why or why not? <br/>
As per the analysis, the slope of the linear model is not zero. This can be best explained with the help of p-value. The p-value is equal to 5.35e-11 which is less than 0.05. Thus indicating a non zero slope. <br/>
The slope of coefficients is another way of affirming this non-zero slope, as shown below: <br/>
Coefficients: <br/>
vehicle_length = 6.267 <br/>
vehicle_weight = 0.001 <br/>
spolier_angle = 0.688 <br/>
ground_clearance = 3.546 <br/>
AWD = -3.411 <br/>

Therefore, the slope of the linear model is not zero, as shown with the help of formula = mpg(-0.01) + vehicle_length(6.267) + vehicle_weight(0.001) + spoiler_angle(0.688) + ground_clearance(3.546) + AWD(-3.411).

* Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not? <br/>
The R-squared value is 0.7149, which indicates that there exists a strong correlation. Thus, this linear model predict mpg of MechaCar prototypes effectively.


## Summary Statistics on Suspension Coils:
### Summary statistics of all the manufacturing lots:

<img width="363" alt="Screen Shot 2022-12-13 at 3 38 44 PM" src="https://user-images.githubusercontent.com/111387025/207537195-0de4f65a-577f-4dc4-a9ab-ce42c6dc589c.png">
The mean is 1498.78, median is 1500, variance is 62.29356 and standard deviation 7.892.

### Summary statistics by manufacturing lot number:

<img width="511" alt="Screen Shot 2022-12-13 at 3 37 51 PM" src="https://user-images.githubusercontent.com/111387025/207538420-f86f53fd-ab9e-424f-9a6d-f0025f5926b9.png">

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not? <br/>
The variance of the suspension coils of all manufacturing lots is 62.29, which is within the limit of 100 pounds per squaure inch. The variance for the lot 1 and lot 2 is 0.98 and 7.469 which is quite low, whereas the variance for the lot 3 is 170.286 which is quite high as compared to the limit of 100 pounds per square inch. Therefore, the lot 3 does not meet the design specifications.

## T-Tests on Suspension Coils:
### T-Tests on all manufacturing lots:
sample mean =1498.78, p-value = 0.06028, level of significance = 0.05 <br/>
p-value is greater than level of significance, therefore the null hypothesis is accepted. Thus, it can be concluded that the result is statistically insignificant.

<img width="414" alt="t-test" src="https://user-images.githubusercontent.com/111387025/211200642-e8a61b91-3cf3-4ec4-ad7d-70d2fc9d15a1.png">

### T-Tests for Lot 1:
p-value = 1, which is greater than the level of significance, 0.05. Thus, the null hypothesis is accepted, indicating that the result is statistically insignificant.

<img width="702" alt="lot 1" src="https://user-images.githubusercontent.com/111387025/211200676-ff073968-0cc4-4733-b1f8-35d3ab1d2fe9.png">

### T-Tests for Lot 2:
p-value = 0.6072, which is greater than the level of significance, 0.05. Thus, the null hypothesis is accepted, indicating that the result is statistically insignificant.

<img width="714" alt="lot 2" src="https://user-images.githubusercontent.com/111387025/211200692-0c7a1645-1d82-46a4-a4c8-cab8310b848d.png">

### T-Tests for Lot 3:
p-value = 0.04168, which is less than the level of significance, 0.05. Thus, the null hypothesis is rejected, indicating that the result is statistically significant.

<img width="680" alt="lot 3" src="https://user-images.githubusercontent.com/111387025/211200700-0ac3fcc0-0bf0-42f9-b6ca-ef43be42dbc9.png">

## Study Design: MechaCar vs Competition
In further analysis, various metrics that can be of interest to a consumer are  cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.

* What metric or metrics are you going to test? <br/>
The metrics used for next analysis can be highway fuel efficiency, maintainance cost and safety rating.

* What is the null hypothesis or alternative hypothesis? <br/>
The null hypothesis can be that there is no significant difference in the highway fuel efficiency, maintainance cost and safety rating. <br/>
The alternate hypothesis can be that there is significant difference in the highway fuel efficiency, maintainance cost and safety rating.

* What statistical test would you use to test the hypothesis? And why? <br/>
Multi Linear Regression analysis can be used to see the how these variables are correlated in affecting the safety rating of MechaCar and their competitors.

* What data is needed to run the statistical test? <br/>
A large sample size (greater than 30) collected from MechaCar users and their competitors, including the data for highway fuel efficiency, maintainance cost and safety rating. 
