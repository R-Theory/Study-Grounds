# STOR 155 Midterm 1 - Master Study Guide

**Topics 1-7 | Exam: February 12, 2026**

---

## TOPIC 1: BASICS OF DATA

### Variables
- **Variable**: A characteristic/attribute that can take different values across observations
- **Numerical (Quantitative)**: Can do math with values
  - **Discrete**: Countable values (0, 1, 2, 3...)
  - **Continuous**: Any value in a range
- **Categorical (Qualitative)**: Categories/groups
  - **Nominal**: No natural order (eye color, gender)
  - **Ordinal**: Has natural order (education level, ratings)

> **Key Point**: Numbers can be categorical! Zip codes, jersey numbers, SSN - if averaging is meaningless, it's categorical.

### Population vs Sample
| Term | Definition |
|------|------------|
| **Population** | The ENTIRE group you want to study |
| **Sample** | A SUBSET of the population you collect data from |
| **Parameter** | A number describing the POPULATION (usually unknown) |
| **Statistic** | A number describing the SAMPLE (what we calculate) |

**Memory trick**: **P**arameter → **P**opulation, **S**tatistic → **S**ample

### Explanatory vs Response Variables
- **Explanatory variable**: The variable that EXPLAINS or predicts (the "cause" or x-variable)
- **Response variable**: The variable being EXPLAINED or predicted (the "effect" or y-variable)

---

## TOPIC 2: DATA COLLECTION & SAMPLING

### Three Sources of Data
1. **Anecdotes** - Individual stories, NOT representative, can't generalize
2. **Observational Studies** - PASSIVE observation, no manipulation
3. **Experiments** - ACTIVE manipulation with treatments

### Observational vs Experimental
| Feature | Observational Study | Experiment |
|---------|-------------------|------------|
| Method | PASSIVE observation | ACTIVE manipulation |
| Causation? | NO (only correlation) | YES (with proper design) |
| Random assignment? | No | Yes |
| Confounding? | Major problem | Controlled |

### Confounding Variables
- A factor OTHER than your explanatory variable that might affect your response variable
- **Classic example**: Ice cream sales ↑ and drowning ↑ are BOTH caused by HOT WEATHER

### Sampling Methods

| Method | Description | Key Feature |
|--------|-------------|-------------|
| **Simple Random Sampling (SRS)** | Every member has equal chance | Drawing from a hat |
| **Stratified Sampling** | Divide into HOMOGENEOUS groups, SRS from EACH | Sample from ALL strata |
| **Cluster Sampling** | Divide into HETEROGENEOUS groups, randomly select WHICH clusters, survey EVERYONE in selected | Sample from SOME clusters |
| **Multistage Sampling** | Cluster + SRS within selected clusters | Two-stage process |

**Critical Difference**:
- Stratified = homogeneous groups, sample from **ALL**
- Cluster = heterogeneous groups, sample from **SOME**

### Types of Bias
- **Convenience Sampling**: Only easy-to-reach participants - BIASED!
- **Voluntary Response**: People choose to participate - only strong opinions - BIASED!
- **Non-response Bias**: Planned sample good, but many don't respond - BIASED!

---

## TOPIC 3: EXPERIMENTS

### Four Principles of Experimental Design
1. **CONTROL**: Assign participants to multiple treatment groups (at least one control)
2. **RANDOMIZE**: Assign subjects RANDOMLY to treatment groups
3. **REPLICATE**: Test on MULTIPLE subjects; must be repeatable
4. **BLOCK**: Separate subjects by blocking variable BEFORE random assignment

