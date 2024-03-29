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
\
$$

## Second Stage Problem and Constraints - 
The sales $\widetilde{\omega}$ are random variables influenced by the advertising strategies $x1$ and $x2$. We choose linear regression to measure it in this project. Therefore, the total sales are denoted as $\widetilde{\omega} = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \widetilde{\epsilon}$ and this equality is added as a constraint in the second-stage production problem. In this equation, we can say the profit is determined by the choice of $x$ and the uncertainty captured by the random variable $\widetilde{\epsilon}$. 
For each specific $\omega$, we have following second stage model. $yA$ and $yB$ mean the batch of door A and door B produced. The first three constraints are the time limits. In this  example, the “Total Hours” are multiplied by two to allow more options for product mix decisions. One more important change is that the product needs to satisfy an additional constraint about the potential future sales. The production should be less or equal to the sales. 

$$
\begin{align*}
& \text{maximize} \quad 3y_A + 5y_B \\
& \text{subject to} \\
& \quad y_A \leq 8 \\
& \quad 2y_B \leq 24 \\
& \quad 3y_A + 5y_B \leq 36 \\
& \quad y_A + y_B \leq \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \epsilon_{ti}, \quad \forall i \\
& \quad y_A, y_B \geq 0 \\
\end{align*}
$$

## Assumptions - 
Since the interface between two stages is $\omega$, it’s important to reconcile the assumptions of linear regression underlying statistical estimation and optimization.
1. Linearity: Linear model is sufficient.
2. Independence: The error terms in regression model are independent random
variables. Each data points represents independent clients.
3. Normality: The error is approximately normally distributed.
4. Homoscedasticity: The variance of errors doesn’t change with the choice of $x$
