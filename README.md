# MechaCar_Statistical_Analysis

## Purpose
I have been encharged with looking at the production of prototype cars for MechaCars to see if there are certain prototypes that are hindering this process. I was given data two Comma Separated Value files, one on [Miles per Gallon](https://github.com/bazinga183/MechaCar_Statistical_Analysis/blob/main/MechaCar_mpg.csv) and one on [Suspension Coils](https://github.com/bazinga183/MechaCar_Statistical_Analysis/blob/main/Suspension_Coil.csv). I use these files and run regressions and t-tests to determine if there are any discrepancies within the data or any aspects of production that should be improved upon.

## Linear Regression to Predict MPG

![regression](https://user-images.githubusercontent.com/46951897/139799926-eb7f8d42-358b-49de-b0c0-55b21258ec47.png)

Here we have a linear model that shows how Miles per Gallon is affected by the followng variables: Vehicle Length, Vehicle Weight, Spoiler Angle, Ground Clearance, and AWD. Judging by the results, vehicle length, weight, and ground clearance are the variables that provide the most non-random variance calculations according to the probability metric (Pr(>|t|)).

In addition, our P-value is 5.35e-11, which is much smaller than the standard significance level of 0.05%. Thus, we can reject our null hypothesis and say that the slope of this linear is not zero. Lastly, if we look at our R-squared figure, it is .71, which suggests that 71% if the data correctly predicts mpg outcomes within the model. 

## Summary Statistics on Suspension Coils

### Total Summary
![total_summary](https://user-images.githubusercontent.com/46951897/139788486-8662ca41-11ba-49d0-a22e-7b84d19315c9.png)

Here, we are using data on suspension coils and the weight they can hold for 50 prototype cars across 3 different lots. We notice that there is consistency across most cars as the mean and median are very close and center on 1500. In addition, the standard deviation, 8, shows that most of our cars are within 20 from 1500.

### Lot Summary
![lot_summary](https://user-images.githubusercontent.com/46951897/139788493-c1ad4d12-a748-4079-bb02-4ef17dfbd728.png)

Here, we have grouped the cars by their manufacturing lot, and once again the mean and median close in on 1500. However, we do notice that the variance and standard deviation for Lot1 and Lot2 do not vary very far. In contrast, Lot3 has a much higher variance at 170 and standard deviation at 13. In addition, the question we are trying to answer here is if the variance of the coils does not exceed 100 PSI. While the total summary table says that we fall within this restriction, it isn't until we look at the lot summary where we see that Lot3 has more than surpassed this restriction with its variance being 170.

## T-Tests on Suspension Coils

### T-Test Across All Lots

![total_t-test](https://user-images.githubusercontent.com/46951897/139790982-991846ed-3d8f-4621-9538-e71d86490d24.png)

This image shows a t-test conducted to compare the means of the PSI from the dataset here versus the mean of 1500 from a sample population. We find that the p-value is .06, which is greater than the standard significance level of 0.05%, thus we fail to reject our null hypothesis that these two are statistically different. 

### T-Tests Across Individual Lots

![lot_t-tests](https://user-images.githubusercontent.com/46951897/139790581-d8d5e90c-54c7-4010-8d8f-b049a794af5f.png)

Here, we take 3 different t-tests across the 3 lots and notice that the p-values for Lots 1 and 2 are above 0.05%, but Lot 3 fails to be above this significance level at .04. Thus, for Lots 1 and 2, we can fail to reject that its PSI means and the sample population mean of 1500 are statistically different, whereas, for Lot 3 we can reject the null hypothesis that the sample mean and Lot 3's means are not statistically different. 

## Study Design: MechaCar vs Competition

Here is a hypothetical section where I design a project for a study to be conducted comparing MechaCars own vehicles against rival competitors. 

### What metric or metrics are you going to test?
Regarding metrics to collect, with the large advent towards electric vehicles (EV) it is best to see if MechaCar gas vehicles are just as efficient as electric vehicles when it comes to total lifetime travel distance. Since EV's are quickly becoming every car company's newest business venture, it is best to see if MechaCar should consider shifting their cars to the renewable option as well.

### What is the null hypothesis or alternative hypothesis?
The null hypothesis (Ho) is that a gas car's total travel distance is equal to an EV's total travel distance.
The alternative hypothesis (Ha) is that the gas car's total travel distance is not equal to an EV's total travel distance.

### What statistical test would you use to test the hypothesis? And why?
For this test, it would be best to use a multiple linear regression so that we can use all of the factors listed above, as well as any new ones that come up, so that we can take into account the vital variables that contribute to total travel distance for these vehicles. The dependet variable would be the total travel distance, and the rest of the variables would be independent.

### What data is needed to run the statistical test?
The metrics to collect from rival competitors would be as follow:
 - Total Miles from a full tank or charge. Compare the total miles a vehicle can get with a full tank of gas versus how much competitor EV's can go with a full charge.
 - Total Revenue Earned From Selling Vehicles. Data can be collected to compare the total revenue earned from selling vehicles from different years, this can be broken down by different standards so long as the final cash figure is there to determine if the gas car industry is effective.
 - Total Cost of Production. Compare the cost of producing gas cars and EV's between MechaCar and rival industries. This would also help establish if MechaCar should explore going into the EV market itself.
 - Average Lifetime Usage. This would be a fun metric to measure as to see if the reliability of the cars hold up over time. In addition, this contributes to the total miles a vehicle can travel before needing to be replaced.
 - Horsepower. This metric would be collected to give consumers the ability to travel where they need to get at the speed they desire (even though we do not want them to go too crazy).
 - Vehicle Weight. This comparison would help to see how big/dense of a car is needed to achieve either vehicle's build. This would also effect the time it takes to build vehicles and the cost of transportation as well.
