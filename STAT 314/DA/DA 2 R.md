```R
# PART 2 ############################################## 
###### Enter Gamma parameter values ###################
# Alpha and Beta may be any positive values. 
alpha = 2
beta = 4

# Define Number of Observations  
observations = 1000

####### Simulation ####################################
####### HIGHLIGHT AND RUN ENTIRE SECTION ##############
####### You may run this multiple times  ##############

#Simulates Gamma Random Variable 
RV = rgamma(observations,alpha,1/beta)

# Plots Random Variable
hist(RV, freq = FALSE, col = "dodgerblue", breaks = 100, 
     main = "Gamma Random Variable Values with Density Curve", 
     xlim=c(0,max(RV)+sqrt(alpha*beta^2)))

# Plots Probability Density Curve
x.range =  seq(0, max(RV)+2*sqrt(alpha*beta^2), 0.01)
pdf = dgamma(x.range,alpha,1/beta)
lines(x.range, pdf, lwd = 4)

#Actual Proportion of values below 6
Proportion = sum(RV<6)/observations
Proportion

##### End of Simulation ################################
```