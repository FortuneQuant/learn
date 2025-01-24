---
title: Introduction to BRAIN
weight: 5
math: true
---

## Introduction to Alphas

For official materials, click [here](https://platform.worldquantbrain.com/learn/courses/introduction-alphas)

**Equity long-short market neutral strategy**

Goal: minimize exposure to the market in general, and **profit from a change** in the spread between two stocks

### 1. Inside simulation

Key settings: Delay, Decay

When you click "simulate"

**Step 1**: Evaluate the expression for each stock to generate the alpha vector for the given date.

**Step 2**: From each value in the vector, subtract the average of the vector values in the group. Sum of all vector values = 0. (Neutralization)

**Step 3**: The resulting values are scaled or ‘normalized’ such that the absolute sum of the alpha vector values is 1. These values can be called as normalized weights.

**Step 4**: Using normalized weights, the BRAIN simulator allocates capital (from a fictitious book of $20 million) to each stock to construct a portfolio.

**Step 5**: Calculate next day PnL based on observed stock returns the next day.

**Step 6**: Perform the operations in Step 1 to Step 5 for each date in a several-year history span also called the In-sample period (IS) to get daily PnL generated for each day.

**Step 7**: Calculate the cumulative PnL of the alpha from the start of the in-sample period to get the PnL chart of the alpha.

If Decay is used
$$
\text{Decay\_linear}(x,n)=\frac{x_t\times n+x_{t-1}\times (n-1)+\cdots+x_{t-n-1}}{n+(n-1)+\cdots+1}
$$

### 2. Simulation results

Most important: **Information Ratio (IR)**
$$
IR=\frac{mean(returns)}{std(returns)}
$$


Need to be high and consistent over years
$$
Sharpe=IR\times \sqrt{252}
$$
**Turnover (tvr)**

Represents the cost of trading
$$
tvr=\frac{\text{Value traded}}{\text{Value held}}
$$
The *lower* the turnover the better (< 40%)

Usually delay-0 alphas have higher turnover

### 3. OS test

- Base tests

  - Check weight: ensures diversify

  - Subuniverse value: the Sharpe in the next smallest standard universe (e.g. the subuniverse of Sector is Industry)

    Pass when greater than

    - Delay 1
      $$
      \sqrt{252}\times \max(0.065, 0.15\times \frac{S_{sub}}{S_{max}})
      $$

    - Delay 0
      $$
      \sqrt{252}\times \max(0.065, 0.25\times \frac{S_{sub}}{S_{max}})
      $$

    Where $S_{sub}$ is the sub-universe size, $S_{max}$ is the largest universe size

- Performance tests

  









