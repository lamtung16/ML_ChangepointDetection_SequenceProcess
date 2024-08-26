# Sequence Features

This document provides explanations and formulas for various sequence features used in my research.

## Features

### 1. Standard Deviation (`std_deviation`)
- **Definition**: Measures the spread of values around the mean.
- **Formula**:
  $$\text{std deviation} = \sqrt{\frac{1}{N} \sum_{i=1}^{N} (x_i - \bar{x})^2}$$
  where $N$ is the number of values, $x_i$ is each individual value, and $\bar{x}$ is the mean of the values.

### 2. Mean
- **Definition**: The average of all values.
- **Formula**:
  $$\text{mean} = \frac{1}{N} \sum_{i=1}^{N} x_i$$
  where $N$ is the number of values, and $x_i$ is each individual value.

### 3. Median
- **Definition**: The middle value in a sorted list of values.
- **Formula**:
  - If $N$ is odd:
    $$\text{median} = x_{\left(\frac{N+1}{2}\right)}$$
  - If $N$ is even:
    $$\text{median} = \frac{x_{\left(\frac{N}{2}\right)} + x_{\left(\frac{N}{2} + 1\right)}}{2}$$
  where $x$ represents the ordered values.

### 4. Variance
- **Definition**: Measures the average squared deviation from the mean.
- **Formula**:
  $$\text{variance} = \frac{1}{N} \sum_{i=1}^{N} (x_i - \bar{x})^2$$
  where $N$ is the number of values, $x_i$ is each individual value, and $\bar{x}$ is the mean.

### 5. Range (`range_value`)
- **Definition**: The difference between the maximum and minimum values.
- **Formula**:
  $$\text{range value} = \max(x) - \min(x)$$
  where $x$ represents the set of values.

### 6. Interquartile Range (`iqr`)
- **Definition**: The range between the 25th percentile (Q1) and 75th percentile (Q3).
- **Formula**:
  $$\text{iqr} = Q3 - Q1$$
  where $Q1$ is the 25th percentile and $Q3$ is the 75th percentile.

### 7. Minimum Value (`min_value`)
- **Definition**: The smallest value in the sequence.
- **Formula**:
  $$\text{min value} = \min(x)$$
  where $x$ represents the set of values.

### 8. Maximum Value (`max_value`)
- **Definition**: The largest value in the sequence.
- **Formula**:
  $$\text{max value} = \max(x)$$
  where $x$ represents the set of values.

### 9. Absolute Skewness (`abs_skewness`)
- **Definition**: Measures the asymmetry of the data distribution.
- **Formula**:
  $$\text{skewness} = \frac{N \sum_{i=1}^{N} (x_i - \bar{x})^3}{(N-1)(N-2) (\text{std deviation})^3}$$
  $$\text{abs skewness} = |\text{skewness}|$$
  where $N$ is the number of values, $x_i$ is each value, and $\bar{x}$ is the mean.

### 10. Kurtosis
- **Definition**: Measures the "tailedness" of the distribution.
- **Formula**:
  $$\text{kurtosis} = \frac{N(N+1) \sum_{i=1}^{N} (x_i - \bar{x})^4}{(N-1)(N-2)(N-3) (\text{std deviation})^4} - \frac{3(N-1)^2}{(N-2)(N-3)}$$
  where $N$ is the number of values, $x_i$ is each value, and $\bar{x}$ is the mean.

### 11. Count
- **Definition**: The total number of values in the sequence.
- **Formula**:
  $$\text{count} = N$$
  where $N$ is the number of values.

### 12. Unique Count
- **Definition**: The number of distinct values in the sequence.
- **Formula**:
  $$\text{unique count} = \text{Number of distinct } x_i$$

### 13. Sum of Differences (`sum_diff`)
- **Definition**: The sum of differences between consecutive values.
- **Formula**:
  $$\text{sum diff} = \sum_{i=2}^{N} (x_i - x_{i-1})$$

### 14. Mean of Differences (`mean_diff`)
- **Definition**: The average of the differences between consecutive values.
- **Formula**:
  $$\text{mean diff} = \frac{1}{N-1} \sum_{i=2}^{N} (x_i - x_{i-1})$$

### 15. Maximum Difference (`max_diff`)
- **Definition**: The largest difference between consecutive values.
- **Formula**:
  $$\text{max diff} = \max(x_i - x_{i-1})$$

### 16. Minimum Difference (`min_diff`)
- **Definition**: The smallest difference between consecutive values.
- **Formula**:
  $$\text{min diff} = \min(x_i - x_{i-1})$$

### 17. 25th Percentile (`percentile_25`)
- **Definition**: The value below which 25% of the data falls.
- **Formula**:
  $$\text{percentile 25} = x_{(0.25 \times (N+1))}$$
  where $x$ is the ordered values.

### 18. 50th Percentile (`percentile_50` or Median)
- **Definition**: The value below which 50% of the data falls.
- **Formula**:
  $$\text{percentile 50} = x_{(0.50 \times (N+1))}$$
  where $x$ is the ordered values.

### 19. 75th Percentile (`percentile_75`)
- **Definition**: The value below which 75% of the data falls.
- **Formula**:
  $$\text{percentile 75} = x_{(0.75 \times (N+1))}$$
  where $x$ is the ordered values.

### 20. Autocorrelation (`autocorr`)
- **Definition**: Measures the correlation of the sequence with a lagged version of itself.
- **Formula**:
  $$\text{autocorr}(k) = \frac{\sum_{i=1}^{N-k} (x_i - \bar{x})(x_{i+k} - \bar{x})}{\sum_{i=1}^{N} (x_i - \bar{x})^2}$$
  where $k$ is the lag, $x_i$ is each value, and $\bar{x}$ is the mean.

## License
This documentation is provided under the MIT License. See the [LICENSE](LICENSE) file for more details.
