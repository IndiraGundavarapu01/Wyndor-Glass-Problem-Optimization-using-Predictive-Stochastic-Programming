### 1. Project Title
**Optimizing Budget Allocation and Production Planning for Wyndor Glass Co. Using Learning Enabled Optimization**

### 2. Executive Summary
**Objective:** The primary goal of this project is to optimize budget allocation between TV and radio advertising to maximize the profit of Wyndor Glass Co., which produces two types of glass doors. The project also aims to develop an effective production planning strategy.

**Context:** The project employs Predictive Stochastic Programming (PSP) integrating learning and optimization methodologies. Tools and platforms used include Python with Pandas and scikit-learn for data preparation and linear regression, and Julia with CPLEX Solver for optimization.

### 3. Business Problem

**Problem Identification:** Wyndor Glass Co. faces the challenge of determining the optimal budget allocation for advertising to maximize sales and profit, amidst uncertain customer demand influenced by advertising spend. Additionally, the company needs an efficient production planning strategy to meet the varying demand.

**Business Impact:** The incorrect allocation of the advertising budget can lead to suboptimal sales and reduced profit margins. Effective optimization can significantly enhance financial performance, ensuring the company can meet demand without overspending on advertising or underutilizing production capacity.

### 4. Methodology

**Data Cleaning & Transformation:** 
- Data was split into training and validation sets.
- Outliers were identified and removed using Q-Q plots.
- Linear regression was performed to fit the sales data against advertising spend.

**Analysis Techniques:**
- **Linear Regression:** To predict sales based on advertising spend.
- **Deterministic Linear Programming (DLP):** To simplify the optimization under certain assumptions.
- **Sample Average Approximation (SAA) and Stochastic Decomposition (SD):** To handle uncertainties and improve optimization accuracy.

### 5. Skills

**Tools, Languages, & Software:**
- **Python:** For data preparation and linear regression using Pandas and scikit-learn.
- **Julia:** For optimization modeling in Jupyter Notebook.
- **CPLEX Solver:** To solve optimization models.

### 6. Results & Business Recommendation

**Business Impact:** 
- Determined optimal budget allocations for TV and radio advertising.
- Developed production plans ensuring resource efficiency and meeting demand.
- Significant profit improvements through better advertising strategies.

**Insights:**
- **Optimal Budget Allocation:** SLP with SAA and SD models recommended spending around $181,361.7 on TV and $18,638.2 on radio for optimal results.
- **Profit Maximization:** These models provided higher Mean Profit Objective (MPO) values within the validation confidence intervals, indicating reliable performance.

### 7. Next Steps

**Future Work:**
- Experiment with different data splits to verify the robustness of the regression model.
- Explore additional validation techniques beyond MVSAE.
- Consider other advertising channels and their impact on sales to further refine the model.
