# Variance Risk Premium Harvesting

**A regime-filtered approach to harvesting the equity variance risk premium, with honest inference about why backtested results should be viewed with skepticism.**

## Key Finding

A simple VIX-based filter improves the Sharpe ratio from 0.38 to 1.18 in backtests. But the 2019–2024 out-of-sample period was in the **99th percentile** of favorable conditions for this strategy. The filter "works," but its effectiveness cannot be predicted ex-ante.

## What I Did

| Stage | Question | Finding |
|-------|----------|---------|
| 1 | Does VRP exist? | Yes. 3.5 vol pts mean, 85% positive, statistically significant |
| 2 | Do filters help? | Sharpe 0.38 → 1.2, but bootstrap CIs are wide |
| 3 | Why did OOS beat IS? | Regime luck. COVID's V-shape was ideal; GFC's slow grind wasn't |
| 4 | Can smarter re-entry help? | No. Hard filter beats hysteresis and alternatives |

## The Honest Take

Filters are catastrophe insurance. They pay off when (a) the spike is severe enough that VRP flips negative, AND (b) the spike doesn't persist so long that you miss recovery premium. COVID satisfied both. GFC satisfied (a) but failed (b). You can't know which type of crisis you're in until it's over.

## Repo Structure

```
├── vrp_stage[1-4].ipynb   # Analysis notebooks
├── vrp_writeup.pdf        # Full paper (19 pages)
└── figures/               # All figures
```

## References

- Carr & Wu (2009). Variance risk premiums. *Review of Financial Studies*
- Bollerslev, Tauchen & Zhou (2009). Expected stock returns and variance risk premia. *Review of Financial Studies*

---

*Economic exposure study, not a trading strategy.*
