# Quantitative Finance Models

This repository contains Python implementations designed to visualize and understand the dynamics of key stochastic models in finance. These scripts were developed as part of my academic preparation in Quantitative Finance.

## Files Overview

### 1. `local_volatility_simulation.py`
**Local Volatility Model (Simulation)**
* **Objective:** Demonstrates the "Inverse Leverage Effect" where volatility increases as asset prices drop.
* **Mechanism:** Uses a state-dependent volatility function $\sigma(S) = 0.2 \cdot \sqrt{100/S}$ within a Monte Carlo simulation.
* **Outcome:** Visualizes how local volatility generates an asymmetric final distribution (Skew), departing from the standard Black-Scholes log-normality.

### 2. `vasicek_simulation.py`
**Vasicek Interest Rate Model**
* **Objective:** Simulates interest rate paths to analyze the Mean Reversion property.
* **Mechanism:** Discretizes the Ornstein-Uhlenbeck SDE using an Euler-Maruyama scheme.
* **Outcome:** Shows how rates fluctuate around the long-term target ($\theta$) over time, highlighting the theoretical behavior of the model.

## Dependencies
* Python 3.x
* NumPy, Matplotlib

## Author
**Katia Grossule**
Quantitative Finance Master's Candidate
