## HW 1
Bayes Theorem
$$P(A | B) = \frac{P(B | A) P(A)}{P(B)}$$
Percentiles
$$P(x< x_{p/100})=\frac{p}{100}$$

Binomial 
- pmf
	- $P(x) = p^x(1-p)^{n-x}$
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

Standard Error/Standard Deviation
- also converts population SD to sample SD.
$$\frac{\sigma}{\sqrt{n}}$$

Z Score
$$\frac{\bar{X}-\micro}{\sigma}$$
Z Statistic
$$\frac{\bar{X}-\micro}{\sigma/\sqrt{n}}$$
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
T Critical
![[../../Ignored/Pasted image 20250213090438.png]]

Test Statistic, z statistic
$$\frac{\hat{p}-p_0}{\sqrt{p_0*(1-p_0)/n}}$$

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