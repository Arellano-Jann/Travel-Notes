  
> Part 1. (3 points) Sampling Distribution and The Central Limit Theorem Simulations
> See the Central Limit Theorem in Action! Simulation is an important tool to investigate theoretical ideas. In this exercises we will: 
• Randomly generate populations of different shapes
• Take random samples of different sizes
• Visualize the sampling distribution of a mean from repeated sampling. 
• Identify the affect of sample size and the shape of the population on the sampled and sampling distribution. 
The goal of this simulation is to visualize and validate the central limit theorem. 
Getting Started: Go to the Simulation in Lesson 24 in the Week 4 Module in Canvas. 

> a. Simulate a normal distribution with a mean of 80 and standard deviation of 15. Take a sample of 20. 

> • (0.5 points) Take a screen shot of the Population, Sampled and Sampling Distribution. Paste it. 



> • (0.5 points) Is the mean of the sampling distribution approximately the same as the mean for the population ? 

Yes, the mean of the sampling distribution is about the same but difference of about .02 which is nothing to worry about.

> • (0.5 points) Is the standard deviation of the sampling distribution approximately ?

Not sure what this question means but it’s approximately 3.38. It’s different than the other 2 by about 12-14.

> • (0.5 points) Is the sampling distribution approximately normal?

I’d say it looks like a bell curve alright. :thumbsup:

> b. (1 point) Simulate different population shapes and manipulate sample sizes. You can change population shapes by selecting one of the other three options under the Population Distribution menu. Which population shapes need larger sample sizes in order for the sampling distribution to follow a Normal Distribution?

The skewed population distribution requires the largest sample size to reach the shape of the bell curve.

> Part 2. (5 points) Confidence Interval Simulations
Confidence Intervals at Work. The goal of a confidence interval is to estimate an unknown parameter. 
A confidence interval is comprised of an estimate from a sample, the standard error of the statistic and a level of confidence. We choose a confidence level based on how precise we need our estimate to be and how willing we are to risk not obtaining the parameter at all. 
The definition of a 95% confidence interval states:
Out of all possible samples of size n taken from the population, the confidence intervals calculated based on those samples will contain the true parameter value 95% of the time.
This means when we construct a 95% confidence interval, 5% of all intervals will not contain the true parameter. Therefore, we assume a 5% risk we might get an interval that does not contain the true parameter. We hope we get one of the “good” intervals. In practice, we will not know. The simulation repeatedly samples from a population, calculates a confidence interval for each sample and indicates how many confidence intervals obtain the true mean. 
The goal of this simulation is to visualize and validate the definition of a confidence interval. 
Getting Started: Go to the Simulation in Lesson 25 in the Week 4 Module in Canvas. 

> 1. Start with a 90% confidence interval and the population for standard deviation. 
> 2. Change Sample Size to 15 and “# of Simulations” to 1. 
> 3. This means you are just taking 1 sample of n = 15. This is most similar to what we do “in the real world”. We only take one sample to estimate a parameter form that sample. 

> a. (1 point) Does your 90% confidence interval contain the true mean? 

Yes

> b. (1 point) Increase “# of Simulations” to 1000. Theoretically, 90% of the sample means we obtain should result in an interval that contains the true parameter. Does this seem to be the case? 

Yes. 89.9%

> c. (1 point) What type of sample will fail to capture the true parameter? 
> • Decrease “# of Simulations” to 100. The intervals that don’t contain the true mean are indicated in red. You can hover over a sample mean (dot in center of interval) to see it’s value and the interval’s margin of error.  

> • Is there a common feature from the intervals that do not contain the true mean?

All their standard deviations are the same. +- 10.699

> • Where are their sample means with respect to the sample means of the intervals that do contain the parameter? 
> • Consider the placement of the sample mean in the sampling distribution. 

Their sample means are usually more than 10.7 away from the true mean. For example, 487 compared to 491. Furthermore, they are usually outliers on the distribution of sample means.

> d. (1 point) How does sample size affect your confidence intervals?
> • Continue with a 90% Confidence Level and “# of Simulations” at 100. 
• Choose a smaller sample size between 2 and 10 observe the width of your intervals. 
• Increase the sample size to something between 30 and 100 observe the width of your intervals.
• Increase your sample size to 1000 observe the width of your intervals. 
• Comment on how the different sample sizes affect the performance of the confidence intervals.

The width of my intervals decreased as the sample sizing went up. This meant that it was usually closer to the confidence interval.

