The dataset ST314ExamData_DA8.csv represents the midterm and final exam grades for students in the ST314 online and campus courses, for two previous terms. Use this data to complete a multiple linear regression analysis in R and answer the following questions.   
  
Note: the data set used in this assignment is different from last week’s. Please make sure you are loading the csv file listed on the Data Analysis 8 Canvas page. 

Final = Final Exam Score out of 100

Midterm = Midterm Exam Score out 100

Term = Has two levels Fall 2021 and Spring 2022

Format = Has two levels Campus and Online 

Part 1. (6 points) Multivariate Visualization:

It is reasonable to consider that more than just midterm score may influence final exam score. Investigate the individual relationships between final exam score and the above explanatory variables. Use the R script Multivariate_Exam_Analysis.R to help you get started with the code. 

a. Construct a scatterplot matrix including final and each of the explanatory variables. 

i. (1 point) Paste the plot. 

ii. (1 point) Do any of the variables have a visual relationship with Final?  

b. The scatterplot matrix is not all that helpful for the categorical variables Term and Format. 

i. Create a side by side boxplot that looks at the relationship between Term and Final. 

• (1 point) Paste your plot. 

• (1 point) Describe the relationship. Visually does Term seem to have a relationship with Final?  

ii. Create a side by side boxplot that looks at the relationship between Format and Final. 

• (1 point) Past your plot. 

• (1 point) Describe the relationship. Visually does Format seem to have a relationship with Final?  

Part 2. (7 points) Fit a Model 

Fit a model that includes Term, Format and Midterm as explanatory variables for the response variable Final.    

a. (1 point) Provide the R output of the model.

b. (2 points) State the least squares regression equation of your model.

c. The model without the variables Term and Format has an adjusted R2 value of 0.1274.

i. (1 point) Does including the variables Term and Format improve the fit of the model? 

ii. (1 point) Interpret the adjusted R2 value for the model that includes all three explanatory variables. 

Part 3. (10 Points) Model interpretation.

Note: Model Interpretation can get tricky when there is more than two levels in a factor. For example, Term has three levels instead of two. The R output will designate this as VariableLevel, like “TermSpring 22”. 

In the model, the coefficient for TermSpring 22 is 1.2171 this means that while the other variables in the model are held constant, a student taking the exam in the spring 2022 will score 1.2171 points more on average than a fall 2021 student. We know to TermSpring 22 is compared to fall, because Fall 2021 is the variable not included in the output. Meaning, fall is represented when spring is at 0. 

a. (2 point) Interpret each of the individual t tests by stating which variables are significant at 0.05, when the other variables are in the model.  

b. (2 points) Interpret in context the coefficient for Format.  

c. (2 points) Interpret in context the coefficient for TermSpring22.  

d. (2 point) Interpret in context the coefficient for the Midterm variable.

e. (2 points) Calculate the 95% confidence interval for . Show work. Interpret the interval.

Part 4. (2 points) Prediction. 

a. (2 points) Use the least squares regression equation to predict final exam score for a fall, online student with a midterm score of 85.