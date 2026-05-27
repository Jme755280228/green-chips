# Scoring Formulas

Green Chips uses four primary ethical metrics.

---

# 1. Harm Potential Score (HPS)

Measures potential harm.

Formula:

HPS = w1*Ph + w2*Sh + w3*Lh

Where:

| Variable | Meaning |
|---|---|
| Ph | Physical harm |
| Sh | Social harm |
| Lh | Long-term harm |
| w1,w2,w3 | Weight coefficients |

---

# Interpretation

Higher HPS means:
- violence risk
- dangerous intent
- destructive instructions

---

# 2. Emotional Distortion Score (EDS)

Measures emotional destabilization.

Formula:

EDS = Af + Aa + Ad + Fu

Where:

| Variable | Meaning |
|---|---|
| Af | Fear amplification |
| Aa | Anger amplification |
| Ad | Despair induction |
| Fu | Uncertainty confusion |

---

# 3. Dependency Risk Score (DRS)

Measures addictive dependency.

Formula:

DRS = Us * Rc * Td

Where:

| Variable | Meaning |
|---|---|
| Us | Usage stimulation |
| Rc | Retention coercion |
| Td | Time dependency |

---

# 4. Truth Confidence Score (TCS)

Measures confidence reliability.

Formula:

TCS = P(correct) - P(uncertainty)

---

# Final Ethical Constraint

Ethical systems attempt to minimize:

L_total = Lt + λ1(HPS) + λ2(EDS) + λ3(DRS)

Where:

| Variable | Meaning |
|---|---|
| Lt | Task loss |
| λ | Constraint weights |