> e. (1 point) How does the confidence level affect your confidence intervals?
• Continue with a 90% Confidence Level, “# of Simulations” at 100 and a moderate sample size between 30 and 100. Observe the width of your intervals.
• Increase the confidence level to 95% observe your intervals. 
• Increase the confidence level to 99% observe your intervals.
• Comment on how the different confidence levels affect the performance of the confidence intervals.

As the confidence level rating rose, the proportion percentage also rose. This means that the number of tests that capture the true mean were higher.

> Part 3: (3 points) Solving a basic hypothesis test for a mean. 
Given the following information: 

**Honestly,  I don’t know what numbers you want me to use so I just looked up a sample of this online and used their numbers. I tried a lot of things to see if my doc was broken or smth was missing so I’m just gonna be using context clues and hope for the best.**

$\bar{x} = 207$
$\sigma = 66$
$n=134$
$\alpha = .10$
$H_0: \micro = 200$
$H_a = \micro != 200$

> a. (1 point) Calculate the z test statistic and p-value.

Z Test
$$z=\frac{\bar{x}-\micro}{\sigma / \sqrt{n}} = \frac{207-200}{66 / \sqrt{134}} = 1.228$$
P Value
$$P(z \leq 1.228)=.8901$$
$$(1-.8901) * 2 = .2198$$

> b. (1 point) Draw the area under the the curve that corresponds to the p-value 
• Hint: There are many ways you can do this. In word, use the Draw feature.
• You can draw it by hand on paper, take a picture and paste it below. 

> c. (1 point) Make a conclusion. 
• State whether we should reject or fail to reject the null hypothesis based on the significance level
• Make a statement in terms of the alternative hypothesis. 

We should fail to reject the null hypothesis since .2198 > .10, our alpha. When our alpha/significance level is .10, there is no evidence that our mean is different than 200 since our p-value is .2198.

> Part 4. (12 points) A winery bottles 1000’s of bottles of wine per season. The winery has a machine that automatically dispenses the amount of wine per bottle. Each season the wine maker randomly samples 25bottles of wine to ensure the amount of wine per bottle is 750 ml. If there is evidence that the amount is different than (less or more than) 750 ml the winery will need to evaluate the machine and perhaps rebottle or consider selling the wine at a discount. The sample yields a mean of   745.4 ml. Assume the population is Normal, with a standard deviation of 9.9 ml.  Use a significance level of 0.05

$x=745.4, n = 25, \sigma = 9.9, \alpha= .05$

> State: Is there sufficient evidence that the average fill of the wine bottles is different than 750 milliliters?
> Plan:

> a. (2 points) State the null and alternative hypotheses to answer the question of interest. 

$H_0:\micro=750$
$H_a:\micro$ != $750$

> b. (2 points) Check conditions for inference. List the conditions and state whether they are met. 

Conditions:
Random: Yes, 25 random bottles
Approximately Normal: Yes
$\sigma$: Yes, 9.9

> Solve:

> c. (1 point) Calculate the test statistic. Show work. 

$$z=\frac{\bar{x}-\micro}{\sigma / \sqrt{n}} = \frac{745.5-750}{9.9 / \sqrt{25}} = -2.32$$

> d. (2 points) Draw the distribution for the test statistic and shade the region corresponding to the p-value(your sketch does not have to be perfect, but it should be clear what distribution the test statistic follows). What is the p-value for the test? 

$P(z \leq -2.32) = .0102$
$.0102 * 2 = .0204$
The p-value is .0204 
.0204 < .05

> e. (1 point) Calculate a 95% confidence interval for µ. Show work.

$$\bar{x} \pm Z_\sigma*(\frac{\sigma}{\sqrt{n}})=745.4\pm1.96*1.98=745.4 \pm 3.881=749.281 \text{ or }741.518$$

$Z_\sigma=1.96$ for 95% confidence
$SE=\frac{9.9}{5}=1.98$
$\bar{x}=745$

The interval is $[741.518, 749.281]$

> Conclude:

> f. Write a four-part conclusion describing the results. 
• (1 point) Provide a statement in terms of the alternative hypothesis. 
• (1 point) State whether (or not) to reject the null.
• (1 point) Give an interpretation of the point and interval estimate.  
• (1 points) Include context.

There is convincing evidence that the average fill of wine bottles is different than 750ml, often less.
We reject the null hypothesis because the p-value is .0204 which is less than the $\alpha$ of .05.
Our samples estimates there to be an average fill of 745.5 ml with a 95% confidence interval of  $[741.518, 749.281]$.
Since there is evidence that the amount is different than 750 ml, and usually lower than 750ml for that matter, the winery will need to evaluate the machine and perhaps rebottle or consider selling the wine at a small discount. 