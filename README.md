# Wyndor-Glass-Problem-Optimization-using-Predictive-Stochastic-Programming
##Introduction -
In the Wyndor problem, there are two types of doors produced by three plants with time limits. The doors have either aluminum frames (A) or wood frames (B). The
plants are named 1, 2 and 3. The company now wants to optimize the profit by using advertising. The sales are needed when making advertising strategy. However, sales information is uncertain and also depends on the advertising strategy. The company uses TV and radio as two different advertising media. In this condition, sales are predicted based on the time slots for advertising spent on TV and radio.

The Wyndor glass problem considered for this project falls under the wing of Predictive Stochastic Programming (PSP). It is a combination of both Predictive Analytics and Stochastic Programming. Unlike an SP which has uncertain scenarios associated with it, a PSP works with covariates (the predictor and response variables.) The solving of a PSP model incorporates methodologies from both learning and Optimization. This integration created a combined methodology known as Learning Enabled Optimization (LEO).

##Constraints -
The dataset has 200 data points. The total budget of advertising is $200,000. Let x1 and x2 denote the TV and Radio expenditures. The total expenditures should be less than $200 (in thousand). One more policy is that the TV expenditures should be as least half of the Radio expenditures. From this, we have lower and upper limits for 𝑥𝑥1 and 𝑥𝑥2, observed from training set. Assuming the adverting costs are c1 = $100 and c2 = $500, the first stage model can be written as following.

$$
\[ \max -0.1x_1 - 0.5x_2 + E[Profit(\omega)] \]
$$