### Blocking
- **Blocking variable**: A characteristic likely to influence outcomes (NOT what you're testing)
- Blocking is the experimental equivalent of **stratifying** in sampling

### Blinding
- **Placebo**: Fake treatment (sugar pill) - controls for placebo effect
- **Placebo effect**: People improve just because they THINK they're being treated
- **Blinding**: Subjects don't know which treatment they receive
- **Double-blind**: NEITHER subjects NOR researchers know who got what

### What Conclusions Can We Draw?
| Design Element | Allows |
|---------------|--------|
| Random assignment | **Causal** conclusions |
| Random sampling | **Generalizable** conclusions |
| Observational study | **NEVER** causation - only correlation |

---

## TOPIC 4: NUMERICAL DATA ANALYSIS

### SOCS Framework
**S**hape, **O**utliers, **C**enter, **S**pread

### Shape
**Modality**:
- Unimodal (1 peak)
- Bimodal (2 peaks)
- Multimodal (3+ peaks)
- Uniform (flat)

**Symmetry**:
- Symmetric
- Right-skewed (tail extends RIGHT, peak on LEFT)
- Left-skewed (tail extends LEFT, peak on RIGHT)

> **Remember**: Skew is named for where the TAIL is, not the peak!

### Skewness and Center Relationship
```
Right-skewed: Mean > Median (mean pulled toward tail)
Left-skewed: Mean < Median
Symmetric: Mean ≈ Median
```

### Measures of Center
**Mean**: x̄ = (1/n) × Σxᵢ

**Median**: Middle value when data is sorted

### Measures of Spread

**Sample Variance**:
```
s² = [1/(n-1)] × Σ(xᵢ - x̄)²
```
> **CRITICAL**: Divide by (n-1), NOT n!

**Standard Deviation**: s = √s²

**IQR**: Q3 - Q1

### Quartiles
- Q1 = 25th percentile (median of lower half)
- Q2 = 50th percentile (median)
- Q3 = 75th percentile (median of upper half)

### Five-Number Summary
Minimum, Q1, Median, Q3, Maximum

### Outlier Detection (IQR Method)
```
Outlier if: x < Q1 - 1.5×IQR  OR  x > Q3 + 1.5×IQR
```

### Robustness
| Measure | Robust to Outliers? |
|---------|-------------------|
| Median | YES |
| IQR | YES |
| Mean | NO (sensitive) |
| Variance | NO (sensitive) |
| Standard Deviation | NO (sensitive) |

### Transformations

**Adding constant c to all values**:
- Mean and Median shift by c
- SD, Variance, Shape UNCHANGED

**Multiplying all values by c**:
- Mean, Median, SD multiply by c
- Variance multiplies by c²
- Shape UNCHANGED

---

## TOPIC 5: CATEGORICAL DATA ANALYSIS

### Contingency Tables
- Table showing counts for TWO categorical variables combined

### Proportions
- **Proportion of total**: (Cell count) / (Grand total)
- **Row proportion**: (Cell count) / (Row total)
- **Column proportion**: (Cell count) / (Column total)

### Bar Plot vs Histogram
| Feature | Bar Plot | Histogram |
|---------|----------|-----------|
| Gaps? | YES (gaps between bars) | NO (adjacent bars) |
| Data type | Categorical | Numerical |

---

## TOPIC 6: CORRELATION

### Definition
Correlation (r) measures the **strength** and **DIRECTION** of **LINEAR** relationship between two numerical variables

### Range
-1 ≤ r ≤ +1

### Interpretation
| Value | Meaning |
|-------|---------|
| r = +1 | Perfect POSITIVE linear relationship |
| r = -1 | Perfect NEGATIVE linear relationship |
| r = 0 | NO linear relationship |
| r > 0 | As x increases, y TENDS TO increase |
| r < 0 | As x increases, y TENDS TO decrease |

### Key Properties of Correlation
1. **Invariant under translation**: Adding/subtracting constant doesn't change r
2. **Invariant under scaling**: Multiplying/dividing by constant doesn't change r
3. **Symmetric**: r(x,y) = r(y,x)
4. **NOT robust to outliers**: Outliers can drastically change r
5. **Only measures LINEAR relationships**: r = 0 could still have strong nonlinear relationship!

### Correlation Formula
```
r = [1/(n-1)] × Σ[(xᵢ - x̄)/sₓ × (yᵢ - ȳ)/sᵧ]
```

> **CRITICAL**: Correlation does NOT equal CAUSATION!

---

## TOPIC 7: LINEAR REGRESSION

### Regression Line Equation
```
ŷ = b₀ + b₁x
```
Where:
- ŷ = predicted value of y
- b₀ = y-intercept
- b₁ = slope

### Computing the Regression Line
```
Slope:     b₁ = r × (sᵧ/sₓ)
Intercept: b₀ = ȳ - b₁x̄
```

### Interpreting Slope and Intercept
- **Slope (b₁)**: "For each 1-unit increase in X, Y changes by b₁ units"
- **Intercept (b₀)**: "When X = 0, we predict Y = b₀" (may not be meaningful!)

### Residuals
```
Residual = Observed - Predicted = y - ŷ
```
- **Positive residual**: Model UNDERESTIMATED (actual > predicted)
- **Negative residual**: Model OVERESTIMATED (actual < predicted)

### R-squared (r²)
```
r² = (correlation)²
```
**Interpretation**: Percentage of variation in Y explained by the regression line

**Example**: r = 0.8 → r² = 0.64 = 64% of variation explained

### Interpolation vs Extrapolation
| Type | Definition | Trustworthiness |
|------|------------|-----------------|
| **Interpolation** | Predicting y for x-values WITHIN data range | TRUSTWORTHY ✓ |
| **Extrapolation** | Predicting y for x-values OUTSIDE data range | UNTRUSTWORTHY ✗ |

### Residual Plots
- **Ideal**: Random scatter around 0, no pattern, constant spread
- **Curved pattern**: Linear model is NOT appropriate (nonlinear relationship)
- **Fan/funnel shape**: Heteroskedasticity (non-constant variance) - problem!

### Important Note
Unlike correlation, switching x and y DOES change the regression line!

---

## FORMULA QUICK REFERENCE

```
Mean:            x̄ = Σxᵢ / n
Sample Variance: s² = Σ(xᵢ - x̄)² / (n-1)  ⚠️ Note: n-1!
Sample SD:       s = √s²
IQR:             Q3 - Q1
Outlier bounds:  Q1 - 1.5×IQR and Q3 + 1.5×IQR
Correlation:     r = [1/(n-1)]Σ[(xᵢ-x̄)/sₓ × (yᵢ-ȳ)/sᵧ]
Regression slope:     b₁ = r × (sᵧ/sₓ)
Regression intercept: b₀ = ȳ - b₁x̄
Residual:        e = y - ŷ
R-squared:       r² = (correlation)²
Complement rule: P(Aᶜ) = 1 - P(A)
Addition rule:   P(A or B) = P(A) + P(B) - P(A and B)
```

---

## TOP 10 MISTAKES TO AVOID

1. **Using n instead of n-1** in variance formula
2. **Confusing stratified and cluster sampling**
3. **Saying "correlation = causation"** - NEVER!
4. **Wrong skew direction** - Skew points to TAIL not peak
5. **Thinking r is a percentage** - It's not! r² is the % explained
6. **Forgetting outliers affect mean/SD** - Use median/IQR with outliers
7. **Claiming observational studies show causation** - They can't!
8. **Thinking r=0 means no relationship** - Could be nonlinear!
9. **Extrapolation is fine** - It's NOT trustworthy!
10. **Confusing blocking variable with explanatory variable**

---

## EXAM DAY STRATEGY

1. **Read questions carefully** - "Experiment" vs "Observational" changes everything
2. **Show all work** - Partial credit is real!
3. **Check reasonableness** - Is r between -1 and 1? Is probability between 0 and 1?
4. **Time management** - Do easy ones first, come back to hard ones
5. **Trust your preparation** - You've got this!

---

**Good luck on your exam!**
