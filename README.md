# Structural Analysis of Inter-Stock Dynamics in the Indian IT Sector

## Overview

This project investigates the long-term relationship and volatility behavior of two major Indian IT firms—Infosys and Tata Consultancy Services (TCS). Although these companies often appear to move in tandem, this study challenges that surface-level perception using time series analysis and volatility modeling techniques.

## Problem Statement

In financial markets, especially within sectorally aligned companies, apparent similarities in stock movements can obscure critical differences in underlying behavior. This is particularly true for Infosys and TCS, whose stock prices often appear to move together. This project explores whether these similarities are statistically supported or simply coincidental and what their implications are for investors and market strategists.

## Objectives

- To determine if a long-run equilibrium relationship (cointegration) exists between the stock prices of Infosys and TCS.
- To analyze and compare their volatility patterns using ARCH/GARCH models.
- To identify how each stock responds to market shocks and fluctuations.
- To explore real-world trading and portfolio strategies based on the findings.

## Data Description

- **Source**: Yahoo Finance
- **Stocks Analyzed**: Infosys (INFY.NS) and TCS (TCS.NS)
- **Time Period**: January 2020 to early 2025
- **Frequency**: Daily closing prices
- **Preprocessing**: Log returns computed for volatility modeling

## Methodology

### 1. Volatility Modeling

- **Techniques Used**: ARCH(1), GARCH(1,1), GARCH(2,2)
- **Findings**:
  - Infosys is best modeled using GARCH(1,1) with strong volatility persistence.
  - TCS is best modeled using GARCH(2,2) with more stable behavior and quicker mean reversion.
  - Infosys exhibits higher long-term volatility than TCS.

### 2. Cointegration and Error Correction Model (ECM)

- **Method**: Engle-Granger Two-Step Method with Dynamic Regression
- **Findings**:
  - Initial static regression showed no cointegration.
  - Including lagged variables revealed stationary residuals, indicating a long-term relationship.
  - ECM showed that INFY corrects approximately 1.09% of deviations from equilibrium per day.

## Real-World Implications

- **Short-Term Strategy**: Infosys is more suitable for short-term traders due to high volatility.
- **Long-Term Strategy**: TCS is preferable for risk-averse, long-term investors.
- **Pairs Trading**: The cointegration relationship can be exploited for mean-reversion-based strategies.
- **Risk Management**: Understanding differential volatility aids in better portfolio diversification.

## Files Included

- `project_report.pdf`: Full detailed report combining volatility and cointegration analyses.
- `notebooks/`: Jupyter notebooks with model implementation and visualizations.
- `README.md`: Overview of the project.

## Tools and Libraries

- Python
- Pandas, NumPy
- statsmodels, arch
- matplotlib, seaborn

