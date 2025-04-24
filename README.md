# dynamic-scaling

 Spencer Butler  
 April 2025   

## Overview

This project investigates the performance of linear vs. non-linear volume participation scaling in the execution of US equity orders benchmarked to arrival price. Specifically, it compares:

- Fixed percentage-of-volume (POV)
- Clamped linear scaling
- Non-linear scaling via a four-parameter logistic (4PL) function

A reversion-based execution framework is implemented where participation rate adjusts based on deviations from the arrival price. The objective is to enhance outcomes in mean-reverting market environments.

## Methodology

- Four stocks are selected at random
- Thirty full trading days from Q1 2025 are sampled
- Bloomberg Python API is used to retrieve 1-minute OHLCV and derived VWAP data
- Three execution strategies are simulated:
  - Fixed POV (10%)
  - Clamped linear scaling (between 5% and 15%)
  - Four-parameter logistic scaling (4PL)
- Execution performance is compared using paired one-tailed t-tests


## Results Summary

- Clamped linear scaling outperforms fixed POV across all test symbols (statistically significant)
- 4PL scaling does not show statistically significant improvement over clamped linear
- In low-volatility environments, the two scaling methods produce nearly identical outcomes

## File Contents

- `dynamic_scaling.ipynb`: Jupyter Notebook containing full implementation, simulation, and analysis
- `Dynamic Scaling.pdf`: Final paper write-up
- `README.md`: Project summary


## Disclaimer

This is an academic research project for demonstration purposes only.  
**This is not investment advice.**
