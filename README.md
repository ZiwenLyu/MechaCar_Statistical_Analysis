# MechaCar_Statistical_Analysis
AutoRu's new prototype, the MechaCar, is having some glitches during the productions and blocking the whole manufacturing team's progress. This project will dig into the data of productions for some insights to reveal problems.  

## Linear Regression to Predict MPG

I conduct a linear regression to predict mpg of MecharCar. I set vehicle length, vehicle weight, spolier angle, ground clearance, and AWD as independent variables, and mpg as a dependent variable. Their slopes are as shown in the graph, are 6.267, 0.001245, 0.06877, 3.546, and -3.411 respectively.

![The coefficents](https://github.com/ZiwenLyu/MechaCar_Statistical_Analysis/blob/main/d1.png)

The significance level is 0.05. From the result below we can know that, the P-values for variables vehicle length, vehicle weight, spolier angle, ground clearance, and AWD are 2.6e-12, 0.0776, 0.3069, 5.21e-8, and 0.1852, respectively. Apparently, the vehicle length and ground clearance have sufficient evidence to reject null hypotheses. They provide a non-random amount of variance to the mpg values.

![The P-values](https://github.com/ZiwenLyu/MechaCar_Statistical_Analysis/blob/main/d1-Pvalue.png)

This linear model predict mpg of MechaCar prototypes effectively. The multiple R squard is 0.7149, which means it accurately predicts 71.49% of mpg values. And the P-value of this model is 5.35e-11, smaller than the significance level 0.05, indicating that it is sufficient to reject the null hypothesis that the slope is zero.


## Summary Statistics on Suspension Coils

According to the AutoRU, the design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. The left graph is the total statistic summary and the right graph is the statistic summary for each lot. As the graph speaks, the variance is only 62.3, implying that the current manufacturing data meet this design specification for all manufacturing lots in total. But by looking closely at each lot individually, the variance of Lot 3 exceeds 100 and it's possible that Lot 3 might have manufacturing issues over producing suspension coils.

![total summary statistics](https://github.com/ZiwenLyu/MechaCar_Statistical_Analysis/blob/main/total_summary.png)
![lot summary statistics](https://github.com/ZiwenLyu/MechaCar_Statistical_Analysis/blob/main/lot_summary.png)

## T-Tests on Suspension Coils

To better understand the suspension coils problem, I performed t-tests to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch.

![t-test of the total sample](https://github.com/ZiwenLyu/MechaCar_Statistical_Analysis/blob/main/t_test0.png)

From the t-test of the all manufacturing lots, the P-value is 0.0628, bigger than the significance level of 0.05. This means that we have insufficient evidence to reject the hypothsis that the mean of all lots is equal to the population mean of 1500.

![t-test of the Lot 1](https://github.com/ZiwenLyu/MechaCar_Statistical_Analysis/blob/main/t_test_lot1.png)

The t-test of the Lot 1 reveals that its P-value is also bigger than 0.05, suggesting we don't have enough evidence to reject the hypothesis that the mean of Lot 1 is equivalent to the population mean.

![t-test of the Lot 2](https://github.com/ZiwenLyu/MechaCar_Statistical_Analysis/blob/main/t_test_lot2.png)

The t-test of the Lot 2 also shows that its P-value is bigger that the significance level 0.05. We cannot reject the hypothesis that the mean of Lot 2 is equal to the population mean.

![t-test of the Lot 3](https://github.com/ZiwenLyu/MechaCar_Statistical_Analysis/blob/main/t_test_lot3.png)

The t-test of the Lot 3 tells a different story. The P-value is 0.04168 and it's samller than the siginificance level. It means that we have sufficient evidence to reject the null hypothesis and accept the alternative hypothesis that the mean of Lot 3 is difference from the mean of the population. The result of t-test increases the likelihood that the production of suspension coils in Lot 3 are problematic.

## Study Design: MechaCar vs Competition

This study is designed to better identify the MechaCar's advantages and quantify MechaCar's performance against the competition. As inflation and gasoline prices soar recently, a cost-effective vehicle with highway fuel efficiency will be popular among customers. To understand how MechaCar performs in these two areas, this study will test MechaCar's costs and fuel efficiency against other cars' in markets.

- Metrics to test: the average price of MechaCar in markets in the nations and the average prices of similar type of vehicles in markets. The average highway fuel efficiency of MecharCar and the that of similar type of vehicles in markets.

- Null hypothesis: there's no statistical difference between their means. 
- Alternative hypothesis: MechaCar's means are statistically different from other similar cars' means.

- Statistical tests: For the cost test, one-sample t-test will be used to test a statistical difference between the mean of the MechaCar distribution and the mean of the all similar type of car distribution. For the fuel efficiency test, we will also use one-sample t-test. Because prices and fuel efficiency are continuous data, and in two tests we are comparing a sample to a large population.

- data we need: prices of MechaCar in every store in the nation, all prices of similar type of cars in the markets in this country, the fuel efficiency of every MechaCar, and the fuel efficiency of other similar cars.
