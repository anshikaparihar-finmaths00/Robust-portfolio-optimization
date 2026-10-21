# Robust vs. Classical Portfolio Optimization: A Comparative Analysis

This repository hosts my M.Sc. Mathematics final-year dissertation project. The research executes a rigorous comparative analysis between the Classical Markowitz Mean-Variance framework and Robust Portfolio Optimization methodologies to address parameter estimation risk in quantitative finance.

## Literature Foundations

This project directly implements, benchmarks, and analyzes the mathematical models established in:
1. Markowitz, H. (1952). *Portfolio Selection.* The Journal of Finance. (The Mean-Variance baseline).
2. Goldfarb, D., & Iyengar, G. (2003). *Robust Portfolio Selection.* Mathematics of Operations Research. (The Second-Order Cone Programming formulations).
3. Fabozzi, F. J., et al. (2007). *Robust Portfolio Optimization and Management.* John Wiley & Sons. (Uncertainty set estimation mechanics).
## Mathematical Formulations

### 1. Classical Baseline (Markowitz, 1952)
The classical formulation assumes deterministic input parameters for expected returns ($\mu$) and the covariance matrix ($\Sigma$):

$$
\min_{x \in \mathcal{X}} \quad x^T \hat{\Sigma} x
$$
$$
\text{subject to} \quad \hat{\mu}^T x \ge R_{\text{target}}
$$

### 2. Robust Portfolio Selection (Goldfarb & Iyengar, 2003)
To protect against data noise, true parameters are assumed to reside within an ellipsoidal uncertainty set $\mathcal{U}_{\mu}$:

$$
\mathcal{U}_{\mu} = \{ \mu \ \Big\vert{}\ (\mu - \hat{\mu})^T \Theta^{-1} (\mu - \hat{\mu}) \le \gamma^2 \ }
$$

The robust model minimizes the worst-case risk across the defined uncertainty boundaries:

$$
\min_{x \in \mathcal{X}} \max_{\Sigma \in \mathcal{U}_{\Sigma}} x^T \Sigma x
$$

## Project Timeline & Implementation Blueprint
- [x] Phase 1: Theoretical literature scoping and mathematical mapping (Active).
- [ ] Phase 2: Analytical derivation of Lagrange dual problems for conic tractability.
- [ ] Phase 3: Computational coding in Python utilizing CVXPY and data pipelines via pandas.
- [ ] Phase 4: Out-of-sample empirical benchmarking using historical market data.
