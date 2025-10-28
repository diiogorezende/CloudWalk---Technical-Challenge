# CloudWalk---Technical-Challenge

### **Brief Report**

This analysis covers a financial dataset containing 841 observations and 17 features, spanning from April 7, 2025, to August 5, 2025.

Initial data processing involved looking at features with high nullity and handling date-type features. Three features (balance, provider_code, credit_card_data) were entirely null, and the 'merchant' feature was mostly null. The 'date' column was converted to a datetime object, and new time-based features, including an 'is_debit' flag, were engineered to support the analysis.

Descriptive statistics were calculated for transaction amounts ('amount_abs') grouped by 'category'. These metrics included count, total amount, mean, median, min/max values, standard deviation (STD), coefficient of variation (CV), and quartiles (Q1, Q3).

The analysis explored spending patterns, calculating the percentage of total debit per category and summarizing general statistics (e.g., total expenses, total received, period balance). An evaluation of seasonality identified May as the month with the highest expenses and August as the lowest.

A trend analysis was performed on monthly spending. This yielded a negative slope ($-5569.75), indicating a downward trend in expenses. However, the corresponding R-squared value was very low ($R^2 = 0.158$), suggesting this trend is not strong or reliable.

Key findings indicate that the 'Serviços' and 'Transferência mesma titularidade' categories show high financial variability, as measured by their high CV. No significant outliers were detected using standard statistical boundaries.


### Formal Metric Definitions

**Descriptive Statistics Used**

- Count ($n$): The total number of observations in the sample.
- Total Amount: The result of the sum of all observations in the dataset. $$\sum_{i=1}^{n} x_i$$
- Mean ($\bar{x}$): A measure of central tendency calculated by summing all values ($x_i$) and dividing by the total number of values ($n$). $$\bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i$$
- Median ($Md$): The central value of the ordered dataset. 
$$
\text{Median} = 
\begin{cases}
x_{\frac{n+1}{2}} & \text{if } n \text{ is odd} \\
\frac{x_{\frac{n}{2}} + x_{\frac{n}{2}+1}}{2} & \text{if } n \text{ is even}
\end{cases}
$$

- Minimum Value (Min(X)): The smallest value observed in the sample. $$Min(X) = x_{(1)}$$
- Maximum Value (Max(X)): The largest value observed in the sample. $$Max(X) = x_{(n)}$$
- Standard Deviation ($s$): A measure of the dispersion of values from the mean. $$s = \sqrt{\frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2}$$
- Coefficient of Variation (CV): A measure of relative dispersion, expressing the standard deviation as a percentage of the mean. $$CV = \frac{s}{|\bar{x}|}$$
- Quartiles: Values that divide the ordered dataset into four equal parts.
    - Q1 (25th Quartile): The value below which 25% of the data falls.
    - Q3 (75th Quartile): The value below which 75% of the data falls.

### Proposed Client Metrics

- Burn Rate: Calculates the total amount spent divided by the total amount received (income) within a period. $$\text{Burn Rate} = \frac{\text{Total Spent}}{\text{Total Received}}$$
- Monthly Pace: A projection of total monthly spending based on the average daily spending observed to date within the current month. $$\text{Monthly Pace} = \left( \frac{\text{Total Spent To Date}}{\text{Current Day of Month}} \right) \times (\text{Total Days in Month})$$