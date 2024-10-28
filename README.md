
# Trendist_v2

`trendist_v2` is a Python class designed to analyze and visualize historical financial data for stocks using Yahoo Finance data. The class enables you to retrieve, analyze, and plot the trends and distributions of stock returns, providing insights into historical price movements and the probability of trend continuation.

## Features

- **Historical Price Plotting**: Visualizes the historical closing price of a stock over a given period.
- **Return Distribution Analysis**: Plots a histogram of returns and overlays a normal distribution to compare actual vs. expected returns.
- **Probability Calculation**: Uses statistical tests to calculate the probability of trend continuation.
- **Cumulative Distribution Plotting**: Shows cumulative probability distributions, including recent return highlights.

## Installation

Ensure you have Python installed. Then install the necessary dependencies:

```bash
pip install yfinance numpy pandas matplotlib scipy
```

## Usage

Import the `trendist_v2` class into your project:

```python
from trendist_v2 import trendist_v2
```

### Creating an Instance

To create an instance, pass the stock ticker symbol and optional parameters for period and time period:

```python
trend = trendist_v2('AAPL', period='5y', timeperiod='W')
```

### Methods Overview

- **plot_history()**: Plot the historical closing price.
  
    ```python
    trend.plot_history()
    ```
  
- **plot_distrib()**: Plot the return distribution histogram with a normal distribution overlay.
  
    ```python
    trend.plot_distrib()
    ```
  
- **get_proba()**: Calculate and print a summary of statistical metrics and the probability of trend continuation.
  
    ```python
    trend.get_proba()
    ```
  
- **plot_cumdistrib()**: Plot the cumulative distribution, highlighting the most recent trend.
  
    ```python
    trend.plot_cumdistrib()
    ```

## Example

Below is an example of how to use `trendist_v2`:

```python
# Import trendist_v2 class
from trendist_v2 import trendist_v2

# Initialize the class with a ticker symbol
trend = trendist_v2('AAPL', period='5y', timeperiod='W')

# Plot the historical price
trend.plot_history()

# Plot the return distribution
trend.plot_distrib()

# Get probability and statistics
trend.get_proba()

# Plot cumulative distribution
trend.plot_cumdistrib()
```

## Dependencies

- `yfinance`: For fetching historical stock data.
- `numpy`: For numerical operations.
- `pandas`: For data manipulation and resampling.
- `matplotlib`: For plotting visualizations.
- `scipy`: For statistical calculations.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
