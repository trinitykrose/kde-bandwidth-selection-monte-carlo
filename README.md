Comparing Parametric and Nonparametric Forecasting Models


Defines a known data generating process (DGP) with a nonlinear log relationship, so that "ground truth" is known and model performance can be benchmarked against the true irreducible error.

Compares bandwidth-selection methods for KDE — plug-in (Silverman) rule vs. least-squares cross-validation — showing that LSCV substantially outperforms the plug-in rule when the underlying distribution is non-normal (here, a U-shaped Beta distribution), reducing Integrated Squared Error by a factor of ~6.

Runs a 200-replication Monte Carlo study comparing three OLS specifications (correctly specified vs. two misspecified variants) on out-of-sample forecast accuracy (MSPE, RMSPE, MAE).

Extends the comparison to two nonparametric estimators — Nadaraya-Watson kernel regression and polynomial series regression — built and tuned from scratch (no off-the-shelf "compare models" library calls), including degree/bandwidth selection via cross-validation.

Tests asymptotic convergence of the nonparametric estimators by repeating the simulation across sample sizes from 500 to 10,000, confirming theoretical convergence rates.


Key findings


The correctly-specified parametric model outperforms all alternatives at every sample size tested — even nonparametric models that are asymptotically consistent need very large samples to close the gap, illustrating the practical cost of nonparametric flexibility at moderate sample sizes.

Cross-validated bandwidth/degree selection meaningfully improves nonparametric model performance over rule-of-thumb defaults, but isn't perfect — degree selection by 5-fold CV was shown to mildly overfit in this setup.

Result rankings were confirmed statistically robust via non-overlapping 95% confidence intervals across replications, not just point-estimate comparisons.
