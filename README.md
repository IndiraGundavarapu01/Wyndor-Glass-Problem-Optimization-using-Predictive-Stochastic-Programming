# Wyndor-Glass-Problem-Optimization-using-Predictive-Stochastic-Programming
## Introduction -
In the Wyndor problem, there are two types of doors produced by three plants with time limits. The doors have either aluminum frames (A) or wood frames (B). The
plants are named 1, 2 and 3. The company now wants to optimize the profit by using advertising. The sales are needed when making advertising strategy. However, sales information is uncertain and also depends on the advertising strategy. The company uses TV and radio as two different advertising media. In this condition, sales are predicted based on the time slots for advertising spent on TV and radio.

The Wyndor glass problem considered for this project falls under the wing of Predictive Stochastic Programming (PSP). It is a combination of both Predictive Analytics and Stochastic Programming. Unlike an SP which has uncertain scenarios associated with it, a PSP works with covariates (the predictor and response variables.) The solving of a PSP model incorporates methodologies from both learning and Optimization. This integration created a combined methodology known as Learning Enabled Optimization (LEO).

## First Stage Problem and Constraints -
The dataset has 200 data points. The total budget of advertising is 200,000 dollars. Let $x1$ and $x2$ denote the TV and Radio expenditures. The total expenditures should be less than 200 dollars (in thousand). One more policy is that the TV expenditures should be as least half of the Radio expenditures. From this, we have lower and upper limits for $x1$ and $x2$, observed from training set. Assuming the adverting costs are $c1$ = 100 and $c2$ = 500, the first stage model can be written as following.

$$
\
\begin{align*}
& \text{maximize} \quad -0.1x_1 - 0.5x_2 + E[Profit(\widetilde{\omega})] \\
& \text{subject to} \\
& \quad x_1 + x_2 \leq 200 \\
& \quad x_1 - 0.5x_2 \geq 0 \\
& \quad L_1 \leq x_1 \leq U_1 \\
& \quad L_2 \leq x_2 \leq U_2 \\
\end{align*}

## Second Stage Problem and Constraints - 
The sales $\widetilde{\omega}$ are random variables influenced by the advertising strategies $x1$ and $x2$. We choose linear regression to measure it in this project. Therefore, the total sales are denoted as $widetilde{\omega} = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \widetilde{\epsilon}$ and this equality is added as a constraint in the second-stage production problem. In this equation, we can say the profit is determined by the choice x and the uncertainty captured by the random variable 𝜀𝜀̃. For each specific 𝑤𝑤, we have following second stage model. 𝑦𝑦𝐴𝐴 and 𝑦𝑦𝐵𝐵 mean the batch of door A and door B produced. The first three constraints are the time limits in Figure 1. In this illustrative example, the “Total Hours” are multiplied by two to allow more options for product mix decisions. One more important change is that the product needs to satisfy an additional constraint about the potential future sales. The production should be less or equal to the sales.
\
$$
