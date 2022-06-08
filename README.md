# MechaCar Statistical Analysis

## Overview of the Analysis

AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles. By running regression analyses and t-tests, I will review production data for AutoRU's newest prototype, the MechaCar, and provide insights that may help the manufacturing team. Additionally, I will design a statistical study to compare the vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.

 
## Deliverable 1 - Linear Regression to Predict MPG

![Deliverable_One_LM.PNG](https://github.com/dwwatson1/MechaCar_Statistical_Analysis/blob/main/images/Deliverable_One_LM.PNG)

The linear regression model above estimates that: 

```mpg = (6.267)vehicle_length + (0.0012)vehicle_weight + (0.0688)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD - 104.0```

* Using the formula above, vehicle length, and ground clearance are statistically likely to provide non-random amounts of variance to the model or are most likely to affect the miles per gallon performance of the MechaCar's AutosRUs prototype.  
* Given the model's ```p-value of 5.35e-11```, which is lower than the 0.05 assumed statistical significance, there is strong evidence **against the null hypothesis** (slope = 0). Therefore, we can accept the alternative hypothesis that the **slope is not 0**.
* The model's ```r-squared value of .7149``` means that about 71% of the variance in mpg predictions can be explained by this model, while 29% cannot. In other words, the variables of vehicle length, spoiler angle, ground clearance, and AWD have a strong positive association with mpg. Therefore, this model effectively predicts mpg of MechaCar prototypes.


## Deliverable 2 - Summary Statistics on Suspension Coils
![Deliverable 2.PNG](https://github.com/sjmisina/MechaCar_Statistical_Analysis/raw/main/static/resources/coil_analysis.png)
- Data points provided in <code>Suspension_Coil.csv</code>
- When reviewed as a whole, variance is within 100 psi, as set by company policy. This is misleading as Lot 3 is well out of range with a variance of 170+; thus the single greatest contributor to negative drag on overall performance.
<br />

## Deliverable 3 - T-Tests on Suspension Coils
Suspension Coils Cumulative T-test
![Suspension Coils Cumulative T-test](https://github.com/ArtTucker/MechaCar_Statistical_Analysis/blob/main/images/sus_coil_one_samp_ttest.png))
* A review of the results of the T-test for the suspension coils across all manufacturing lots shows that they are not statistically different from the population mean, and the p-value is not low enough (0.0603) for us to reject the null hypothesis.
![Suspension Coil Lot 1 T-test](https://github.com/ArtTucker/MechaCar_Statistical_Analysis/blob/main/images/sus_coil_lot1_samp_ttest.png)
* A review of the results of the T-test for the suspension coils for Lot 1 shows that they are not statistically different from the population mean, and the p-value is not low enough (1) for us to reject the null hypothesis.
![Suspension Coil Lot 2 T-test](https://github.com/ArtTucker/MechaCar_Statistical_Analysis/blob/main/images/sus_coil_lot2_samp_ttest.png)
* A review of the results of the T-test for the suspension coils for Lot 2 shows that they are not statistically different from the population mean, and the p-value is not low enough (0.6072) for us to reject the null hypothesis.
![Suspension Coil Lot 3 T-test](https://github.com/ArtTucker/MechaCar_Statistical_Analysis/blob/main/images/sus_coil_lot3_samp_ttest.png)
* A review of the results of the T-test for the suspension coils for Lot 3 shows that they are slightly statistically different from the population mean, and the p-value is just low enough (0.0417) for us to reject the null hypothesis. This lot may be need to be discarded, or at least more closely evaluated.

## Deliverable 4 - Study Design: MechaCar vs Competition

Many consumers, especially families and those who have previously been in accidents, value safety when it comes to picking their car. To test MechaCar's safety rating against its competition, we need to create a null and alternative hypothesis.

**H0 (Null Hypothesis):** MechaCar's vehicle safety ratings are no different from its competitors 

**Ha (Alternative Hypothesis):** MechaCar's vehicle safety ratings are different from its competitors 

To test these, we'd need to collect safety ratings on MechaCar's models as well as its competitors from the Insurance Institute for Highway Safety, which determines saftey ratings. As the non-profit explains, their scores are determined by four factors: measurements from dummies, survival space, airbags, and seat belt effectiveness. Using that data, we could t-test the population of vehicles and each carmaker. This will help us determine if MechaCar's vehicles' safety rating scores are statistically different from its competitors as a whole and then statistically different from each competitor.
