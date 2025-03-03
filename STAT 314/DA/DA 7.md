> The dataset ExamDataW24.csv represents the midterm and final exam grades for students in the ST314 online and campus courses for three previous consecutive terms. Use these data to complete a regression analysis in R and answer the following questions. 

> Part 1. Describing the relationship between your two variables

> a. (2 points) Graphically: Make a scatterplot of the relationship between ST314 student midterm grades (explanatory variable) and final exam grades (response variable). Include your plot in your submission. Describe in context the relationship from the scatterplot. Include strength, direction, form and outliers (if any). 

As midterm grades are higher, the final grades are also higher. They follow a very linear relationship. We can say that the relationship is modterately weak, positive, and linear since there seems to be a good concentration of data points on the line of best fit. There are a few outliers like the 95 on the midterm scoring a 70. Also, there’s another with a 60 on the midterm scoring a 95 or so. Furthermore, another surprising outlier is a 78 on the midterm that scored about a 30 on the final. There’s a few more outliers that are surprising but these were the ones that stood out to me.

![[../../../Ignored/IMG_2968.jpeg]]

> b. (2 points) Numerically: Calculate the correlation coefficient . Report the value of and describe in context the strength of the relationship based on your value. 

`cor(Midterm, Final)` = 0.636. The relationship on the scatterplot looks to be linear. Furthermore, with a value of .636, we can say that the strength of the relationship is in between moderately weak and moderately strong, leaning towards the weaker side.

> Part 2. Calculate the Least Square Regression Line (Model) and Check Conditions for Inference

> a. (3 points) Using R, calculate the least squares regression line that predicts final exam scores from midterm exam scores for ST314 students. Paste the R output for the model summary. Separately, state the least squares regression line (model) using statistical notation. Only pasting your R output without reporting the least squares regression line will not earn you points. 

$$\hat y=(r\frac{s_y}{s_x})x+b_0$$
$$y=.622x+30.197$$

![[../../../Ignored/IMG_2970.jpeg]]

> b. (4 points) Plot the residuals for the model. Include a reference line at 0. Include your plot in your submission. Check the linearity, normality and constant variation conditions using the residual plot. State why each condition is met or why it is not met. 

Linearity: Yes, There is no U shape or obvious curves in the plot
Normality: Yes, There seems to be random scatter of points above and below the reference line.
Independent: Yes, We assume this. Furthermore, it’s all different students so it’s implied also.
Constant Variation: No, The scatterplot does have a slight funnel shape from the right side.

![[../../../Ignored/IMG_2969.jpeg]]

> c. (4 points) Using your linear model, predict what the final score would be for a student who received a 84grade on the midterm, on average.

$$y=.622(84)+30.197$$
$$y=82.45$$

> Part 3. Is your model a good fit? Use your R output from the model in Part 2a. From the output, is there statistical evidence midterm exam score is a significant predictor of final exam score? Use a significance level of 0.05. 

> a. (2 points) State the null and alternative hypothesis for the individual t test on the slope. 

Null Hypothesis: There is no relationship between midterm and final grades
Alternative Hypothesis: There is a relationship between midterm and final grades

> b. (2 points) State the test statistic, degrees of freedom and p-value from the output. 

Test Statistic: 578.4
DF: 1 and 850 DF
P-value: 2.2e-16 (about 0)

> c. (2 points) Make a conclusion. Include context, a statement in terms of the alternative and whether to reject the null based on the level of significance.   

There is convincing evidence that there is a relationship between midterm and final grades. Since the p-val is below the significance level of .05, at 2.2e-16 (which) is almost 0, we reject the null hypothesis. As a students midterm grade rises, then their projected final grade would also rise in a linear relationship.

Note that we do not state anything about the confidence interval in this question since it does not state anything about it and the conf interval portion is on the next part (d).

> d. (2 points) Calculate the 95% confidence interval for the slope. Interpret the point and interval estimate

This does not say whether we should calculate by hand or not, therefore, we are going to be taking it from the code (since there is code to calculate it for us, I’ll assume we are supposed to do that). 

$$b_1\pm(t_{n-(k+1),\alpha/2})(SE_{b1})$$
$$.62\pm2.01(.026)$$

The 95% confidence interval for the slope is [.5714, .6729]. This means that the final grade increases by a minimum of .57 points to a maximum of .67 points per point scored on the midterm. The point estimate, .62, is the average point increase per point scored on the midterm. While the interval estimate, about .05, is how much that could differ depending on a specified confidence interval, in this case 95%. 