## HW 1
Bayes Theorem
$$P(A | B) = \frac{P(B | A) P(A)}{P(B)}$$
Percentiles
$$P(x< x_{p/100})=\frac{p}{100}$$
Notes: pdf -> cdf we integrate
Binomial 
- pmf
	- $$P(k)=(\frac{n!}{k!n!})(p)^k(1-p)^{n-k}$$
- E(x)
	- $np$
- V(x)
	- $np(1-p)$
Poisson 
- pmf
	- $P(x) = \frac{\lambda^xe^{-\lambda}}{x!}$
- E(x)
	- $\micro = \lambda$
- V(x)
	- $\sigma^2 = \lambda$
Exponential Distribution
- pdf (0 when below 0)
	- $f(x) = \lambda e^{-\lambda x}$
- E(x)
	- $\micro = \frac{1}{\lambda}$
- V(x)
	- $\sigma^2 = \frac{1}{\lambda^2}$


## HW 4
Confidence Interval - Point Estimate $\pm$ Margin of Error
$$CI=\bar{X}\pm Z_{\sigma/2} \times \frac{\sigma}{\sqrt{n}}$$
where:
- $X$ = sample mean
- $Z_\sigma$ = crit value (or t_crit/$t^*$)
- $\sigma$ = SD
- $n$ = sample size

- Find sample size given margin or error
	- $$(Z_{\sigma/2} \times \frac{\sigma}{ME})^2= n$$


Confidence Interval for proportion
$$CI=\hat{p}\pm Z_{\alpha/2} \times \sqrt{\frac{\hat{p}(1-\hat p)}{n}}$$

- where p is proportion from $\text{sample}/\text{population}$
- Find Sample Size
	- $$(\frac{z_{\alpha/2}}{ME})^2\times p(1-p)$$
Confidence Interval for $\mu$ when $\sigma$ unknown
$$CI=\bar{X}\pm t_{n-1,\alpha/2} \times \frac{s_x}{\sqrt{n}}$$

Standard Error/Standard Deviation
- also converts population SD to sample SD.
$$\frac{\sigma}{\sqrt{n}}$$

Z Score
- $$\frac{\bar{X}-\micro}{\sigma}$$
- $$\frac{\hat p - p}{\sqrt {(\hat{p}(1-p))/n)}}$$

Z Statistic
$$\frac{\bar{X}-\micro}{\sigma/\sqrt{n}}$$

Hypothesis
(convincing < .01, moderately suggestive < .05, slightly suggestive < .10)

4 Part Conclusion
- There is convincing evidence that the average abv of craft beers is different from 5%.
- Since the p-val is below the significance level of .01, at $3.55*10^{-5}$, we reject the null hypothesis.
- With a 95% confidence interval, we can estimate that the average abv of craft beers is between 5.407 and 6.08. 
- Since 5 is below these values, we can safely say that the average abv of craft beers is different from 5%. In fact, we can say that the avg abv of craft beers is greater than 5% given that our confidence interval values are above 5%.
## DA 5
Z Test Proportion
- Use: when testing the avg val $p$ from a single population
- Conditions
	- Random Sample
	- Normality
		- $np \geq 10$
		- $n(1-p) \geq 10$

Z Critical ($z_{1-\alpha/2}$) (at least for $p$)
- 90% Confidence - 1.645
- 95% Confidence - 1.96
- 99% Confidence - 2.576
- use always unless not given $\sigma$, then resort to the T Critical
T Critical
- use when not given $\sigma$ and instead given $s$, the sample SD
![[../../Ignored/Pasted image 20250213090438.png]]

Test Statistic
- Z Stat$$\frac{\hat{p}-p_0}{\sqrt{p_0*(1-p_0)/n}}$$
- T Stat $$\frac{\bar{x}-\mu_0}{s/\sqrt n}$$
## DA6 
T Procedure for Different Means
- Matched Pair T Stat
- 2 Sample
	- Test Statistic$$\frac{\bar{x}_1 - \bar{x}_2 -\delta}{\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}$$
	- Confidence Interval $$(\bar x_1 - \bar x_2)\pm(t_{v,a/2)})(\sqrt{ \frac{s_1^2}{n_1} + \frac{s_2^2}{n_2} })$$
	- t crit
		- 2 tailed - 95% = .975

## HW 6
deg of freedom (between groups) $$df_{1}=I-1$$
deg of freedom (within groups)$$df_{2}=I(j-1)$$
Treatment deg of freedom $$df_{Tr}=k-1$$
Error deg of freedom $$df_{E}=N-k$$

MSTr Mean Square for Treatment
$$\text{MSTr} = \frac{SSTr}{df_{Tr}}=\frac{J}{I-1}\Sigma^I_i(\bar{x}_{i.}-\bar{x}_{i..})^2$$
- $J$ = observations in each group, $n_i$
- $I$ = population
- $\bar{x_i}$ = mean for sample $i$
- $\bar{x}_{i..}$ = grand mean for all $i$
- $n_i$ = size for sample i
MSE Mean Square for Error
$$\text{MSE}=\frac{SSE}{df_{E}}=\frac{1}{I}\Sigma^j_is_i^2$$
- $\bar{s_i}$ = std for sample $i$
F Test Statistic
$$F=\frac{MSTr}{MSE}$$
## DA 7
Population Regression Equation
$$Y=\beta_0+\beta_1x+\epsilon$$
Confidence interval for a slope
$$b_1\pm(t_{n-(k+1),\alpha/2})(SE_{b1})$$
- $SE_{b1}$ is a complicated equation so we don’t care.
## HW 8
SST Total Sum Of Squares
$$SST=SSR + SSE$$
Coefficient of Determination $R^2$
$$R^2=\frac{SSR}{SST}$$

Adjusted Coefficient of Determination $R^2$
$$R^2=\frac{SSR/(n-k-1)}{SST/(n-1)}$$
- $n$ = observations
- $k$ = predictors

Deg freedom Predictors$$df_1=k$$
Deg freedom Denominator$$df_2=n-k-1$$

F Statistic
$$F=\frac{SSR/k}{SSE/(n-k-1)}=\frac{R^2/k}{(1-R^2)/(n-k-1)}$$

## HW 10