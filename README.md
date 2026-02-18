# Root-Locus-Velocity-Feedback-rlocus-rlocfind-gain-optimisation

MATLAB scripts for **ENG3018 Practical 3**: root locus analysis, closed-loop stability ranges, and velocity-feedback system reduction to unity-feedback form with gain selection for **ζ = 0.7071**.

---

# ENG3018 Practical 3 — Root Locus & Velocity Feedback (MATLAB)

MATLAB solution scripts for **ENG3018 Practical 3**, covering:
- Root locus plotting and **closed-loop stability ranges** for a unity negative-feedback system with **positive gain** \(K>0\).
- Reduction of a **velocity feedback** block diagram into an equivalent unity-feedback form.
- Gain selection so the **dominant complex poles** satisfy **\(\zeta \approx 0.7071\)**.

---

## What’s in here

### Q1 — Root locus + stability range for \(K\)

For the given plant:

```math
G_1(s)=\frac{s^2+2s+4}{s(s+4)(s+6)(s^2+1.2s+1)}
```

This repo:
- Plots `rlocus(G1)`
- Numerically scans \(K\) and refines **stability boundary estimates** (approx. imaginary-axis crossings)

---

### Q2 — Velocity feedback → equivalent unity-feedback + \(\zeta\) design

Given:

```math
H(s)=\frac{5}{s^2+5s+1}
```

A velocity-feedback structure is rewritten into a unity-feedback root-locus form:
- Defines \(K = 5k\)
- Uses an equivalent:

```math
G_2(s)=\frac{s}{s^3+5s^2+s+5}
```

Then selects \(K\) so the **dominant complex pole pair** has \(\zeta \approx 0.7071\).

> ⚠️ Note: You may see another intersection with \(\zeta=0.707\) at a different \(K\) (e.g. around 11.4), but it can correspond to a **non-dominant** complex pair (a slow real pole may dominate). The script targets the **dominant complex poles**, which is typically what the design requirement implies.

---

## Requirements
- MATLAB (tested with **R2024a**)
- Control System Toolbox

---

## How to run
1. Open MATLAB  
2. Copy/paste the script into MATLAB (or run the `.m` file if saved)  
3. Run the code  

---
