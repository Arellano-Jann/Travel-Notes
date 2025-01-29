```R
#### PART 1 ####


############# Getting a Data File into R ##############################
# Download the data set st314-student-survey.csv from Canvas to your computer.
# Don't change anything about the dataset. 
# Simply download and save to familiar location.
# Upload Dataset using the read.csv() command below. 
# file.choose() will open a search window for you to select the file.
# Note your data is called cardata.population

st314data <- read.csv(file.choose(), header = TRUE)


# Look at the names of the variables in the data with names()

names(st314data)

# Look at the first six rows of data with head()

head(st314data)

# Look at the size of the dataset with nrow()
# n is the number of rows or students in the sample
n <- nrow(st314data)
n

# Choose a categorical variable to make a table of counts and a bar chart. 
# To choose a variable from the dataset
# dataset$variable, $ tells R "use this variable from this dataset".

# Example: st314data$SubjectPreffered 
# CHOOSE A DIFFERENT CATEGORICAL VARIABLE FOR YOUR OWN ANALYSIS!

table(st314data$SubjectPreferred)
barplot(table(st314data$SubjectPreferred), 
        main = "Subject Preferred by ST314 Fall Students",
        col = c("blue","green"),
        cex.names = 0.5,
        las = 2)

# Choose a quantitative variable to visualize. 
# To choose a variable from the dataset
# call the dataset followed by $ and the variable name 
# Example: st314data$Email

# CHOOSE A DIFFERENT QUANTITATIVE VARIABLE FOR YOUR ANALYSIS!

# Make a histogram of your variable of interest 
# Use the hist() command and define the variable from the dataset. 
# dataset$variable, $ tells R "use this variable from this dataset". 

hist(st314data$Email)

# The basic histogram is ugly. Should add a title and some color. 
# Add a title with main = " Title" 
# Add x axis or y axis labels, xlab = " xlabel", ylab = "ylabel" 
# Add color with col = "blue" (or "red" or "orange" etc...)
# More graphical options can be explored at help(hist)

hist(st314data$Email, 
     main = "ST314 Fall 2020 Students: Email Count", 
     xlab = "Number of emails over 24 hour period", 
     col = "dodgerblue")

# Now create a boxplot. 
# Should add a title and some color. 
# Add a title with main = " Title" 
# Add x axis or y axis labels, xlab = " xlabel", ylab = "ylabel" 
# Add color with col = "blue" (or "red" or "orange" etc...)
# Graphical options are the essentially the same as histogram. 
# More graphical options can be explored at help(boxplot)

boxplot(st314data$Email, 
     main = "ST314 Fall 2020 Students: Email Count", 
     xlab = "Number of emails over 24 hour period", 
     col = "dodgerblue")

# This plot is vertical. 
#Make is horizontal by adding , horizontal = TRUE) 

boxplot(st314data$Email, 
        main = "ST314 Fall 2020 Students: Email Count", 
        xlab = "Number of emails over 24 hour period", 
        col = "dodgerblue", horizontal = TRUE)

# Calculate the summary statistics for your chosen variable. 

# Calculate the "Five Number Summary" and the mean with summary()
summary(st314data$Email)

# Calculate the Sample Standard Deviation sd()
sd(st314data$Email)



#### PART 2 ####

# Randomly sample 10 of the rows from the st314data data frame
# In the code below, we first specify the data set we want to subset: st314data
# The square brackets [ , ] then indidcate what rows and columns of the data set
# we want to keep.
# The argument before the comma specifies the rows to subset.
# The argument after the comma specifies the columns to subset.
# We'll use the sample() function to determine which 10 randomly select rows will
# be used in the sample. 

# sample(1:n, 10) will randomly sample 10 numbers between 1 and n (the number of rows
# in the original data set). 
# Run the line below. Your sample of 10 students will be stored in the object called sampled_data.

sampled_data <- st314data[sample(1:n, 10), ]

# Use the summary statistic functions and plotting functions from part 1 to answer 
# the questions in part 2 of the assignment using your sampled_data data set.
```