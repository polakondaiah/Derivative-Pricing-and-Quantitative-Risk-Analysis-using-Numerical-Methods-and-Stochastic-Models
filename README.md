# 📊 Derivative Pricing – Numerical Methods for Quantitative Finance

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![NumPy](https://img.shields.io/badge/NumPy-1.21+-brightgreen.svg)](https://numpy.org/)
[![SciPy](https://img.shields.io/badge/SciPy-1.7+-orange.svg)](https://scipy.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A comprehensive, production-ready implementation of classical and advanced numerical methods for option pricing, risk management, and hedging. This repository covers lattice models, Monte Carlo simulation, stochastic volatility, jump-diffusion processes, barrier options, and dynamic delta hedging—all rigorously validated against no-arbitrage principles.

---

## 📖 Table of Contents

- [Overview](#overview)
- [Implemented Methods](#implemented-methods)
- [Project Parameters](#project-parameters)
- [Installation](#installation)
- [Quick Start](#quick-start)
- [Key Results & Validation](#key-results--validation)
- [Project Structure](#project-structure)
- [References](#references)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 Overview

This repository contains the complete numerical implementations from a group project on derivative pricing. The codebase demonstrates:

- **Binomial & Trinomial Trees** for European and American options (CRR lattice)
- **Monte Carlo Simulation** for path-dependent and exotic payoffs
- **Heston Stochastic Volatility Model** with leverage effects (\(\rho\))
- **Merton Jump-Diffusion Model** for capturing market discontinuities
- **Finite Difference Greeks** (Delta, Gamma, Vega) via symmetric perturbations
- **Dynamic Delta Hedging** with cash-account replication and hedging error analysis
- **Barrier Options** (Up-and-In Call, Down-and-In Put) with parity validation
- **Put–Call Parity** validation across all models

All implementations are modular, well-documented, and tested against theoretical no-arbitrage conditions.

---

## 🧮 Implemented Methods

| Method | Purpose | Key Features | Status |
| :--- | :--- | :--- | :---: |
| **Binomial Tree** | European & American option pricing | CRR lattice, early-exercise checks, convergence analysis | ✅ |
| **Trinomial Tree** | Improved lattice approximation | Three-price movements, faster convergence | ✅ |
| **Monte Carlo Simulation** | Numerical pricing under uncertainty | Variance reduction, path-dependent payoffs | ✅ |
| **Finite Difference Greeks** | Delta, Gamma, Vega estimation | Central difference approximations | ✅ |
| **Dynamic Delta Hedging** | Portfolio replication | Cash-account evolution, hedging error tracking | ✅ |
| **Heston Model** | Stochastic volatility pricing | Leverage effect (\(\rho\)), mean-reverting variance | ✅ |
| **Merton Model** | Jump-diffusion pricing | Poisson jumps, lognormal jump sizes | ✅ |
| **Barrier Options** | Up-and-In Call / Down-and-In Put | Knock-in features, path-dependent | ✅ |

---

## 📊 Project Parameters

The following base parameters are used throughout the implementations:

### Part I: Lattice Models (Binomial/Trinomial)

| Parameter | Value |
| :--- | :--- |
| Initial Stock Price (\(S_0\)) | 100.00 |
| Risk-Free Rate (\(r\)) | 5.00% |
| Volatility (\(\sigma\)) | 20.00% |
| Time to Maturity (\(T\)) | 0.25 years (3 months) |
| Strike (\(K\)) | 100.00 (ATM) |
| Binomial Steps | 200 (European), 100 (American) |

### Part II: Stochastic Volatility & Jump Models

| Parameter | Value |
| :--- | :--- |
| Initial Stock Price (\(S_0\)) | 80.00 |
| Risk-Free Rate (\(r\)) | 5.50% |
| Volatility (\(\sigma\)) | 35.00% |
| Time to Maturity (\(T\)) | 0.25 years (3 months) |
| Strike (\(K\)) | 80.00 (ATM) |
| **Heston Parameters** | |
| Initial Variance (\(\nu_0\)) | 0.032 |
| Mean Reversion (\(\kappa_\nu\)) | 1.85 |
| Long-Term Variance (\(\theta_\nu\)) | 0.045 |
| Correlation (\(\rho\)) | -0.30 / -0.70 |
| **Merton Parameters** | |
| Jump Intensity (\(\lambda\)) | 0.25 / 0.75 |
| Mean Jump Size (\(\mu_J\)) | -0.50 |
| Jump Volatility (\(\delta_J\)) | 0.22 |

### Part III: Dynamic Delta Hedging

| Parameter | Value |
| :--- | :--- |
| Initial Stock Price (\(S_0\)) | 180.00 |
| Risk-Free Rate (\(r\)) | 2.00% |
| Volatility (\(\sigma\)) | 25.00% |
| Time to Maturity (\(T\)) | 0.50 years |
| Strike (\(K\)) | 182.00 |
| Binomial Steps | 25 (American Put) |

---

## ⚙️ Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/yourusername/derivative-pricing-numerical-methods.git
cd derivative-pricing-numerical-methods
pip install -r requirements.txt
