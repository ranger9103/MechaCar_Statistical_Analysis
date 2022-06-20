# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG
- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
o Vehicle length and ground clearance are shown to have a non-random amount of variance. Vehicle weight, spoiler angle and AWD have a random amount of variance based on the p-values.
- Is the slope of the linear model considered to be zero? Why or why not?
o The slope of this model is not zero as the p-value is 5.35e-11 which is significantly less than 0.05. 
- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not? 
o With an r value of 0.7149 the model can be deemed to effectively predict mpg 71.49% of the time. In a real world application this would have to be acknowledged and determined if it was adequate for the use case.



## Summary Statistics on Suspension Coils
- The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
- The overall variance of 62.3 PSI is well within the limit of 100 PSI. 
Individually lots 1 and 2 have a variance of <10 where lot 3 is well over the range. Lot 3 should be evaluated for the significant variance to avoid manufacturing issues.






## T-Test on Suspension Coils
- Briefly summarize your interpretation and findings for the t-test results. Include screen shots of the t-test to support your summary.
o For lots 1 and 2 the null hypothesis cannot be rejected as the p-values are 1 and 0.61 respectively. However, lot 3 does not fall in the same category as the p-value is 0.04. 
o Again, lot 3 procedures need to be reviewed to avoid further issues.

data:  lot1$PSI
t = 0, df = 49, p-value = 1
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1499.719 1500.281
sample estimates:
mean of x 
     1500

data:  lot2$PSI
t = 0.51745, df = 49, p-value = 0.6072
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1499.423 1500.977
sample estimates:
mean of x 
   1500.2

data:  lot3$PSI
t = -2.0916, df = 49, p-value = 0.04168
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1492.431 1499.849
sample estimates:
mean of x 
  1496.14

## Study Design: MechaCar vs Competition
There are many options to compare the MechaCar to competitors. The first step is to determine the major competition. Taking this comparison will allow for marketing to compete and focus on those areas the MechaCar surpasses the main competition. 

Many things go into the decision on a new vehicle. Looking at the cost of ownership, purchase price and safety are all areas to look at for the end consumer. From a manufacturing perspective, the cost of production between the two is also important if the information is available. This can lead to adjustments in pricing if the margins are more flexible compared to the competition.

The main category to look at would be purchase price of the MechaCar versus the next closest competitor. This is something the average consumer looks at and will be an important metric for production and marketing.

The null hypothesis is the MechaCar is priced appropriately/competitively when compared to the competition. Conversely, the alternative hypothesis would be that it is not and adjustments may need to be reviewed.

Additional multiple linear regressions could be utilized for initial evaluations to compare price, average cost of ownership and safety. 
