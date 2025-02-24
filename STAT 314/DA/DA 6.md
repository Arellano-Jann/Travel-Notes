> The following information will be used for parts 1 and 2 of this assignment.
The EPA_W24.csv contains a set of randomly sampled vehicles. Each vehicle in the data set has a projected Annual Fuel Cost that estimates how much the vehicle will cost over a year in fuel, along with many other variables about the vehicle.
Use the EPA_W24.csv dataset and the ComparingTwoMeans_DA6.R script to compare the average annual fuel cost in dollars between automatic and manual transmissions from 2021 vehicles.  
Part 1. (6 points) Exploring the data. 
a. (2 points) Visualize the data with a side by side boxplot. 
i. (1 point) Paste the side-by-side box plot of the data. 
![[../../../Ignored/IMG_2964.jpeg]]

> ii. (1 point) Add a title and axis labels. 

Title - Annual Fuel Cost based on Trans (EPA) whatever EPA means
x Label - Cost in dollars

> b. (2 points) Describe the distribution in context. Is there visual evidence the average annual fuel cost is different between the automatic and manual vehicles? Explain.   

The median is quite different, visually, by about 300 or so. As for the 1QR and 3QR, the 1QR is relatively close while the 3QR is also different by about 300 or so. This tells us that the average fuel cost is different between auto and manual trans. The manual transmission is typically cheaper while the auto is typically more expensive.

> c. (2 points) Provide an organized table of the summary statistics. Include the sample means, standard deviations and sample sizes for each group. Round to nearest whole number. 

|        |      |                    |             |
| ------ | ---- | ------------------ | ----------- |
|        | Mean | Standard Deviation | Sample Size |
| Auto   | 1983 | 615                | 35          |
| Manual | 1776 | 449                | 35          |

  

> Part 2. (8.5 Points) Hypothesis Testing and Estimation. 
Question of interest: Do the data provide evidence of a difference between the average annual fuel cost for automatic and manual transmissions? 
Hypotheses: The null and alternative hypotheses are as follows, where represents the average annual fuel cost for all vehicles with automatic transmissions and represents the average annual fuel cost for all vehicles with manual transmissions.
Checking Conditions: 
• The data available come from random samples from the population of all vehicles manufactured in 2021, so we can assume the sample are representative of their respective populations.
• The sample sizes are large enough so that the sampling distributions for   and   are both normal according to the central limit theorem. 
• Lastly, the populations are independent. There is no repeated measurement nor is there any dependence between the two groups. 
Overall, the conditions are somewhat met. The sampling method is unknown so we should consider this in our conclusions. 

>Calculate: 
a. (1 point) From the summary statistics calculate the test statistic “by hand”. Show work. You must show how the calculation for the test statistic is done (it is not enough to just show R output for this question).  



> b. (1 point) State the degrees of freedom. You may choose conservative or Satterthwaite. Either are okay.   

> c. (1 point) Obtain a p-value based on your calculated test statistic and degrees of freedom using the pt() function in R. Show work/code.  

>d. (2 points) From the summary statistics, calculate the 95% Confidence Interval “by hand”. Show work.   

>e. (0.5 point) Obtain a p-value from t-test and confidence interval using R.  Paste the output. Are your answers different? Why, yes/no?  

> Conclude: 
f. From the R output, write a four-part conclusion describing the results. 
• (1 point) Provide a statement in terms of the alternative hypothesis. 
• (1 point) State whether (or not) to reject the null.
• (1 point) Give in context an interpretation of the point and interval estimate.  
• Make sure to provide a direction to your interval, for example, one group had a smaller (or larger) mean than the other, include this relationship in your point and interval estimate.

> Part 3. (8.5 points) ANOVA   
  The General Social Survey collects data on demographics, education, and work, among many other characteristics of US residents. Using ANOVA, we can consider educational attainment levels for all 1,172 respondents at once. Below are the distributions of hours worked by educational attainment and relevant summary statistics that will be helpful in carrying out this analysis. 

![](blob:capacitor://localhost/7493b688-71cf-4765-97d7-f207981d16ec)

![](blob:capacitor://localhost/0feffb86-8476-4348-b81a-6ad85209b5ab)

> a. (2 points) Write the null and alternative hypotheses for evaluating whether the average number of hours worked varies across the five groups.   

b. (1.5 points) Using the information provided, assess whether the following conditions necessary to accurately perform an ANOVA F test are met:

i. (0.5 point) Are the observations in the study independent?

ii. (0.5 point) Are the sample sizes sufficiently large? (Hint: the n row of the table above provides the sample sizes of each group.)

iii. (0.5 point) Is the variation in the groups about equal from one group to the next? (Hint: use the spread of the boxplots and standard deviation values from the table to assess this condition.)

  
To assess whether there is a significant difference in the average number of hours worked between one or more of the groups, we need to determine the mean squares between groups (MSTr) and the mean squares within groups (MSE). Each of these values has an associated degrees of freedom. 

• The degrees of freedom associated with the MSTr are

• The degrees of freedom associated with the MSE are

c. (1 point) An ANOVA was performed in R. The estimate for the mean squares between groups is MSTr = 501.54 and the resulting F statistic is equal to 2.189. Determine the average variation within each group. That is, calculate the MSE. 

d. (2 points) Using the F statistic from the previous question (c.) and the two values for the degrees of freedom listed above, calculate the p-value for this test. 

e. (2 points) Using the p-value calculated in question 5, write a conclusion for this ANOVA F test using a significance level of . (Hint: your conclusion should include a statement of evidence in favor of the alternative and a statement as to whether the null hypothesis is rejected or not.)