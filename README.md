# eco43000-efficient-frontier-23841777
Markowitz Efficient Frontier portfolio optimization project using Python, Monte Carlo simulation, and machine learning regression. ECO 43000 — Student ID: 23841777.
# Efficient Frontier Project — ECO 43000 Quantitative Finance

//

**Student ID:** 23841777  
**Course:** ECO 43000 — Quantitative Finance  
**Instructor:** John Droescher  
**Due Date:** Oct 31, 2025

---

## 📌 Project Objective

Use the Markowitz Mean-Variance framework to:
- Select **7 NYSE stocks**
- Retrieve **2 years of historical daily prices**
- Compute **expected returns**, **covariance**, and **correlation matrix**
- Generate **50,000+ Monte Carlo portfolios**
- Compute the **optimal portfolio maximizing the Sharpe Ratio**
- Use **regression (machine learning)** to estimate the Efficient Frontier
- Chart:
  - Efficient frontier + Monte Carlo cloud
  - Correlation matrix heatmap
- Provide final **optimal weights** & summary in report

---

## 📈 Selected NYSE Assets

| Ticker | Company |
|--------|---------|
| IBM | IBM Corp. |
| JPM | JP Morgan Chase |
| XOM | Exxon Mobil |
| WMT | Walmart |
| JNJ | Johnson & Johnson |
| KO | Coca-Cola |
| T | AT&T |

---

## 🧮 Methodology

1. Downloaded daily adjusted close prices using `yfinance`
2. Calculated daily log returns → annualized:
   - Expected return vector **μ**
   - Covariance matrix **Σ**
   - Correlation matrix **ρ**
3. Monte Carlo simulation:
   - **50,000** random long-only portfolios
   - Portfolio statistics computed:
     - \\(E(R_p) = w^T μ\\)
     - \\(\sigma_p = \sqrt{w^T Σ w}\\)
4. Risk-free rate assumed: **4%**
5. Polynomial regression used to estimate the efficient frontier boundary
6. Result: **Maximum Sharpe Ratio portfolio** identified

---

## 📊 Results Overview

| Metric | Optimal Portfolio |
|--------|------------------|
| Expected Annual Return | ~32.4% |
| Annual Volatility | ~14.4% |
| Sharpe Ratio | ~1.97 |

✅ Full report: `report.md`  
✅ Weights: `optimal_weights.csv`

---

## 📦 Project Files

| File | Description |
|------|-------------|
| `efficient_frontier_project.py` | Main Python class + analysis pipeline |
| `correlation_matrix.png` | Correlation heatmap |
| `efficient_frontier.png` | Efficient frontier + optimal portfolio |
| `optimal_weights.csv` | Final weights |
| `report.md` | Written project report |

---

## ▶️ How to Run

```bash
pip install -r requirements.txt
python efficient_frontier_project.py
