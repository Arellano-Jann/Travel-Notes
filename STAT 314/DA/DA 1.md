Part 1 (6 points) 

For each random variable, state whether the random variable should be modeled with a Binomial distribution or a Poisson distribution. Explain your reasoning. State the parameter values that describe the distribution and give the probability mass function. 

> Random Variable 1 (3 points)  
A software development team is concerned with the performance of their code. Historically, 3% of code modules exhibit performance issues. A development team samples 25 code modules from a project. Assuming the chance of performance issues is independent between modules, what type of distribution could be used to model the number of successful code modules from the sample of 25? Hint: the event of interest here is a code module performing well (i.e., not exhibiting performance issues).

**Distribution:** Binomial
**Why?** Over 25 trials, We have 2 things to keep track of. If it works (well) or not. We’re also given the probability of success.
**Params and pmf:**
n = 25, p = .97, q = .03
$$P_x = (^{25}_x)(.97)^x(.03)^{25-x}$$

> Random Variable 2 (3 points) A brand of smartphone has a warranty period of 2 years. During this time frame, there is no limit on the number of warranty claims that can be made. Historically, the average number of claims per smartphone during the 2-year period is 1.2 claims. What type of distribution could be used to model the number of warranty claims per smartphone? Hint: the event of interest here is the number of warranty claims made in a 2-year period. 

**Distribution:** Poisson 
**Why?** We have a count of warranty claims over the course of 2 years. These claims occur at an avg rate of 1.2 claims per phone so we’re given the lambda.
**Params and pmf:**
$\lambda$ = 1.2
$$P_x = \frac{1.2^xe^{-1.2}}{x!}$$


Part 2: (11 points) 

Wheel of Fortune is a popular game show on Television. Contestants spin a wheel and try to guess a correct letter from a word puzzle. If they guess correctly, they earn the dollar amount from the wheel. If they spin “bankrupt” or “lose a turn” they get nothing and can’t play. To the right is an example of the wheel.  Watch this video to see an example of someone spinning the wheel. [https://www.youtube.com/watch?v=_Pv33JWBdY8](https://www.youtube.com/watch?v=_Pv33JWBdY8)

The outcome of a spin on the wheel is a discrete random variable. Consider X the dollar amount spun on the wheel, where Bankrupt and Lose a Turn = $0. There are 24 wedges on the wheel. 

> a. (2 points) The table below displays the values the random variable X can take on, along with the number of times each value appears on the wheel (labeled Count). Fill in the last row of the table with the correct probability mass function values. That is, for each value X can take on, determine the probability the wheel is spun and lands on the given value, p(x). Round values to three decimal places. 

|       |      |      |      |      |      |      |      |      |      |      |      |      |      |       |
| ----- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ----- |
| x     | $0   | $150 | $200 | $250 | $300 | $350 | $400 | $450 | $500 | $700 | $750 | $800 | $900 | $1000 |
| Count | 2    | 2    | 4    | 2    | 2    | 1    | 3    | 1    | 2    | 1    | 1    | 1    | 1    | 1     |
| p(x)  | .083 | .083 | .167 | .083 | .083 | .042 | .125 | .042 | .083 | .042 | .042 | .042 | .042 | .042  |

> b. (1 point) What is the most likely dollar amount the spin will land on? 

$400

> c. (2 points) What is the average dollar amount? Show work! 

$0*.083+150*.083+200*.167+250*.083+300*.083+350*.042+400*.125+450*.042+500*.083+(700+750+800+900+1000)*.042$
$=390.9$

> d. (3 points) Suppose a contestant spins the wheel three times, how likely is it they spin $500 each time? Show work!


$.083*.083*.083 = .000572$

> e. (3 points) Suppose a contestant spins the wheel three times, how likely is it they spin $500 at least one time? Show work! 

$1-(1-.083)^3$
$=.229$

Part 3: (6 points) 

The PMF in Part 2 is based on probability theory. Do these probabilities stand up when a contestant actually spins the wheel?  Go back to the Data Analysis #1 instructions page on Canvas, download the R script titled: Wheel_of_Fortune_Spin_Script.R , open the file it will automatically open in R. You need R software on the computer to open the script window.  Follow the instructions in the code then answer the following:  

> a. (1 point) What value did you spin? 

500

> b. (1 point) What is the average of the 1000 simulated spins? How does this value compare to your answer in part 2c? 

390.4. Very similar and off by just a bit.

> c. (1 point) Include the simulated probability mass function AND the plot of the probability mass function from R. For the probability mass function, you should include a table with the all possible outcomes and the proportion of times each outcome was spun (output from line 45 of the code). 

| **Amount ($)**  | 0     | 150   | 200   | 250   | 300   | 350   | 400   | 450   | 500   | 700   | 750   | 800   | 900   | 1000  |
| --------------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| **Frequency**   | 86    | 79    | 151   | 83    | 98    | 38    | 119   | 41    | 100   | 41    | 43    | 42    | 47    | 32    |
| **Probability** | 0.086 | 0.079 | 0.151 | 0.083 | 0.098 | 0.038 | 0.119 | 0.041 | 0.100 | 0.041 | 0.043 | 0.042 | 0.047 | 0.032 |
![[../../../Ignored/Pasted image 20250113112152.png]]

![[../../../Ignored/Pasted image 20250113112210.png]]

> d. (1 point) How do the simulated probabilities compare to the theoretical probabilities in part 2? 

They’re very similar and holds the facts that $200, $400 are the most probable occurrences. 

> e. (1 point) Based on the plot is the most likely outcome the same as it is in part 2a? 

Yes it is.

> f. (1 point) In general, what action will make the simulated values more like the theoretical ones?

More spins. As there are more data values, the graph will start to smooth out more.