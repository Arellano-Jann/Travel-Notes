```r
# Read in the microbeers_Winter2024.csv dataset
microbeers = read.csv(file.choose(), header = TRUE)

# gives variable names.
names(microbeers) # gives variable names. 

# Make an appropriate visual display for abv. 
# Recall hist() or boxplot()
# Add a title. 
# Add color and other aesthetics if you like. 
# See week 3 lessons or the script from Data Analysis #3. 

# Calculate the mean and standard deviation. mean() and sd()
# Again week 3 lessons or the script from Data Analysis #3. 

# Perform a t test using the t.test() command. The coded need to do this
# begins at line 33. 
# The format is t.test(data, mu = mu_0, alternative = "alt") 
# where data is a quantitative variable mu_0 is the hypothesized mean,
# and alt is either "less", "greater" or "two.sided" (default).

# After running the t.test() function, you'll be given a few lines of 
# output including: 
# the test statistic (look for t = )
# the degrees of freedom (look for df = )
# the p-value (look for p-value = or pvalue < )
# a statement describing the alternative hypothesis
# a confidence interval based on the value set in the conf.level = argument
# the point estimate for the population mean

t.test(microbeers$abv, 
       alternative = "two.sided", 
       mu = 5, conf.level = 0.95)
```