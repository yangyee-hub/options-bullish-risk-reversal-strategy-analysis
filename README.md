## Options Trading Strategy: Analysis on Bullish Risk Reversal Strategy

This project analyzes various scenarios for a **Bullish Risk Reversal** strategy that involves:

- **Selling** 1-month **5% OTM SPY put options** (1000 contracts)
- Using the collected premium to **buy** 1-month **5% OTM SPY call options** (1000 contracts)

The strategy is placed as of late **April 9, 2025**, following a strong intraday market rally of approximately **10%**, one of the largest single-day moves in S&P 500 history.

---

## 📘 Project Description

We consider whether this bullish risk reversal trade would have been appropriate to put on during the late afternoon of April 9, 2025.  
This project includes **scenario analysis**, **historical data evaluation**, and **alternative structure comparisons**.

The work is divided into three major components.

---

## 1. Scenario Analysis (Python)

This section constructs a complete scenario framework for evaluating the trade.

### 1a. Build an equity option valuation model  
A set of reasonable assumptions is used to build a valuation model capable of computing prices for both the short 95% put and the long 105% call.

### 1b. Compute the PnL of the trade structure  
For each scenario, the model calculates:

- Option values  
- Net premium  
- 1-week-before-expiry PnL of the combined structure  
- Sensitivities to underlying price, volatility, and time decay  

---

## 2. Trade Assessment and Justification

This section explains the rationale for **why we would or would not** enter the risk-reversal trade on April 9, 2025.

### 2a. Historical data analysis  
We examine relevant historical data, including:

- SPY returns after extreme large-move days  
- Volatility term structure behavior  

- Skew and risk-premium considerations  

### 2b. Discuss reasonable max loss / max gain  
A clear discussion of:

- Downside risk from the short put  
- Upside convexity from the long call  
- Impact of extreme tail events  

---

## 3. Comparison With Alternative Structures

Two alternative strategies are evaluated to determine whether they may offer a better risk-adjusted payoff.

### 3a. Put spread + call structure  
Instead of selling a naked put, we may:

- Sell a 5% OTM put  
- **Buy a further OTM put** (e.g., 10%) to define downside risk  
- Use the net premium to fund the 5% OTM call

Analysis considers whether this structure is more appropriate given the market conditions on April 9, 2025, including:

- Skew shape  
- Crash risk  

- Post-rally volatility environment  

### 3b. Buying SPY outright  
We compare outright long SPY exposure vs. entering the options structure.

---

# Project Overview

This project analyzes SPY option data through:

* Option chain exploration
* Yield & risk-free rate estimation
* Scenario simulation (spot + IV shocks)
* Historical rally-day analysis
* Backtesting of option strategies
* Pricing models (Black–Scholes + Binomial)

---

# 📁 Project Structure

```
project/
│
├── code/                     # Analysis & modeling notebooks
│   ├── 0_ols_estimation_of_dividend_yield...
│   ├── 0_option_chain_data_exploration...
│   ├── 0_spy_data_exploration...
│   ├── 1_options_trade_scenario_analysis.ipynb
│   ├── 2.1_historical_rally_date_options_data_gather.ipynb
│   ├── 2.2_trade_backtesting_and_analysis.ipynb
│   ├── 3_max_min_pnl.ipynb
│   └── 3_extension_scenarios.ipynb
│
├── data/
│   ├── Option/               # Raw option chain CSV files
│   ├── Result/               # Simulation + backtest outputs
│   ├── SPY/                  # SPY price & return data
│   └── Yield/                # Yield and dividend rate series
│
├── environment.yml           # Conda environment
├── .env                      # Local environment variables
├── .gitignore
└── README.md
```

---

#  Environment Setup

A full Conda environment is provided.

### **1. Create environment**

```bash
conda env create -f environment.yml
```

### **2. Activate**

```bash
conda activate options-env    # or the name inside environment.yml
```

### **3. Launch notebooks**

```bash
jupyter lab
```

---

# Usage

Run notebooks in order (recommended):

1. **Data preparation & EDA** — `/code/0_*.ipynb`
2. **Scenario analysis** — `/code/1_options_trade_scenario_analysis.ipynb`
3. **Historical rally day & backtest** — `/code/2.*`
4. **Extensions & PnL extremes** — `/code/3_*`

Results will be exported to:

```
data/Result/
```

