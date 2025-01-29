```r
# Upload the epa data set 
# call the dataset available on DA 6 page on Canvas

cardata <- read.csv(file.choose(), header = TRUE)

View(cardata)

# Create a side by side boxplot. 
# Give the plot an appropriate title and x-axis
boxplot(EPACalculatedAnnualFuelCost~trans, data = cardata, 
        main = "add title", 
        xlab = "add horizontal axis name",
        col = c("red", "green"), ### add different color names
        horizontal = TRUE)

# Calculate the mean, sd and sample sizes for annual fuel cost split among automatic and manual
# The command aggregate() will perform the given function on the specified groups
# aggregate(response~treatment, data = datasetname, function)
# Make a table of values with the results. 

aggregate(EPACalculatedAnnualFuelCost~trans, data = cardata, mean)
aggregate(EPACalculatedAnnualFuelCost~trans, data = cardata, sd)
aggregate(EPACalculatedAnnualFuelCost~trans, data = cardata, length)

# Perform a two sample t test 
# In the code below, replace the following items: response with the response variable, 
# treatment with the name of the grouping variable, datasetname with the name of the 
# dataset, and enterconfidencelevel with the desired confidence level (value between 0 and 1)

t.test(response~treatment, data = datasetname, conf.level = enterconfidencelevel, alternative = "two.sided" )


```