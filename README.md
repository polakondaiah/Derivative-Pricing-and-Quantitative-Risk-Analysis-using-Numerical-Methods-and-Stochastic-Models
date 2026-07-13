# Derivative Pricing and Risk Analysis using Numerical Methods and Stochastic Models

This repository presents a comprehensive implementation of numerical techniques used in modern quantitative finance for pricing and analyzing derivative securities.

The project progresses from classical lattice-based pricing methods to advanced stochastic models, demonstrating how different numerical techniques are applied to value financial derivatives and manage market risk.

# 📊 Derivative Pricing – Numerical Methods for Quantitative Finance

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![NumPy](https://img.shields.io/badge/NumPy-1.21+-brightgreen.svg)](https://numpy.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A comprehensive implementation of classical and advanced numerical methods for option pricing, risk management, and hedging. This repository covers lattice models, Monte Carlo simulation, stochastic volatility, jump-diffusion processes, and dynamic delta hedging—all validated against no-arbitrage principles.

---

## 📖 Table of Contents

- [Overview](#overview)
- [Implemented Methods](#implemented-methods)
- [Project Parameters](#project-parameters)
- [Installation](#installation)
- [Quick Start](#quick-start)
- [Key Results & Validation](#key-results--validation)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 Overview

This repository contains the numerical implementations from a group project on derivative pricing. The codebase demonstrates:

- **Binomial & Trinomial Trees** for European and American options
- **Monte Carlo Simulation** for path-dependent and exotic payoffs
- **Heston Stochastic Volatility Model** with leverage effects
- **Merton Jump-Diffusion Model** for capturing market discontinuities
- **Finite Difference Greeks** (Delta, Gamma, Vega)
- **Dynamic Delta Hedging** with cash-account replication
- **Barrier Options** (Up-and-In Call, Down-and-In Put)
- **Put–Call Parity** validation across all models

All implementations are modular, well-documented, and tested against theoretical no-arbitrage conditions.

---

## 🧮 Implemented Methods

| Method | Purpose | Key Features |
| :--- | :--- | :--- |
| **Binomial Tree** | European & American option pricing | CRR lattice, early-exercise checks |
| **Trinomial Tree** | Improved lattice convergence | Three-price movements, faster convergence |
| **Monte Carlo Simulation** | Numerical pricing under uncertainty | Variance reduction, path-dependent payoffs |
| **Finite Difference Greeks** | Delta, Gamma, Vega estimation | Central difference approximations |
| **Dynamic Delta Hedging** | Portfolio replication | Cash-account evolution, hedging error |
| **Heston Model** | Stochastic volatility pricing | Leverage effect (\(\rho\)), mean-reverting variance |
| **Merton Model** | Jump-diffusion pricing | Poisson jumps, lognormal jump sizes |
| **Barrier Options** | Up-and-In Call / Down-and-In Put | Knock-in features |

---

## 📊 Project Parameters

The following base parameters are used throughout the implementations:

| Parameter | Value |
| :--- | :--- |
| Initial Stock Price (\(S_0\)) | 100 (or 80 for specific sections) |
| Risk-Free Rate (\(r\)) | 5% (or 5.5% for specific sections) |
| Volatility (\(\sigma\)) | 20% (or 35% for specific sections) |
| Time to Maturity (\(T\)) | 0.25 years (3 months) |
| Strike (\(K\)) | ATM (varies for moneyness analysis) |
| Heston Parameters | \(\nu_0 = 0.032\), \(\kappa_\nu = 1.85\), \(\theta_\nu = 0.045\), \(\rho = -0.30\) / \(-0.70\) |
| Merton Parameters | \(\mu_J = -0.50\), \(\delta_J = 0.22\), \(\lambda = 0.75\) / \(0.25\) |

---

## ⚙️ Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/yourusername/derivative-pricing-numerical-methods.git
cd derivative-pricing-numerical-methods
pip install -r requirements.txt
