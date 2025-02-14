Z Critical Value (also, percentiles $x_p$) ```qnorm(1-(confidence_interval/2))```
Normal CDF (never forget to convert to a Z score)`pnorm(z, mean=0, sd=1, lower.tail=TRUE)`
Binomial PMF (point) `dpois(x, n, probability)`
Binomial CDF (cumulative) `dpois(x, n, probability)`
Poisson CDF `ppois(x)`
Poisson PMF `dpois(x)`
Exponential CDF `pexp(x, lambda)`
Exponential Inverse CDF - find percentiles $x_p$ `qexp(p, lambda)`


P Value for ANOVA F Test(confidence, degrees freedom treatment, degrees freedom error) `pf(z, df1, df2)`
F Value Cutoff(confidence, degrees of freedom num, dof denom) `qf(z, df1, df2)`
t-critical value `qt(alpha, df)`
- .975 corresponds to 95% confidence (for 2 tailed?)
- alpha is (1-confidence) and (1-confidence)/2 for 2 tailed
p-values for T test `pt(t-statistic, df)`


t test example w rnorm `t.test(x, mu=0, alternative=“less”,conf.level=.95)`
```r
# Given data
x_bar <- 15.68  # Sample mean
s <- 0.64       # Sample standard deviation
n <- 24         # Sample size
mu0 <- 16       # Hypothesized population mean

# Simulate data using the sample mean and standard deviation
set.seed(123)  # For reproducibility
simulated_data <- rnorm(n, mean = x_bar, sd = s)

# Perform the one-sample t-test
t_test <- t.test(simulated_data, mu = mu0, alternative = "less", conf.level = 0.99)

# Print the results
t_test
```

ANOVA Summary Example
```r
# Define the data
Wheat <- c(5.2,4.5,5.9,6.1,6.8,5.7)
Barley <- c(6.6,8.1,6.0,7.4,5.8,5.6)
Maize <- c(5.9,4.8,6.4,4.8,5.9,5.1)
Oats <- c(8.2,6.0,7.7,6.9,5.5,7.2) 

# Combine into a dataframe
grain_data <- data.frame(
  Thiamin = c(Wheat, Barley, Maize, Oats),
  GrainType = rep(c("Wheat", "Barley", "Maize", "Oats"), each = 6)
)

# Perform ANOVA
anova_result <- aov(Thiamin ~ GrainType, data = grain_data)

# View ANOVA summary
summary(anova_result)
```


Linear Regression Model Summary + Residual Summary + find $\beta_2$ confidence interval
```r
# Assuming 'model' is the fitted multiple linear regression model
new_data <- data.frame(x1 = 1300, x2 = 7)

x1 = c(1250,1300,1350,1250,1300,1250,1300,1350,1350)
x2 = c(6,7,6,7,6,8,8,7,8)
y = c(80,95,101,85,92,87,96,106,108)
mod = lm(y~x1+x2)
summary(mod)
residuals(mod)
cor(x1, y)

# Predict the mean response with a confidence interval
predict(mod, newdata = new_data, interval = "confidence", level = 0.95)

# Extract coefficients and standard errors
coefficients <- summary(mod)$coefficients
beta_2 <- coefficients["x2", "Estimate"]
SE_2 <- coefficients["x2", "Std. Error"]
df2 <- 6
t_star <- qt(.975, df2)

# Compute confidence interval
lower_bound <- beta_2 - t_star * SE_2
upper_bound <- beta_2 + t_star * SE_2

# Print rounded results
round(c(lower_bound, upper_bound), 3)```
$\sigma$ is known as residual std error
$\hat{y}$ is predicted y
lwr, upr is lower and upper confidence intervals (for $\micro$ when given specific x and y values)
lower_bound and upper_bound are the formulas for confidence intervals (specific vars)
df2 is degrees of freedom (error/total)


Calculate $R^2$ and F Stat given SSR and SSE

```R
# Input the given values
n <- 33  # Number of observations
k <- 6   # Number of predictors
SSR <- 779.5  # Sum of Squares Regression
SSE <- 311.8  # Sum of Squares Error

# Calculate SST
SST <- SSR + SSE
print(paste("SST:", SST))

# Calculate R-squared
R_squared <- SSR / SST
print(paste("R-squared:", R_squared))

# Calculate Adjusted R-squared
Adjusted_R_squared <- 1 - (SSE / (n - k - 1)) / (SST / (n - 1))
print(paste("Adjusted R-squared:", Adjusted_R_squared))

# Calculate F-statistic
F_statistic <- (SSR / k) / (SSE / (n - k - 1))
print(paste("F-statistic:", F_statistic))
```

Probability and Z Scores (multi var regression)
```r
# Given values
mu_y <- 5 + (0.007 * 78) - (0.05 * 22) - (0.09 * 10) - (0.01 * 138)
sigma <- 0.4

# Compute probabilities using the standard normal distribution
lower_bound <- 1.406
upper_bound <- 2.926

# Convert to z-scores
z_lower <- (lower_bound - mu_y) / sigma
z_upper <- (upper_bound - mu_y) / sigma

# Compute probability
prob <- pnorm(z_upper) - pnorm(z_lower)

# Display result
prob
```