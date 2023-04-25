# Stochastic Option Pricing with MLMC, QMC, and Brownian Bridge

This repository contains a Python project focused on the evaluation of an Asian option using the Cox-Ingersoll-Ross (CIR) model. Our team of three, Georgii Nikishin, Tristan Kirscher, and Julien Sklarik implemented various simulation techniques to compare their performance in terms of CPU time and mean square error (MSE).

## Project Overview

We wish to evaluate the price of an Asian option:
$C = \mathbb E\left[e^{-rT}(\frac{1}{k}\sum_{i=1}^{k}S(t_i)-K)^+\right]$

The project is based on the CIR (Cow, Ingersoll, Ross) model:

$dS_t = \alpha(b-S_t)\, dt + \sigma\sqrt{S_t}\, dW_t$

with the following parameters:

α = 0.15, b = 1, σ = 0.2, T = 1, r = 0.05, K = 4, k = 20, ti = i/20

The project covers the following techniques:

1. Multi-Level Monte Carlo (MLMC) method
2. Standard Monte Carlo (MC) method
3. (Randomized) Quasi-Monte Carlo (QMC) method
4. Brownian Bridge construction

## Features

- Comprehensive implementation of MC, MLMC, QMC , and QMLMC methods to approximate the option price
- Detailed comparison in terms of CPU time and MSE ceteris paribus
- Explanation of the Monte Carlo sample size selection for each level
- Exploration of Brownian Bridge construction and its impact on simulation results

## Usage

1. Clone the repository
2. Install the required dependencies: `pip install -r requirements.txt`
3. Run the main script: `python main.py`

## Contributing

We welcome contributions, feedback, and suggestions to help improve and expand the project further. Please feel free to submit a pull request or create an issue for any bugs, enhancements, or questions.

## License

[MIT](LICENSE)
