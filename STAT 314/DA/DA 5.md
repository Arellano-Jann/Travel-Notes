> Part 1. (6 points) Match the Scenario to the Test. There is one of each of the following tests described in the scenarios: one sample z test for the population mean, one sample t test for the population mean, and a one sample z test for the population proportion.  For each scenario decide what type of hypothesis testing procedure is appropriate and explain why. 

> Scenario 1. A manufacturer of seat belts routinely samples the strength of seat belts to ensure their product meets specifications. Past experience has indicated the breaking strength of seat belts is normally distributed with a standard deviation of . A random sample of 16 specimens yields an average breaking strength of 2003 psi.  What type of procedure is appropriate to test whether the mean is other than the desired 2000 psi?

T Test for population mean because the sample size is small, 16. We need to use the t distribution

> Scenario 2. In an effort to support students beyond tuition assistance, a philanthropy group would like to provide eligible students with a monthly amount for food and groceries. They would like to know if $300 a month is a reasonable amount to support a student. A report from a University’s housing and dining department claims students spend on average $315 on food and groceries per month with a standard deviation $126. They assume this data from a random sample of 161 students represents the population. Which procedure is appropriate to investigate whether $300 is not a reasonable amount per month, on average?

Z test for population mean because the sample size is large enough for a normal distribution, 161.

> Scenario 3. During a viral pandemic, a state applies a tiered risk assessment to counties based on the proportion of residents who test positive for the virus. Suppose a county randomly samples and tests 1000 residents for the virus every two weeks. If the proportion of positive tests is more than 0.01, the county is assessed as high risk.Which procedure is most appropriate to test whether the proportion for positive tests is more than 1%? 

Z test for population proportion because the sample size is large, 1000, and we are testing for proportion.

> Part 2. (9 points) Suppose a new initiative is interested in increasing the percent of students who identify as female to pursue an engineering or computer science degree. A university will receive funding to actively market to these students if there is evidence that less than 1 in 3 engineering or computer science students identify as female.  Use the information presented in the bar graph below to answer the following questions.
> Is there evidence the proportion of all OSU engineering students who identify as female is less than 0.33? Use a significance level of 0.01.    

> a. (0.5 points) Based on the bar chart of the data is there evidence the proportion of those who identify as female is less than 0.33? How many students are in the sample?   

Based on the bar chart, the proportion of female students seem to be around 0.2. So, yes it’s less than .33. Furthermore, there are 111 students in the sample. (24 + 85 + 2 = 111)

> b. (1 point) State the null and alternative hypotheses.  

$H_0$: $p\geq.33$ bc we are seeing if female proportion is at least .33
$H_a$: $p<.33$ bc we are testing if female proportion is less than .33

> c. (0.5 points) Do you think it is appropriate to use the ST314 Student Survey data to represent the population of all OSU engineering students? Why or why not?  

No. It needs to span multiple classes as there may be bias towards a certain engineer if we just consider the ST314 student group. For example, in our greetings of this semesters survey data, we have a majority of CS majors which is certainly not representative of the vast amount of engineering majors. I think a better survey may be Calculus students who are engineers. Of course, this is given that the survey data being collected is random too.

> d. (1 point) Check conditions. Are they met? If not, still proceed.  

Conditions:
Random and Representative: Yes, 111 random students out of the seemingly large population of OSU students
Approximately Normal: Yes, greater than 10
$\sigma$: No, we don’t know but we don’t need it.

Checking for normality
$np = 111*0.33 = 36.63\geq 10$ 
$n(1-p) = 111*(1-0.33) = 74.37 \geq 10$ 

> e. (1 point) Calculate the test statistic. Show work!  

Test Statistic, z statistic
$$\frac{\hat{p}-p_0}{\sqrt{p_0*(1-p_0)/n}}$$
$$\frac{(24/111)-.33}{\sqrt{.33*(1-.33)/111}}=\frac{-.1138}{\sqrt{.001991}}=-2.55$$

> f. (0.5 point) Give the appropriate p-value and state whether it is one-sided or two-sided.   

$P(z < -2.55) = .00538$
1 Sided test, .00538 < .01, reject $H_0$

> g. (1.5 point) Calculate the appropriate 99% confidence interval. Show work!   

$$\hat{p}\pm z_{a/2} \times \sqrt{\frac{\hat{p}(1-\hat{p})}{n}}$$
$$\hat{p}=24/111=.2162$$
$$.2162\pm 2.576 \times \sqrt{\frac{.2162(1-.2162)}{111}}$$
$$.2162\pm 2.576 \times \sqrt{.001526}$$
$$.2162\pm .1007$$
$$[.1155,.3169]$$

> h. (3 points) Finally, using the results from parts e, f and g, summarize your conclusions to the university. Construct a four-part conclusion, which includes a statement in terms of the alternative, whether you reject or fail to reject the null based on a significance level, state and interpret the confidence intervaland point estimate and include context.

There is convincing evidence that the proportion of female engineering students is less than .33.
Since the p-val is below the significance level of .01, at .0054, we reject the null hypothesis.
With a 99% confidence interval, we can estimate that the proportion of female engineering students is between .1155 and .3169. 
Since .33 is not within these values, we can safely say that the proportion of female engineers is less than .33.

> Part 3. (8 points) The microbeers_Winter2024.csv dataset is a random sample of 75 microbrews from around the United States. The variable “abv” represents the percent of alcohol by volume for each craft beer. According to the National Institute of Health, one standard serving of alcohol is usually about 5% alcohol by volume (abv). 
Does the sample of microbrews provide evidence the average alcohol by volume of all craft beers is different from a standard serving of beer at 5% abv?
Use this dataset and the R script DA5_t_procedures.R to complete the following:

> a. (0.5 point) What is the parameter of interest in this scenario? Provide the symbol and context.   

The abv of craft beers is different from 5%. 
$\micro$ = Population mean of abv of all craft beers


> b. (1 point) State the null and alternative hypothesis to answer the question of interest.   

$H_0$: $\micro = 5$ bc we are seeing if abv is 5%
$H_a$: $\micro\neq 5$ bc we are testing if abv is different from 5%

> c. (1.5 points) Make a histogram or boxplot to visualize the variable abv.  Is there visual evidence the average alcohol by volume is different than 5%?  

Do we paste the plot LOL. It doesn’t say to so I’m not going to…
No it looks like the average ABV isn’t different from 5%. There are outliers going up to almost 10%. However, 5% is within the IQR, albeit on the lower end. Furthermore, there is a bunch of craft beers that are at the 5% which bring the mean/average more towards 5%.

> d. (1 point) Check the conditions for inference. State them and whether they are met.   

Conditions:
Random and Representative: Yes, 75 random craft beers
Approximately Normal: Yes, the histogram looks bell shaped
$\sigma$: No, we don’t know but we don’t need it.


> e. (1 point) Use the t.test() command in R to perform the test. Paste your results.  

![[../../../Ignored/IMG_2956.jpeg]]

> f. (3 points) From the R output, write a four-part conclusion describing the results. Use . Provide a statement in terms of the alternative hypothesis. State whether (or not) to reject the null. Give in context an interpretation of the point and interval estimate.  Include any other information you might feel to relevant.

There is convincing evidence that the average abv of craft beers is different from 5%.
Since the p-val is below the significance level of .01, at $3.55*10^{-5}$, we reject the null hypothesis.
With a 95% confidence interval, we can estimate that the average abv of craft beers is between 5.407 and 6.08. 
Since 5 is below these values, we can safely say that the average abv of craft beers is different from 5%. In fact, we can say that the avg abv of craft beers is greater than 5% given that our confidence interval values are above 5%.