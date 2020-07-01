# DP Solver

Note: To view the equations correctly, download [MathJax](https://chrome.google.com/webstore/detail/mathjax-plugin-for-github/ioemnmodlmafdkllaclgeombjnmnbima?hl=en)

## Dynamic Programming
# Formulation
Consider a finite horizon problem with finite time $T$. We have the following notations

&emsp; 1) State $ x_t $

&emsp; 2) Action $ u_t $

&emsp; 3) Dynamic of the system $x_{t+1} = f_t(x_t, u_t) $

&emsp; 4) Strategy(Policy) $\gamma_t : \mathbb{X}_t \to U_t$, and $\gamma = (\gamma_1, \gamma_2, ..., \gamma_T)$

# Bellman's Principle of Optimality

&emsp; Policy $\bar{\gamma}^* $ is optimal iff the policy is optimal for the truncated problem from time $t$ to $T$. This holds for all $ t = 0, 1, ..., T - 1 $.

# DP Iteration
For every time step, we compute the following

&emsp; 1) $\gamma_t^* (x_t) = argmin_{u_t}[g_t(x_t, u_t) + V_{t+1}(f_t(x_t, u_t))]$

&emsp; 2) $V_t(x_t) = min_{u_t}[g_t(x_t, u_t) + V_{t+1}(f_t(x_t, u_t))]$

Starting with $V_T(x_T) = g_T(x_T)$, we compute the policy and value from time $t=T-1$ to $t=0$.
