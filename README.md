# Options Strategy: Bullish Risk Reversal Strategy Analysis

This project analyzes various scenarios for a **Bullish Risk Reversal** strategy that involves:

- **Selling** 1-month **95% OTM SPY put options** (1000 contracts)
- Using the collected premium to **buy** 1-month **105% OTM SPY call options** (1000 contracts)

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
- Distribution of forward 1-month moves  
- Skew and risk-premium considerations  

### 2b. Discuss reasonable max loss / max gain  
A clear discussion of:

- Downside risk from the short put  
- Upside convexity from the long call  
- Impact of extreme tail events  
- Realistic vs. theoretical payoff bounds  

---

## 3. Comparison With Alternative Structures

Two alternative strategies are evaluated to determine whether they may offer a better risk-adjusted payoff.

### 3a. Put spread + call structure  
Instead of selling a naked put, we may:

- Sell a 95% OTM put  
- **Buy a further OTM put** (e.g., 90%) to define downside risk  
- Use the net premium to fund the 105% OTM call

Analysis considers whether this structure is more appropriate given the market conditions on April 9, 2025, including:

- Skew shape  
- Crash risk  
- Liquidity  
- Post-rally volatility environment  

### 3b. Buying SPY outright  
We compare outright long SPY exposure vs. entering the options structure.

We consider:

- When outright SPY is superior (e.g., low implied volatility, muted skew, strong conviction)  
- When the risk reversal is better (e.g., elevated IV, expensive calls, favorable put skew)  

---

## 📂 Project Structure
```
project/
│
├── code/           # All notebooks, scripts, and analysis modules
├── data/           # Raw and processed data used for analysis
├── README.md       # Project documentation
├── .gitignore      # Git ignore rules for the repository
└── environment/    # (Optional) Environment or configuration files
```

---