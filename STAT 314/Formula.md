## HW 1
Bayes Theorem
$$P(A | B) = \frac{P(B | A) P(A)}{P(B)}$$

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


## HW 4
Confidence Interval
$$CI=X+Z_\sigma \times \frac{\sigma}{\sqrt{n}}$$
where:
- $X$ = sample mean
- $Z_\sigma$ = crit value (or t_crit/$t^*$)
- $\sigma$ = SD
- $n$ = sample size

Standard Error
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
T Critical T Table

| df    | Cum. Prob | t .50 | t .75 | t .80 | t .85 | t .90 | t .95 | t .975 | t .99 | t .995 | t .999 | t .9995 |
|-------|----------|------|------|------|------|------|------|------|------|------|------|------|
| one-tail  | 0.50 | 0.25  | 0.20  | 0.15  | 0.10  | 0.05  | 0.025 | 0.01  | 0.005 | 0.001 | 0.0005 |
| two-tails | 1.00 | 0.50  | 0.40  | 0.30  | 0.20  | 0.10  | 0.05  | 0.02  | 0.01  | 0.002 | 0.001  |
| 1     |  ∞      | 1.000 | 1.376 | 1.963 | 3.078 | 6.314 | 12.71 | 31.82 | 63.66 | 318.31 | 636.62 |
| 2     | 0.000   | 0.816 | 1.061 | 1.386 | 1.886 | 2.920 | 4.303 | 6.965 | 9.925 | 22.327 | 31.599 |
| 3     | 0.000   | 0.765 | 0.978 | 1.250 | 1.638 | 2.353 | 3.182 | 4.541 | 5.841 | 10.215 | 12.924 |
| 4     | 0.000   | 0.741 | 0.941 | 1.190 | 1.533 | 2.132 | 2.776 | 3.747 | 4.604 | 7.173  | 8.610  |
| 5     | 0.000   | 0.727 | 0.920 | 1.156 | 1.476 | 2.015 | 2.571 | 3.365 | 4.032 | 5.893  | 6.869  |
| 6     | 0.000   | 0.718 | 0.906 | 1.134 | 1.440 | 1.943 | 2.447 | 3.143 | 3.707 | 5.208  | 5.959  |
| 7     | 0.000   | 0.711 | 0.896 | 1.119 | 1.415 | 1.895 | 2.365 | 2.998 | 3.499 | 4.785  | 5.408  |
| 8     | 0.000   | 0.706 | 0.889 | 1.108 | 1.397 | 1.860 | 2.306 | 2.896 | 3.355 | 4.501  | 5.041  |
| 9     | 0.000   | 0.703 | 0.883 | 1.100 | 1.383 | 1.833 | 2.262 | 2.821 | 3.250 | 4.297  | 4.781  |
| 10    | 0.000   | 0.700 | 0.879 | 1.093 | 1.372 | 1.812 | 2.228 | 2.764 | 3.169 | 4.144  | 4.587  |
| 20    | 0.000   | 0.687 | 0.860 | 1.064 | 1.325 | 1.725 | 2.086 | 2.528 | 2.845 | 3.552  | 3.850  |
| 30    | 0.000   | 0.683 | 0.854 | 1.055 | 1.310 | 1.697 | 2.042 | 2.457 | 2.750 | 3.385  | 3.646  |
| 40    | 0.000   | 0.681 | 0.851 | 1.050 | 1.303 | 1.684 | 2.021 | 2.423 | 2.704 | 3.307  | 3.551  |
| 60    | 0.000   | 0.679 | 0.848 | 1.045 | 1.296 | 1.671 | 2.000 | 2.390 | 2.660 | 3.232  | 3.460  |
| 80    | 0.000   | 0.678 | 0.846 | 1.043 | 1.292 | 1.664 | 1.990 | 2.374 | 2.639 | 3.195  | 3.416  |
| 100   | 0.000   | 0.677 | 0.845 | 1.042 | 1.290 | 1.660 | 1.984 | 2.364 | 2.626 | 3.174  | 3.390  |
| 1000  | 0.000   | 0.675 | 0.842 | 1.037 | 1.282 | 1.646 | 1.962 | 2.330 | 2.581 | 3.098  | 3.300  |
| z     | 0.000   | 0.674 | 0.842 | 1.036 | 1.282 | 1.645 | 1.960 | 2.326 | 2.576 | 3.090  | 3.291  |

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