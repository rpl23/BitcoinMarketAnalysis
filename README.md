# Bitcoin Time Series Analysis and Market Comparison

This project conducts a comprehensive econometric analysis of Bitcoin price movements and their relationship with traditional financial markets. The analysis combines multiple time series forecasting techniques with comparative market analysis to understand cryptocurrency price dynamics.

## Project Overview

- **Time Period**: 2020-01-01 to 2024-12-02
- **Assets Analyzed**: Bitcoin, Gold, S&P 500
- **Data Source**: Yahoo Finance
- **Analysis Types**: Time Series Forecasting, Market Comparison, Volatility Analysis

## Project Structure

```
.
├── Data/
│   ├── market_data.csv           # Combined market data for all assets
│   ├── correlations.csv          # Asset correlation matrix
│   └── summary_statistics.csv    # Key statistical metrics
├── Reports/
│   └── BitcoinFinalReport.docx   # Comprehensive analysis report
├── Scripts/
│   └── BitcoinProject.Rmd        # R Markdown analysis script
└── Outputs/
    └── price_comparison.png      # Visualization outputs
```

## Key Features

### Time Series Models Implemented
- **Regression Models**
  - Mean (baseline)
  - Naïve
  - Random Walk with Drift
  - Time Series Linear Models (TSLM)

- **Exponential Smoothing (ETS)**
  - Automated ETS selection
  - ETS(A,A,M) - Additive error, additive trend, multiplicative seasonality
  - ETS(A,A,N) - Additive error, additive trend, non-seasonal

- **ARIMA Models**
  - Automated ARIMA selection
  - Manual ARIMA specification

### Market Analysis Features
- Asset correlation analysis
- Volatility comparison
- Risk-adjusted performance metrics
- Rolling statistics
- Maximum drawdown analysis

## Key Findings

- Bitcoin exhibits higher volatility (σ = 0.5348) compared to traditional assets
- ETS(A,A,N) model shows superior predictive performance (RMSE: 12777.11)
- Significant differences in risk-return profiles:
  - Bitcoin: μ = 0.5115, σ = 0.5348
  - Gold: μ = 0.1210, σ = 0.1555
  - S&P 500: μ = 0.1487, σ = 0.2144

## Requirements

### R Packages
- quantmod
- tidyverse
- lubridate
- TTR
- fpp3
- tseries
- forecast

### Installation
```R
# Install required packages
install.packages(c("quantmod", "tidyverse", "lubridate", "TTR", 
                  "fpp3", "tseries", "forecast"))
```

## Usage

1. Clone the repository
2. Install required R packages
3. Run the analysis:
```R
# Open R Studio
# Open BitcoinProject.Rmd
# Run all chunks or knit the document
```

## Data Processing

The project follows a structured data processing pipeline:
1. Data acquisition from Yahoo Finance
2. Cleaning and preprocessing
3. Feature engineering
4. Model training (80% of data)
5. Model validation (20% of data)
6. Performance evaluation

## Model Evaluation Metrics

- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- Mean Absolute Percentage Error (MAPE)
- Mean Absolute Scaled Error (MASE)
- Akaike Information Criterion (AIC)
- Bayesian Information Criterion (BIC)

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## Authors

- Ryan Lancaster

## Acknowledgments

- Data provided by Yahoo Finance
- Analysis framework based on the `fpp3` package ecosystem
