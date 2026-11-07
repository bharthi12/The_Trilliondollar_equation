# Quantum-Inspired Stock Price Probability Model

> A quantitative finance project applying the mathematical framework of the Schrödinger equation to model asset return distributions, volatility potentials, and price probability density functions.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1LyVI0PzNsAZTvTsIMW1Ehk_8Jfw3uAp0)

## Table of Contents

* [About the Project](#about-the-project)
* [The Quantum-Finance Analogy](#the-quantum-finance-analogy)
* [Key Features](#key-features)
* [Project Workflow & Architecture](#project-workflow--architecture)
* [Getting Started on Google Colab](#getting-started-on-google-colab)
* [Code Structure & Usage](#code-structure--usage)
* [Results & Visualizations](#results--visualizations)
* [Contributing](#contributing)
* [License](#license)

---

## About the Project

Traditional financial models (like standard geometric Brownian motion) often fail to capture extreme market anomalies, fat tails (high kurtosis), and localized volatility clustering. This project explores an alternative approach by mapping financial asset dynamics to **quantum mechanical wave equations**. 

By casting stock return distributions and option barrier dynamics into a zero-energy Schrödinger-type framework, this notebook models how stock price probabilities diffuse, encounter market barriers (support/resistance lines), and exhibit quantum-like tunneling behavior.

## The Quantum-Finance Analogy

The project bridges quantum mechanics and market economics using the following conceptual mapping:

| Quantum Mechanic Concept | Financial / Economic Counterpart |
| :--- | :--- |
| **Wavefunction ($\psi$)** | Probability amplitude of a stock price or log-return |
| **Probability Density ($|\psi(S)|^2$)** | Likelihood distribution of where the stock price will land |
| **Potential Well ($V(S)$)** | Market boundaries, support/resistance levels, or strike prices |
| **Quantum Tunneling** | Probability of a stock breaking through major resistance barriers |
| **Planck’s Constant ($\hbar$) / Mass ($m$)** | Calibrated volatility parameters ($\sigma$) and drift scaling factors |

## Key Features

* **Quantum-Inspired PDE Solvers:** Numerical implementation to solve wave-like partial differential equations for financial asset states.
* **Fat-Tail Distribution Modeling:** Better accounts for extreme market shifts and volatility smiles compared to classical normal distribution assumptions.
* **Interactive Probability Visualizations:** Generates dynamic surface plots and probability density clouds shifting over distinct time horizons.
* **Zero-Setup Execution:** Fully runnable within a cloud-based Google Colab environment with integrated Python numeric and plotting libraries.

## Project Workflow & Architecture

```
[ Historical Market Data / Returns ]
                │
                ▼
[ Parameter Calibration (Volatility & Drift) ]
                │
                ▼
[ Schrödinger-Black-Scholes PDE Solver ] (Google Colab Runtime)
                │
                ▼
[ Probability Density Cloud & Tunneling Evaluation ]
```

## Getting Started on Google Colab

This project is optimized to run directly in your browser via Google Colab with no complex local setup required.

1. **Open the Notebook:** Click the badge below or use the project link:
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1LyVI0PzNsAZTvTsIMW1Ehk_8Jfw3uAp0)
2. **Runtime Configuration:** Ensure you are connected to a Python 3 runtime (GPU acceleration is optional but speeds up heavy matrix operations).
3. **Run All Cells:** Execute cells sequentially from top to bottom to fetch data, configure potentials, solve the wave equations, and render charts.

## Code Structure & Usage

Below is an overview of how the quantum-inspired simulation is initialized and solved inside the notebook:

```python
import numpy as np
import matplotlib.pyplot as plt

# Define spatial grid for log-prices and potential wells (support/resistance)
x = np.linspace(-3, 3, 500)
V_x = 0.5 * x**2  # Harmonic oscillator potential representing a range-bound market

# Initialize wave function and evolve probability density over time horizons
# (Refer to the Google Colab notebook for the full numerical PDE solver implementation)
print("Quantum-inspired probability distribution framework initialized.")
```

## Results & Visualizations

The model outputs probability density functions mapping out potential price corridors. 
* **Stable States:** High probability concentration within localized support-resistance bands.
* **Breakout Analysis:** Quantification of tail-risk probabilities indicating potential price tunneling beyond historical barriers.

## Contributing

Contributions, mathematical refinements, or alternative PDE discretization methods are welcome! Feel free to fork the repository and open a pull request.

## License

Distributed under the MIT License. See `LICENSE` for more information.