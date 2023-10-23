# Unit 3: Regression

- [Unit 3: Regression](#unit-3-regression)
    - [Linear Regression](#linear-regression)
    - [Introduction to Regression](#introduction-to-regression)
    - [Simple and Multiple Linear Regression](#simple-and-multiple-linear-regression)
    - [Correlation vs. Regression](#correlation-vs-regression)
    - [SST (Sum of Squares Total)](#sst-sum-of-squares-total)
    - [SSR (Sum of Squares Regression)](#ssr-sum-of-squares-regression)
    - [SSE (Sum of Squares Error)](#sse-sum-of-squares-error)
    - [R-Square and Adjusted R-Squared](#r-square-and-adjusted-r-squared)
    - [Multiple Linear Regression](#multiple-linear-regression)
    - [Regression Using Data Analysis Toolbox of Excel](#regression-using-data-analysis-toolbox-of-excel)
    - [Significance of P-Value](#significance-of-p-value)

### Linear Regression

**Linear regression** is a fundamental statistical method used to model the relationship between a dependent variable (target) and one or more independent variables (predictors). It assumes a linear relationship between the predictors and the target. The primary objective of linear regression is to find the best-fitting linear equation that predicts the target variable based on the values of the predictor variables.

Linear regression can be categorized into two main types:

1. **Simple Linear Regression:** This type involves a single predictor variable and a single target variable. The relationship between the two is modeled using a straight line (hence "linear"). The equation of a simple linear regression model is typically represented as: `Y = a + bX`, where `Y` is the target variable, `X` is the predictor variable, `a` is the intercept, and `b` is the slope of the line.

2. **Multiple Linear Regression:** In this type, multiple predictor variables are used to model the target variable. The equation becomes more complex: `Y = a + b1X1 + b2X2 + ... + bnXn`, where `Y` is the target variable, `X1, X2, ..., Xn` are the predictor variables, and `a`, `b1, b2, ..., bn` are coefficients to be estimated. Multiple linear regression allows for modeling more complex relationships and capturing the influence of multiple predictors on the target.

### Introduction to Regression

**Regression analysis** is a statistical technique that aims to understand the relationship between one or more independent variables and a dependent variable. It is used to model and predict the values of the dependent variable based on the values of the independent variables. Regression analysis can be applied in various fields, including economics, finance, social sciences, and natural sciences.

The core idea behind regression is to find the best-fitting model that explains the relationship between variables. In linear regression, this model is linear, as discussed earlier. However, there are other types of regression, such as logistic regression for binary classification and polynomial regression for nonlinear relationships.

Regression analysis helps answer questions like:

- How does the change in one variable affect another?
- Can we predict a particular outcome based on certain input factors?
- Which factors are most influential in determining an outcome?

It is a powerful tool for data analysis and decision-making.

### Simple and Multiple Linear Regression

As mentioned earlier, **simple linear regression** involves a single predictor variable and a single target variable. It assumes a linear relationship between the predictor and the target. This relationship is described by a linear equation.

**Multiple linear regression**, on the other hand, extends the concept of linear regression to include multiple predictor variables. The relationship between the target variable and the predictors is modeled as a linear combination of the predictors, where each predictor has an associated coefficient. This allows for the analysis of more complex relationships and the consideration of multiple factors influencing the target.

In both cases, the goal is to estimate the coefficients (slopes and intercept) that define the linear relationship. This estimation is typically done using methods like ordinary least squares (OLS) to find the best-fitting line or plane that minimizes the sum of squared errors.

### Correlation vs. Regression

**Correlation** and **regression** are related but distinct concepts in statistics:

- **Correlation** measures the strength and direction of the linear relationship between two variables. It quantifies how one variable changes when the other changes. Correlation coefficients, such as Pearson's correlation coefficient (r), provide a numerical measure of the degree of association between variables. Correlation does not imply causation, and it does not involve predicting one variable from another.

- **Regression** goes a step further by modeling the relationship between one or more predictor variables and a target variable. It aims to predict the target variable based on the values of the predictor variables. While regression also assesses the strength and direction of the relationship, its primary purpose is to make predictions or understand how changes in predictors impact the target.

In summary, correlation is about assessing the association between variables, while regression is about modeling and predicting relationships.

### SST (Sum of Squares Total)

The **Sum of Squares Total (SST)** is a statistical measure used in the context of linear regression. It represents the total variation in the target variable (dependent variable, Y). SST is the sum of the squared differences between each data point's Y value and the overall mean of Y. Mathematically, it can be expressed as:

SST = Σ(Yi - Ŷ)^2

Where:

- SST is the Sum of Squares Total.
- Yi represents the individual observed values of the target variable.
- Ŷ is the mean (average) of all Y values.

SST represents the total variability in the target variable without considering any predictors. It serves as a baseline for assessing how well a regression model explains or accounts for the variability in the data. The goal in regression analysis is to reduce the unexplained variation (SSE) relative to the total variation (SST).

### SSR (Sum of Squares Regression)

The **Sum of Squares Regression (SSR)** is another key statistical measure in linear regression. It represents the portion of variability in the target variable (dependent variable, Y) that is explained by the regression model. SSR is the sum of the squared differences between the predicted Y values (based on the regression model) and the overall mean of Y. Mathematically, it can be expressed as:

SSR = Σ(Ŷi - Ŷ)^2

Where:

- SSR is the Sum of Squares Regression.
- Ŷi represents the predicted values of the target variable based on the regression model.
- Ŷ is the mean (average) of all Y values.

SSR quantifies the improvement in explaining the variability in the target variable achieved by the regression model. It is a measure of the model's effectiveness in capturing the relationships between predictors and the target.

### SSE (Sum of Squares Error)

The **Sum of Squares Error (SSE)** is a statistical measure in linear regression that represents the unexplained or residual variation in the target variable (dependent variable, Y) after accounting for the effects of the predictor variables. SSE is the sum of the squared differences between the observed Y values and the predicted Y values from the regression model. Mathematically, it can be expressed as:

SSE = Σ(Yi - Ŷi)^2

Where:

- SSE is the Sum of Squares Error.
- Yi represents the individual observed values of the target variable.
- Ŷi represents the predicted values of the target variable based on the regression model.

SSE quantifies the portion of variability in the target variable that the regression model has not explained. It represents the "error" or residuals in the model. The goal in linear regression is to minimize SSE to create the best-fitting model.

### R-Square and Adjusted R-Squared

**R-squared (R²)** is a statistical measure used to assess the goodness of fit of a linear regression model. It provides insight into how well the model explains the variation in the target variable (dependent variable, Y). R² is a value between 0 and 1, with higher values indicating a better fit. It is calculated as the proportion of the total variation in Y explained by the model (SSR) relative to the total variation (SST). Mathematically:

R² = SSR / SST

R² can be interpreted as the percentage of variation in the target variable that is accounted for by the regression model. However, it has a limitation: it tends to increase as more predictors are added to the model, even if those predictors do not improve the model significantly.

**Adjusted R-squared (Adjusted R²)** addresses this limitation. It adjusts R² based on the number of predictors in the model. Adjusted R² penalizes the inclusion of unnecessary predictors that do not improve the model's performance. It is particularly useful when comparing models with different numbers of predictors.

The formula for Adjusted R² is:

Adjusted R² = 1 - [(1 - R²) * (n - 1) / (n - k - 1)]

Where:

- n is the total number of data points.
- k is the number of predictors in the model.

Adjusted R² provides a more reliable measure of a model's quality, especially when dealing with multiple predictors.

### Multiple Linear Regression

**Multiple linear regression** is an extension of simple linear regression to accommodate multiple predictor variables. In a multiple linear regression model, the relationship between the target variable (dependent variable, Y) and two or more predictor variables is expressed through a linear equation. The model aims to find the best-fitting linear combination of the predictors that explains the variation in the target variable.

The multiple linear regression model can be represented as:

Y = a + b1X1 + b2X2 + ... + bnXn

Where:

- Y is the target variable.
- X1, X2, ..., Xn are the predictor variables.
- a is the intercept.
- b1, b2, ..., bn are the coefficients to be estimated.

Multiple linear regression allows for the modeling of more complex relationships between the target variable and multiple factors. It is a valuable tool in fields such as economics, finance, and social sciences, where various factors can influence an outcome.

### Regression Using Data Analysis Toolbox of Excel

Microsoft Excel provides a powerful Data Analysis Toolbox that includes various tools for conducting regression analysis. These tools can be used for both simple and multiple linear regression. Here are the general steps to perform regression using Excel:

1. **Data Preparation:** Organize your data in an Excel worksheet. You should have a column for the target variable (Y) and one or more columns for the predictor variables (X1, X2, ...).

2. **Data Analysis ToolPak:** Ensure that the Data Analysis ToolPak is installed in Excel. If not, you can enable it in Excel's options or settings.

3. **Select Regression:** In Excel, go to the Data tab and find the Data Analysis option. Select "Regression" from the list of tools.

4. **Input Range:** Specify the input range for the Y variable and the X variables. Excel allows you to select the data directly from your worksheet.

5. **Output Range:** Choose where you want the regression results to be displayed. This can be a new worksheet or a range within your existing worksheet.

6. **Options:** Set any specific options, such as whether you want confidence intervals, residual plots, or other statistics in the output.

7. **Run the Regression:** Click "OK" to perform the regression analysis. Excel will calculate the coefficients, standard errors, R-squared, and other relevant statistics.

8. **Interpret the Results:** Review the output to understand the coefficients, R-squared, p-values, and other statistics. These results will help you assess the quality and significance of the regression model.

Excel's Data Analysis ToolPak provides an accessible way to perform regression analysis for users who are familiar with the software.

### Significance of P-Value

The **p-value** is a critical statistic in the context of regression analysis, particularly in hypothesis testing. It quantifies the significance of the relationship between predictor variables and the target variable. Here's how it works:

- In a regression model, each predictor variable has an associated p-value.
- The p-value assesses whether the relationship between the predictor and the target is statistically significant.
- The null hypothesis (H0) for each predictor is that there is no significant relationship; in other words, the predictor has no effect on the target variable.
- The alternative hypothesis (Ha) is that there is a significant relationship between the predictor and the target variable.
- A low p-value (typically below a significance level, such as 0.05) indicates that you can reject the null hypothesis, suggesting that the predictor is statistically significant in explaining the target variable.

In summary, the p-value helps you determine whether a predictor variable is relevant and whether its inclusion in the model is warranted. It's a crucial tool for assessing the significance of predictors and, in turn, the quality of your regression model.
