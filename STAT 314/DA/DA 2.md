Part 1.  (6 points) Identify the distribution

> Random Variable 1. (2 points)
A board game buzzer is set to a random time increment anywhere between 45 and 120 seconds. Consider time until the buzzer sounds a random variable where any time between 45 and 120 has an equal likelihood. Players of the game must guess a phrase from clues given by their teammates before the buzzer sounds. 

> a. State the distribution that will best model random variable. Choose from the common continuous distributions: Uniform, Exponential or Normal distribution. Explain your reasoning. 

This is a classic uniform distribution because the random variable has the same probability of occurring from the endpoints (45 and 120). Keywords are: equal likelihood.

> b. State the parameter values that describe the distribution. 

A = 45, B =120

> c. Give the probability density function. 

$$
f(x) =
\begin{cases}
\frac{1}{b - a}, & a \leq x \leq b \\
0, & \text{otherwise}
\end{cases}
$$


> Random Variable 2. (2 points)
The time between patients arriving at an emergency room is a random variable. During a one-hour period, a staff member measures the time between successive patients and finds that, on average, the time between patients is 7 minutes. Furthermore, they observe that times are more likely to be close to 0 and less likely as they get further from 0. 

> a. State the distribution that will best model random variable. Choose from the common continuous distributions: Uniform, Exponential or Normal distribution. Explain your reasoning. 

Exponential because it’s through a continuous period of time (1 hour) and it’s skewed towards one side. Furthermore, it models time between patients (the events).

> b. State the parameter values that describe the distribution. 

$\alpha = 1$
$\lambda = 1/7$

> c. Give the probability density function. 

$$
f(x) =
\begin{cases}
(\frac{1}{7})e^{-\frac{1}{7} x}, & x \geq 0 \\
0, & \text{otherwise}
\end{cases}
$$

> Random Variable 3. (2 points)
Steel cylinders are produced as a part of a manufacturing process. The length of the cylinder is a random variable with an average of 3.25 inches and a standard deviation of 0.009 inches. The distribution of cylinder lengths is symmetrical, where lengths are more likely to be close to the mean rather than further away from the mean. 

> a. State the distribution that will best model random variable. Choose from the common distributions: Uniform, Exponential or Normal distribution. Explain your reasoning. 

Normal distribution because it’s the only one left out of the three. Just kidding. It’s because it has an average length with a standard deviation value. It also tells us that the distribution is symmetrical and values (lengths) are closer to the mean which are all tell tale signs of a bell curve/normal distribution.

> b. State the parameter values that describe the distribution. 

$\mu = 3.25$
$\sigma = .009$

> c. Give the probability density function. 

$$
f(x) =
\frac{1}{\sqrt{2\pi(.009)^2}}e^{-\frac{(x-3.25)^2}{2(.009)^2}}, -\infty \leq x \leq \infty 
$$



> Part 2. (6 points) Normal Distributions 
> The Normal distribution curve to the right displays the distribution of grades given to managers based on management performance at Ford. Of the large population of Ford managers, 10% were given A grades, 80% were given B grades, and 10% were given C grades. A’s were given to those who scored 380 or higher and C’s were given to those who scored 160 or lower.  

> a. (2 point) What are the z scores associated with the 10th and 90th percentiles from the standard normal distribution? Recall that a z-score is value from the Standard Normal distribution and represents the number of standard deviations a value is away from its mean. 

10th = -1.28
90th = 1.28

> b. (2 point) From part a, you should have two values - the z-scores associated with the 10th and 90th percentiles. Using these two values and the mathematical definitions of a z-score, calculate the mean and standard deviation of the performance scores? Show work.

$$z=\frac{x-\mu}{\sigma}$$
$$x = z\sigma + \mu$$
$$160 = -1.28\sigma + \mu$$
$$380 = 1.28\sigma + \mu$$
$$540=2\mu$$
$$\mu=270$$
$$380 = 1.28\sigma + 270$$
$$110 = 1.28\sigma$$
$$110/1.28= 85.93 =\sigma$$
Thus $\sigma = 85.93$ & $\mu=270$

> c. (2 point) Suppose the company adds grades D and F so there are 5 categories to grade performance. If they want to give A’s only to those in the top 3%, what performance score must a manager exceed to get an A? 

They would need to be in the top 3% thus the z-score would be 1.88. Note that it would not be -1.88 because that is to the left of the curve and the top x% is on the right side.
$$\mu = 270, \sigma = 85.93, z = 1.88$$
$$x=1.88(85.93)+270$$
$$x=431.548$$




