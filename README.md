# Housing Market Data Analysis in R

This project analyzes housing market data using R, focusing on data analysis, visualization, hypothesis testing, and linear regression. It guides users through understanding dataset structure, computing statistical insights, creating visualizations, and applying predictive modeling techniques.

## Project Overview

The project is divided into the following phases:

1. **Data Analysis**: Exploratory analysis, descriptive statistics, correlation analysis, and handling missing values.
2. **Data Visualization**: Creating a histogram to visualize the distribution of median home values.
3. **Hypothesis Testing**: Conducting a T-test to analyze the impact of crime rates on home values.
4. **Linear Regression**: Building a predictive model to estimate home prices using average room size.

---

## Dataset Description

The dataset is sourced from a CSV file containing the following variables:

- **Crime.Rate**: Local crime rate per capita.
- **Average.Rooms**: Average number of rooms in homes.
- **Public.Transport.Access**: Proximity to public transport.
- **Number.of.Schools**: Number of local schools.
- **Median.Home.Value**: Median value of homes.

---

## Project Phases

### 1. Data Analysis
- **Objectives**:
  - Perform exploratory data analysis (EDA).
  - Compute descriptive statistics (mean, median, mode).
  - Conduct correlation analysis and identify the strongest relationships.
  - Handle missing values by imputing with the median.

- **Key Steps**:
  - Load the dataset using R.
  - Use `summary()`, `head()`, and `tail()` for exploration.
  - Implement a custom function to compute the mode.
  - Identify and replace missing values using `mutate_all()`.

---

### 2. Data Visualization
Using `ggplot2`, plot a histogram to analyze the distribution of home values.

- **Specifications**:
  - Number of bins: 9
  - Style:
    - Fill: `darkcyan`
    - Outline color: `white`
    - Transparency: `alpha = 0.7`
  - Labels and theme:
    - Title: "Distribution of Median Home Values"
    - X-axis: "Median Home Value"
    - Y-axis: "Frequency"
    - Theme: `theme_minimal()`

---

### 3. Hypothesis Testing
- **Objective**: Analyze the relationship between crime rates and home values.
- **Hypotheses**:
  - Null Hypothesis (H0): No difference in median home values between high and low crime areas.
  - Alternative Hypothesis (H1): A difference exists in median home values.

- **Steps**:
  1. Define high and low crime rate groups based on the median crime rate.
  2. Conduct a Two-Sample Independent T-Test using `t.test()` with equal variances.
  3. Interpret results based on the p-value (significance level: 0.05).

---

### 4. Linear Regression
- **Objective**: Predict median home prices using the average room size.
- **Steps**:
  1. Build a linear regression model using `lm()` and summarize results with `summary()`.
  2. Create a scatter plot with a regression line using `ggplot2`:
     - Scatter points: `geom_point(alpha = 0.6)`
     - Regression line: `geom_smooth(method = "lm", col = "red", se = FALSE)`
  3. Apply labels and themes for clarity.

---

## Tools and Libraries
- **R Libraries**:
  - `tidyverse` (for data manipulation and visualization)
  - `ggplot2` (for visualizations)
  - `dplyr` (for data wrangling)
  - `car` (optional: for Levene's test)

---

## Results and Insights
- Descriptive statistics reveal the central tendencies of variables.
- Visualizations provide insights into home value distributions and correlations.
- Hypothesis testing uncovers the impact of crime rates on home prices.
- Linear regression demonstrates the relationship between average room size and median home values.

---

## Instructions for Use
1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo/housing-market-analysis.git
