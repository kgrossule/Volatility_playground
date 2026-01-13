# Quantitative Finance Models

This repository contains Python implementations designed to visualize and understand the dynamics of key stochastic models in finance. These scripts were developed as part of my academic preparation in Quantitative Finance.

## Model Comparison: Constant vs. Local Volatility

This repository includes a specific comparison between two distinct approaches to volatility modeling, implemented in the following scripts:

* `vasicek_simulation.py`
* `local_volatility_simulation.py`

**Goal of the analysis:**
The primary purpose of these scripts is to demonstrate the structural limitations of **constant volatility models** (like the standard Vasicek framework) when compared to **non-constant volatility approaches** (Local Volatility).

By simulating both dynamics, I aimed to visualize:
1.  **Distributional Differences:** How the assumption of constant $\sigma$ fails to capture the heavy tails often observed in market data.
2.  **Smile Replication:** Why a state-dependent volatility function $\sigma(S,t)$ is necessary to replicate the implied volatility smile, which constant parameter models cannot produce.

This comparison serves as a foundational step for my thesis work on extending Dupire's Local Volatility model to interest rates using Particle Methods.

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
