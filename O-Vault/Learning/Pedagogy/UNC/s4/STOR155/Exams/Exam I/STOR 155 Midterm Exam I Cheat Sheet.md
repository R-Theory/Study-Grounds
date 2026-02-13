---
cssclasses:
  - cheat-sheet
Learning Type: Pedagogy
Subject: Statistics
---
# Midterm Exam I Cheat Sheet

> **Topics 1–7 | Spring 2026**

---

## 1. Variable Types

--- start-multi-column: varTypes
```settings
Number of Columns: 2
Largest Column: standard
Border: off
```

### Numerical
*Arithmetic makes sense*
- **Discrete** — countable integers (# students, dice rolls, count of events)
- **Continuous** — any value in range (height, weight, time, temperature)

--- column-break ---

### Categorical
*Labels / groups*
- **Nominal** — no inherent order (colors, states, gender, yes/no)
- **Ordinal** — natural order (letter grades, satisfaction levels, age groups)

--- end-multi-column

> [!tip] Quick Test
> Can you calculate a meaningful average? → **Numerical**
> Are values labels/categories? → **Categorical**

| Role | Description |
| --- | --- |
| **Explanatory ($X$)** | Predicts/explains → plotted on x-axis |
| **Response ($Y$)** | Outcome being measured → plotted on y-axis |
| **Blocking** | Creates similar groups — **NOT** manipulated by researcher |

---

## 2. Study Design & Causation

--- start-multi-column: studyDesign
```settings
Number of Columns: 2
Largest Column: standard
Border: off
```

### Observational Study
- Researcher **only observes**, no intervention
- Can only establish **correlation**
- Cannot control for confounding variables
- Often used when experiments are unethical or infeasible

--- column-break ---

### Experiment
- Researcher **actively assigns** treatments
- Can establish **causation** (with random assignment)
- Controls for confounding variables
- **Gold standard** of research methods

--- end-multi-column

> [!warning] Golden Rule
> Only **experiments** with **random assignment** → **causation**
> Observational studies → **correlation only**

**Sources of Data:**
1. **Anecdotes** — individual stories, single cases → **BAD** for scientific inquiry
2. **Observational studies** — passive data collection → good scientific inquiry
3. **Experiments** — active intervention with treatment → good scientific inquiry

**Confounding variable:** a factor *other than* the explanatory variable that might affect what you observe in the response variable — affects **BOTH** $X$ and $Y$

### Causation & Generalization Grid

| | **Random Assignment** | **No Random Assignment** |
| --- | --- | --- |
| **Random Sampling** | Causation + Generalization | Correlation + Generalization |
| **No Random Sampling** | Causation (sample only) | Correlation (sample only) |

> [!info] Key Takeaway
> **Random assignment** → controls causation vs. correlation
> **Random sampling** → controls generalizability to population
> Be careful to ONLY draw conclusions that align with your sampling and assignment methods.

---

## 3. Sampling Methods

--- start-multi-column: samplingTerms
```settings
Number of Columns: 2
Largest Column: standard
Border: off
```

### Population → Parameter
- The **entire group** you want to study
- True unknown value
- Greek letters: $\mu$, $\sigma$, $p$

--- column-break ---

### Sample → Statistic
- A **subset** of the population
- Calculated estimate from data
- Roman letters: $\bar{x}$, $s$, $\hat{p}$

--- end-multi-column

- **Census** = data from the **full population** (accurate but often infeasible)
- **Survey** = data from a **sample** (practical, less accurate)
- **Inference** = a conclusion about an entire population based on observations of a sample

### Sampling Types

| Method | How It Works | Key Detail |
| --- | --- | --- |
| **Simple Random (SRS)** | Every individual has equal probability | "Draw names out of a hat" |
| **Stratified** | Divide into **homogeneous** strata → SRS from **each** | Ensures all subgroups represented |
| **Cluster** | Divide into **heterogeneous** clusters → select **entire** clusters | Convenient for large populations |
| **Multistage** | Combine methods (e.g., cluster → SRS within) | Used when clusters are too big |

> [!tip] Stratified vs. Cluster
> **Stratified:** strata are *homogeneous* within → sample **from each** → ensures representation
> **Cluster:** clusters are *heterogeneous* within (mirror the population) → sample **entire** clusters → convenience

### Sources of Bias

| Bias Type | Description |
| --- | --- |
| **Sampling bias** | Systematic exclusion of groups from the sample |
| **Nonresponse** | Selected individuals don't respond (resulting sample ≠ planned sample) |
| **Voluntary response** | Self-selection — people with strong opinions overrepresented |
| **Convenience** | Only sample easy-to-reach individuals |
| **Question wording** | Word choice influences responses (e.g., "welfare" vs. "assistance to the poor") |
| **Question framing** | Question format matters (open-ended vs. multiple-choice give different results) |

---

## 4. Experimental Design — 4 Principles

| Principle | Description |
| --- | --- |
| **1. Control** | Assign to **multiple treatment groups**; include a **control group** (no treatment) |
| **2. Randomize** | **Randomly assign** subjects to groups → reduces bias, improves control |
| **3. Replicate** | Large sample sizes; design so study is **repeatable** by others |
| **4. Block** | Group similar subjects by a **blocking variable** → randomize **within** blocks |

> [!info] Blocking = Experimental Equivalent of Stratifying
> If you think a variable will influence outcomes, **block** by it before assigning treatments.
> Example: in medical studies, block by gender because drugs interact differently with different endocrine systems.
> A blocking variable is **NOT** an explanatory variable.

### Reducing Bias in Experiments

--- start-multi-column: biasReduction
```settings
Number of Columns: 2
Largest Column: standard
Border: off
```

- **Treatment** — the explanatory variable you are manipulating
- **Placebo** — fake treatment given to the control group so subjects don't know their group
- **Placebo effect** — psychological phenomenon where control subjects experience effects they *believe* should occur

--- column-break ---

- **Blinding** — subjects don't know which group they're in
- **Double-blind** — **both** subjects AND researchers are unaware of group assignments
  - Prevents the **Rosenthal effect** (researcher expectations subconsciously influencing outcomes)
- **Matched pairs** — pair "similar" subjects, put 1 in control and 1 in treatment (twins = ideal pairs)

--- end-multi-column

---

## 5. Numerical Data Summaries

### Measures of Center

$$\bar{x} = \frac{1}{n}\sum_{i=1}^{n} x_i \qquad \text{(mean — sensitive to outliers)}$$

- **Median** — middle value when data is ordered **(resistant to outliers)**
  - $n$ odd → single middle value
  - $n$ even → **average** of the two middle values
- **Mode** — most frequent value(s)

### Skewness & Center

| Shape | Relationship | Remember |
| --- | --- | --- |
| Right-skewed | $\bar{x} > \text{median}$ | Tail pulls mean **right** |
| Left-skewed | $\bar{x} < \text{median}$ | Tail pulls mean **left** |
| Symmetric | $\bar{x} \approx \text{median}$ | — |

> [!warning] Skew Is Named by TAIL Direction
> "Right-skew" = tail on the **RIGHT**, peak on the left.
> "Left-skew" = tail on the **LEFT**, peak on the right.

### Measures of Spread

$$s^2 = \frac{1}{n-1}\sum_{i=1}^{n}(x_i - \bar{x})^2 \qquad \text{(sample variance — sensitive to outliers)}$$

$$s = \sqrt{s^2} \qquad \text{(sample standard deviation)}$$

$$\text{IQR} = Q_3 - Q_1 \qquad \text{(resistant to outliers)}$$

$$\text{Range} = \max - \min \qquad \text{(sensitive to outliers)}$$

> [!danger] Divide by $n - 1$
> Sample variance uses $n - 1$ in the denominator, **NOT** $n$.

### Quartiles & Five-Number Summary

--- start-multi-column: quartiles
```settings
Number of Columns: 2
Largest Column: standard
Border: off
```

| Quartile | Meaning |
| --- | --- |
| $Q_1$ (25th %ile) | Median of lower half |
| $Q_2$ (50th %ile) | Median |
| $Q_3$ (75th %ile) | Median of upper half |

**Five-Number Summary:**

$$\min, \quad Q_1, \quad \text{median}, \quad Q_3, \quad \max$$

--- column-break ---

> [!warning] Quartile Calculation When $n$ Is Odd
> Two methods to split into halves:
> - **Inclusive:** include median in both halves
> - **Exclusive:** exclude median from both halves
>
> The halves **MUST** have equal numbers of data points!

--- end-multi-column

### Outlier Detection (IQR Rule)

$$\text{Lower fence} = Q_1 - 1.5 \times \text{IQR}$$

$$\text{Upper fence} = Q_3 + 1.5 \times \text{IQR}$$

Any value **beyond** either fence is an **outlier**.

### Choosing Summary Measures

| Distribution | Center | Spread |
| --- | --- | --- |
| Symmetric, no outliers | **Mean** | **Std Dev** |
| Skewed or has outliers | **Median** | **IQR** |

### Describing Distributions — Always Mention All 4

1. **Shape** — unimodal / bimodal / multimodal / uniform; symmetric / left-skewed / right-skewed
2. **Center** — mean or median (choose based on shape)
3. **Spread** — standard deviation or IQR (choose based on shape)
4. **Outliers** — identify if present

### Visualization

| Plot | Data Type | Key Feature |
| --- | --- | --- |
| **Histogram** | Numerical | Bars **touch**; equal-width bins; no gaps; no overlap |
| **Boxplot** | Numerical | Box = $Q_1$ to $Q_3$; line at median; whiskers to min/max **non-outliers**; dots for outliers |
| **Bar plot** | Categorical | Bars **don't touch** (gaps between); categories on x-axis |
| **Pie chart** | Categorical | Shows proportions but harder to compare (bar plot generally preferred) |

> [!info] Histogram Details
> - **Frequency table:** sort data into equal-width bins (classes)
> - **Relative frequency** $= \text{freq} \;/\; n$ — always sums to 1
> - Relative frequency histograms let you compare datasets with **different** sample sizes
> - Same data can have many valid bin choices, as long as bins are equal width with no gaps/overlap

---

## 6. Categorical Data

### Contingency Tables (Two-Way Tables)
- Contain aggregate data for **2 categorical variables** combined
- **Row proportions:** cell / row total — use when **row variable** is explanatory
- **Column proportions:** cell / column total — use when **column variable** is explanatory
- If proportions differ substantially across groups → relationship likely exists

### Visualization
- **Bar plot** — frequencies or proportions for one categorical variable (gaps between bars)
- **Pie chart** — proportions of categories (bar plots are almost always better)
- **Side-by-side plots** — separate numerical data by categories from a categorical variable, then plot (e.g., boxplot or histogram) for each category on the **same figure**
  - This uses a categorical variable as **explanatory** for a numerical **response**

---

## 7. Correlation

$$r = \frac{1}{n-1}\sum_{i=1}^{n}\left(\frac{x_i - \bar{x}}{s_x}\right)\left(\frac{y_i - \bar{y}}{s_y}\right)$$

Requires **paired** observations of **2 numerical** variables: $(x_1, y_1), (x_2, y_2), \ldots, (x_n, y_n)$

Preliminary computations needed: $\bar{x}$, $\bar{y}$, $s_x$, $s_y$

### Properties of $r$

--- start-multi-column: corrProps
```settings
Number of Columns: 2
Largest Column: standard
Border: off
```

- Range: $-1 \leq r \leq +1$
- $r = \pm 1$ → perfect linear relationship
- $r = 0$ → no **linear** relationship (could still have a nonlinear one!)
- **Sign** → direction (positive or negative)
- **Magnitude** → strength (closer to $\pm 1$ = stronger)

--- column-break ---

- **Unitless** — doesn't change with unit changes
- **Symmetric:** $r(X,Y) = r(Y,X)$
- **Invariant under translation:** adding/subtracting a constant doesn't change $r$
- **Invariant under scaling:** multiplying/dividing by a positive constant doesn't change $r$
- Only measures **LINEAR** relationships (misses curves!)
- **Sensitive** to outliers

--- end-multi-column

> [!warning] Always Plot Your Data!
> $r$ can be very misleading. A strong nonlinear relationship can have $r \approx 0$.
> **Anscombe's quartet:** 4 completely different datasets all have $r = 0.816$ and the same regression equation $\hat{y} = 3 + 0.5x$. Visual inspection is essential!

### Quadrant Contributions

*Divide the scatterplot at $(\bar{x}, \bar{y})$:*

| Quadrant | Position | $(x_i - \bar{x})$ | $(y_i - \bar{y})$ | Product → Contribution |
| --- | --- | --- | --- | --- |
| 1 (top-left) | $x < \bar{x}$, $y > \bar{y}$ | $-$ | $+$ | **Negative** |
| 2 (top-right) | $x > \bar{x}$, $y > \bar{y}$ | $+$ | $+$ | **Positive** |
| 3 (bottom-left) | $x < \bar{x}$, $y < \bar{y}$ | $-$ | $-$ | **Positive** |
| 4 (bottom-right) | $x > \bar{x}$, $y < \bar{y}$ | $+$ | $-$ | **Negative** |

---

## 8. Linear Regression

### Least-Squares Regression Line

$$\hat{y} = b_0 + b_1 x$$

$$b_1 = r \cdot \frac{s_y}{s_x} \qquad \text{(slope)} \qquad\qquad b_0 = \bar{y} - b_1\bar{x} \qquad \text{(intercept)}$$

- The least-squares line **minimizes** $\displaystyle\sum_{i=1}^{n}(y_i - \hat{y}_i)^2$ (sum of squared residuals)
- The line **always passes through** the point $(\bar{x}, \bar{y})$

### Interpretation — ALWAYS Include Units & Context

- **Slope** $b_1$: "For each 1-[unit] increase in $x$, we **predict** $y$ changes by $b_1$ [units]"
- **Intercept** $b_0$: "When $x = 0$, the **predicted** $y$ is $b_0$ [units]"

> [!danger] Intercept Interpretation
> Only interpret the intercept if $x = 0$ **makes sense in context** and is **within the data range**. Otherwise it may be extrapolation error (e.g., negative blood alcohol content).

### Residuals

$$e_i = y_i - \hat{y}_i = \text{observed} - \text{predicted}$$

--- start-multi-column: residuals
```settings
Number of Columns: 2
Largest Column: standard
Border: off
```

- **Positive** residual → point **above** line (model **underestimates**)
- **Negative** residual → point **below** line (model **overestimates**)
- $\sum e_i = 0$ always
- Least squares minimizes $\sum e_i^{\,2}$

--- column-break ---

### Residual Plot Diagnostics
Plot residuals vs. $x$ (or $\hat{y}$):
- **Good:** random scatter around 0 (rectangle shape), no pattern
- **Bad — Nonlinear:** curved pattern (U-shape or S-shape) → linear model is wrong
- **Bad — Heteroscedasticity:** fan/cone shape → spread of residuals changes across $x$, non-constant variance

--- end-multi-column

> [!info] Why Residual Plots Matter
> A regression line that looks good on a scatterplot might actually be a poor model — residual plots reveal hidden patterns. Outliers in residual plots heavily influence the regression line.

### $R^2$ — Coefficient of Determination

$$R^2 = r^2$$

- **Proportion of variation** in $Y$ explained by the regression on $X$
- Range: $0$ to $1$ (equivalently 0% to 100%)
- Interpretation: "$R^2 \times 100$% of the variation in [Y] is explained by [X]"

> [!tip] $R^2$ vs. $r$
> Use $R^2$ to describe the **strength** of the linear relationship.
> Use $r$ to describe the **direction** (positive vs. negative).

### Predictions

--- start-multi-column: predictions
```settings
Number of Columns: 2
Largest Column: standard
Border: off
```

**Interpolation**
Predict **within** the range of observed $x$-values
→ **Reliable**

--- column-break ---

**Extrapolation**
Predict **outside** the range of observed $x$-values
→ **NOT reliable** (can produce nonsensical results)

--- end-multi-column

### Key Differences: Regression vs. Correlation

| | Correlation ($r$) | Regression ($\hat{y} = b_0 + b_1 x$) |
| --- | --- | --- |
| **Switching $X \leftrightarrow Y$** | Does **NOT** change | **Changes** (different slope & intercept) |
| **Directionality** | Symmetric | Directional ($X$ explains $Y$) |

---

## Formula Quick Reference

| Name | Formula |
| --- | --- |
| Mean | $\bar{x} = \dfrac{1}{n}\displaystyle\sum_{i=1}^n x_i$ |
| Variance | $s^2 = \dfrac{\displaystyle\sum_{i=1}^n (x_i - \bar{x})^2}{n-1}$ |
| Standard Deviation | $s = \sqrt{s^2}$ |
| IQR | $Q_3 - Q_1$ |
| Outlier Fences | $Q_1 - 1.5(\text{IQR})$ and $Q_3 + 1.5(\text{IQR})$ |
| Relative Frequency | $\dfrac{\text{frequency}}{n}$ (sums to 1) |
| Correlation | $r = \dfrac{1}{n-1}\displaystyle\sum_{i=1}^n\left(\dfrac{x_i - \bar{x}}{s_x}\right)\!\left(\dfrac{y_i - \bar{y}}{s_y}\right)$ |
| Slope | $b_1 = r \cdot \dfrac{s_y}{s_x}$ |
| Intercept | $b_0 = \bar{y} - b_1\bar{x}$ |
| Regression Line | $\hat{y} = b_0 + b_1 x$ |
| Residual | $e = y - \hat{y}$ |
| R-squared | $R^2 = r^2$ |

---

## Exam Strategy

### Common Traps

> [!danger] Watch Out For These
> - "Associated" ≠ causation — need **random assignment** for causation!
> - Discrete = countable integers only; continuous = any value in a range
> - Bar plots ≠ histograms — categorical vs. numerical; gaps vs. touching bars
> - Switching $X \leftrightarrow Y$: correlation **unchanged**, regression line **changes**
> - Extrapolation = **unreliable** predictions outside data range
> - "Right-skew" = tail on the **RIGHT**, peak on the left — named by **tail**, not peak!
> - $r$ only measures **LINEAR** relationships — plot your data!
> - Don't interpret the intercept if $x = 0$ is outside the data range
> - Variance divides by $n - 1$, not $n$
> - Regression equation + correlation alone do NOT fully describe data — **always plot!**

### Decision Trees

**Mean vs. Median?**
- Outliers or skew? → **Median & IQR**
- Symmetric, no outliers? → **Mean & Std Dev**

**Can we claim causation?**
- Randomized experiment with random assignment? → **YES**
- Observational study? → **NO** (correlation only)

**Can we generalize to the population?**
- Random sampling? → **YES**
- No random sampling? → **NO** (applies to sample only)

**Is the prediction reliable?**
- Within data range (interpolation)? → **YES**
- Outside data range (extrapolation)? → **NO**

### Show Your Work
- Write formula → plug in values → solve step by step
- Include **units and context** in ALL interpretations
- Use **"predicted"** language for regression — not definitive statements
