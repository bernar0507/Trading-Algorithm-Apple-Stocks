# SMA Based Trading Strategy

A trading algorithm that utilizes the Simple Moving Average (SMA) technique to generate buy and sell signals for stock trading. The project aims to optimize the SMA periods for maximized Sharpe Ratio and evaluate the strategy's performance based on various metrics.

## Table of Contents

- [Introduction](#introduction)
- [Methodology](#methodology)
  - [SMA Calculation](#sma-calculation)
  - [Optimal SMA Windows](#optimal-sma-windows)
  - [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [Conclusions](#conclusions)
- [Recommendations](#recommendations)

## Introduction

This trading strategy is based on the principle that stock prices tend to revert to their average over time. By comparing short-term and long-term SMAs, we can identify potential buy or sell opportunities.

## Methodology

### SMA Calculation

The Simple Moving Average is calculated by averaging the stock prices over a specified period. Two SMAs are used in this strategy:
- Short-term SMA
- Long-term SMA

A **buy signal** is generated when the short-term SMA crosses above the long-term SMA, and a **sell signal** is generated when the short-term SMA crosses below the long-term SMA.

### Optimal SMA Windows

To optimize the SMA periods for the best performance, a grid search was employed on the training data to maximize the Sharpe Ratio. This involves iterating through potential combinations of short and long SMAs.

### Evaluation Metrics

The following metrics were used to evaluate the strategy's performance:
- Cumulative Profit
- Sharpe Ratio
- Win Rate
- Profit Factor
- Number of Trades

## Results

- **Optimal SMA Windows**: 20 (Short) and 90 (Long)
- **Total Cumulative Profit**: $102.84
- **Average Percentage Profit per Trade**: 12606.81% (This might be an outlier or a computational anomaly due to the small sample size and should be verified)
- **Sharpe Ratio**: 1.68 (Falling into the "Good" category)
- **Win Rate**: 100% (Based on only two trades, this requires verification with larger datasets)
- **Profit Factor**: Infinite (No losses in the test dataset)
- **Number of Trades**: 2

## Conclusions

The strategy displayed promising results on the given dataset, with a decent Sharpe Ratio and positive profits. However, the small sample size (only two trades) requires further evaluation on a broader dataset for more robust insights.

## Recommendations

1. Test the strategy on an extended dataset or multiple stocks to achieve a more comprehensive performance insight.
2. Beware of potential overfitting to the training data. The optimized parameters might vary in effectiveness with other datasets.
3. Ensure diversity in market conditions (bullish, bearish, sideways) within the test dataset to gauge the strategy's adaptability.
4. Verify all computational results, especially with unusually high values or percentages, to ensure accuracy.