> Part 3.  (11 points) Simulation of Gamma Random Variables 
Background: When we use the probability density function to find probabilities for a random variable, we are using the density function as a model. This is a smooth curve, based on the shape of observed outcomes for the random variable. The observed distribution will be rough and may not follow the model exactly. The probability density curve, or function, is still just a model for what is actually happening with the random variable. In other words, there can be some discrepancies between the actual proportion of values above x and the proportion of area under the curve above the same value x. Our expectation is as the number of observations increase, literally or theoretically, the observed distribution will align more with the density curve. Over the long run, the differences are negligible, the model is sufficient and more convenient to find desired information.  

> Simulation:  Use R to simulate 1000 observations from a gamma distribution. To begin, set alpha = 2 and beta = 4. Highlight and run the parameters and observation values. Run the simulation code to plot the observations and fit the probability density function over the observations.  You don’t need to change anything. You may run the section all at once by highlighting all of the section and running it by clicking the run button at the top of the script window.

> a. Given the values are from a gamma distribution with alpha= 2 and beta = 4, 

> i. (1 points) What is the expression for the probability density function?
> 

$$
f(x) =
\begin{cases}
\frac{1}{4^2 \Gamma (2)}x^{2 - 1}e^{-x/4}, & x \geq 0 \\
0, & \text{otherwise}
\end{cases}
$$
$$
f(x) =
\begin{cases}
\frac{1}{4^2 * 1}x^{2 - 1}e^{-x/4}, & x \geq 0 \\
0, & \text{otherwise}
\end{cases}
$$
$$
f(x) =
\begin{cases}
\frac{1}{16}xe^{-x/4}, & x \geq 0 \\
0, & \text{otherwise}
\end{cases}
$$

> ii. (1 point) What is the average and standard deviation of the random variable? Show work in regards to how you derived these quantities. 

For avg:
$$\mu_x=\alpha\beta=2*4=8$$
For std var:
$$\sigma^2_x=\alpha\beta^2=2*4^2=32$$

> iii. (1 point) What is the probability x is less than 6? Show work.

Note that we do integration by parts because of $xe^{-x/4}$

$$P(x<6)=\int^6_0\frac{1}{16}xe^{-x/4}$$
$$u=x,dv=e^{-x/4},du=dx,v=-4e^{-x/4}$$
$$uv-\int vdu$$
$$=-4xe^{-x/4}-\int-4e^{-x/4}dx$$
$$=-4xe^{-x/4}-16e^{-x/4}$$
$$=\frac{1}{16}(-4xe^{-x/4}-16e^{-x/4})$$
$$[-\frac{1}{4}xe^{-x/4}-e^{-x/4}]^6_0$$
$$=[-\frac{1}{4}6e^{-6/4}-e^{-6/4}]-[-\frac{1}{4}0e^{-0/4}-e^{-0/4}]$$
$$=[-\frac{6}{4}e^{-6/4}-e^{-6/4}]-[0-1]$$
$$=[-\frac{6}{4}(.2231)-(.2231)]-[-1]$$
$$=[-\frac{10}{4}(.2231)]-[-1]$$
$$=[-.5578254]+[1]=.44217$$



> b. (2 point) Run the simulation and paste your plot. Comment on the general shape of the distribution. How well does the density curve fit the observations?

The curve fits pretty well. I was wondering if my work on part 3 was correct because .089 seems to be quite a low number for P(x<6) but it seems to be correct from the histogram. Furthermore, being a gamma curve, it has a tail and a skewed peak, which lines up with the characteristics.

> c. (2 point) What is the exact proportion of values below 6? How does the actual proportion compare to the probability from the density curve in part 2-a-iii? 

It is exactly .436 in my case. This is close enough with our value of .44217 in the previous part. I take it that it’s within the realm of error.

> d. (1 point) Increase the number of observations to 10000, rerun the simulation. Paste your plot. How does increasing the number of observations affect the fit of the density curve? 

It makes the data more fit. They stay under the line more rather than over.

> e. (1 point) What is the exact proportion of values below 6? How does increasing the number of observations affect the accuracy of the model? Make a comparison between this proportion and 2-a-iii and 2c. 

It’s .45 in this case. You would think that it would steer more towards the .442 number more than the 1000 run but it went farther away by .002 which is interesting.

> f. (1 point) Rerun the simulation with alpha = 1, beta = 4, and observations = 10000. Paste your plot. Comment on the general shape of the distribution.

It’s highly skewed left and doesn’t go back down. Looks like an exponential distribution.

> g. (1 point) The model in part (f) is a special case of the gamma distribution, what is it specifically? What is the expression for the probability density function?     

It’s the exponential distribution.
$$
f(x) =
\begin{cases}
(\frac{1}{4})e^{-\frac{1}{4} x}, & x \geq 0 \\
0, & \text{otherwise}
\end{cases}
$$