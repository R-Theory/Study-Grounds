# STOR 155 Midterm 1 - Flashcards

**Topics 1-7 | Exam: February 12, 2026**

---

## TOPIC 1: BASICS OF DATA

| FRONT (Question/Term) | BACK (Answer/Definition) |
|---|---|
| What is a **variable**? | A characteristic/attribute that can take different values across observations |
| What are the two main types of variables? | **Numerical (quantitative)** and **Categorical (qualitative)** |
| What are the two subtypes of numerical variables? | **Discrete** (countable: 0,1,2,3...) and **Continuous** (any value in a range) |
| What are the two subtypes of categorical variables? | **Nominal** (no order: eye color) and **Ordinal** (has order: education level) |
| Can numbers be categorical? Give an example. | **YES!** Zip codes, jersey numbers, SSN - if averaging is meaningless, it's categorical |
| What is the **population**? | The ENTIRE group you want to study/make conclusions about |
| What is a **sample**? | A SUBSET of the population that you actually collect data from |
| What is a **parameter**? | A number describing the POPULATION (usually unknown) |
| What is a **statistic**? | A number describing the SAMPLE (what we calculate) |
| Memory trick: Parameter vs Statistic? | **P**arameter → **P**opulation, **S**tatistic → **S**ample |
| What is an **explanatory variable**? | The variable that EXPLAINS or predicts (the "cause" or x-variable) |
| What is a **response variable**? | The variable being EXPLAINED or predicted (the "effect" or y-variable) |

---

## TOPIC 2: DATA COLLECTION & SAMPLING

| FRONT (Question/Term) | BACK (Answer/Definition) |
|---|---|
| What are the THREE sources of data? | 1) Anecdotes, 2) Observational Studies, 3) Experiments |
| Why are **anecdotes** bad for research? | Cannot generalize from one or few cases; individual stories aren't representative |
| What is an **observational study**? | PASSIVE data collection - observe without influencing responses |
| Can observational studies establish causation? | **NO!** Can only show correlation/association due to confounding variables |
| What is an **experiment**? | ACTIVE data collection - deliberately influence responses with treatment |
| Can experiments establish causation? | **YES!** With proper design (random assignment, control group) |
| What is a **confounding variable**? | A factor OTHER than your explanatory variable that might affect your response variable |
| Classic example of confounding? | Ice cream sales and drowning deaths - TEMPERATURE is the confounder |
| What is **Simple Random Sampling (SRS)**? | Every member has equal chance of selection (drawing names from a hat) |
| What is **Stratified Sampling**? | Divide into homogeneous groups (strata), then SRS from EACH group |
| What is **Cluster Sampling**? | Divide into heterogeneous groups, randomly select WHICH clusters, survey EVERYONE in selected clusters |
| What is **Multistage Sampling**? | Cluster sampling + SRS within selected clusters |
| What is **Convenience Sampling**? | Sample only easy-to-reach participants - BIASED! |
| What is **Voluntary Response** bias? | People choose to participate - only strong opinions respond - BIASED! |
| What is **Non-response** bias? | Planned sample is good, but many don't respond - resulting sample differs |
| Key difference: Stratified vs Cluster? | **Stratified**: homogeneous groups, sample from ALL. **Cluster**: heterogeneous groups, sample from SOME |

---

## TOPIC 3: EXPERIMENTS

| FRONT (Question/Term) | BACK (Answer/Definition) |
|---|---|
| What are the 4 principles of experimental design? | **CONTROL, RANDOMIZE, REPLICATE, BLOCK** |
| What does CONTROL mean in experiments? | Assign participants to multiple treatment groups (at least one control group) |
| What does RANDOMIZE mean in experiments? | Assign subjects RANDOMLY to treatment groups to reduce bias |
| What does REPLICATE mean in experiments? | Test on MULTIPLE subjects; must be repeatable by others |
| What does BLOCK mean in experiments? | Separate subjects into groups by a blocking variable BEFORE random assignment |
| What is a **blocking variable**? | A characteristic likely to influence outcomes (NOT what you're testing) |
| Blocking is the experimental equivalent of what? | Stratifying (in sampling) |
| What is a **placebo**? | Fake treatment (sugar pill) - controls for placebo effect |
| What is the **placebo effect**? | People improve just because they THINK they're being treated |
| What is **blinding**? | Subjects don't know which treatment they receive |
| What is **double-blind**? | NEITHER subjects NOR researchers know who got what treatment |
| Random assignment allows what type of conclusion? | **Causal** conclusions |
| Random sampling allows what type of conclusion? | **Generalizable** conclusions (to the population) |
| Observational studies can NEVER establish...? | **CAUSATION** - only correlation/association |

---

## TOPIC 4: NUMERICAL DATA ANALYSIS

| FRONT (Question/Term) | BACK (Answer/Definition) |
|---|---|
| What does SOCS stand for? | **S**hape, **O**utliers, **C**enter, **S**pread |
| What are the types of modality (Shape)? | Unimodal (1 peak), Bimodal (2 peaks), Multimodal (3+), Uniform (flat) |
| What does "right-skewed" mean? | Tail extends to the RIGHT, peak on LEFT |
| What does "left-skewed" mean? | Tail extends to the LEFT, peak on RIGHT |
| In right-skewed data, Mean vs Median? | Mean > Median (mean pulled toward tail) |
| In left-skewed data, Mean vs Median? | Mean < Median |
| In symmetric data, Mean vs Median? | Mean ≈ Median |
| Formula for **mean**? | x̄ = (1/n) × Σxᵢ |
| What is the **median**? | Middle value when data is sorted |
| Formula for **sample variance**? | s² = [1/(n-1)] × Σ(xᵢ - x̄)² |
| CRITICAL: Variance divides by...? | **(n-1)**, NOT n! |
| Formula for **standard deviation**? | s = √(variance) = √s² |
| Formula for **IQR**? | IQR = Q3 - Q1 |
| What is Q1? | 25th percentile (median of lower half) |
| What is Q3? | 75th percentile (median of upper half) |
| How to identify outliers (IQR method)? | x < Q1 - 1.5×IQR OR x > Q3 + 1.5×IQR |
| What is the **five-number summary**? | Min, Q1, Median, Q3, Max |
| Which measures are ROBUST to outliers? | Median and IQR |
| Which measures are SENSITIVE to outliers? | Mean, Variance, Standard Deviation |
| If you ADD constant c to all values, what changes? | Mean and Median shift by c; SD, Variance, Shape UNCHANGED |
| If you MULTIPLY all values by c, what changes? | Mean, Median, SD multiply by c; Variance multiplies by c²; Shape UNCHANGED |

---

## TOPIC 5: CATEGORICAL DATA ANALYSIS

| FRONT (Question/Term) | BACK (Answer/Definition) |
|---|---|
| What is a **contingency table**? | Table showing counts for TWO categorical variables combined |
| How to find proportion of total? | (Cell count) / (Grand total) |
| How to find row proportion? | (Cell count) / (Row total) |
| How to find column proportion? | (Cell count) / (Column total) |
| Bar plot vs Histogram: gaps? | Bar plot has GAPS between bars; Histogram bars are ADJACENT |
| Bar plot vs Histogram: data type? | Bar plot = Categorical; Histogram = Numerical |
| What do side-by-side plots show? | How a categorical variable influences a numerical variable |

---

## TOPIC 6: CORRELATION

| FRONT (Question/Term) | BACK (Answer/Definition) |
|---|---|
| What does correlation (r) measure? | Strength and DIRECTION of LINEAR relationship between two numerical variables |
| What is the range of r? | -1 ≤ r ≤ +1 |
| r = +1 means? | Perfect POSITIVE linear relationship |
| r = -1 means? | Perfect NEGATIVE linear relationship |
| r = 0 means? | NO linear relationship (but could have nonlinear!) |
| r > 0 indicates? | As x increases, y TENDS TO increase |
| r < 0 indicates? | As x increases, y TENDS TO decrease |
| Does r change if you add a constant to x or y? | **NO** - correlation is invariant under translation |
| Does r change if you multiply x or y by a constant? | **NO** - correlation is invariant under scaling |
| Does r change if you swap x and y? | **NO** - r(x,y) = r(y,x) |
| Can r = 0 with a strong relationship? | **YES** - if relationship is NONLINEAR (e.g., parabola) |
| Is r robust to outliers? | **NO!** Outliers can drastically change r |
| Correlation ≠ ? | **CAUSATION!** Association is not causation |

---

## TOPIC 7: LINEAR REGRESSION

| FRONT (Question/Term) | BACK (Answer/Definition) |
|---|---|
| What is a regression line? | Describes how response Y changes with respect to explanatory X |
| Equation of regression line? | ŷ = b₀ + b₁x |
| Formula for slope (b₁)? | b₁ = r × (sᵧ / sₓ) |
| Formula for y-intercept (b₀)? | b₀ = ȳ - b₁x̄ |
| What does the SLOPE represent? | Change in Y for each 1-unit increase in X |
| What does the Y-INTERCEPT represent? | Predicted value of Y when X = 0 (may not be meaningful!) |
| What is a **residual**? | Residual = Observed - Predicted = y - ŷ |
| Positive residual means? | Model UNDERESTIMATED (actual > predicted) |
| Negative residual means? | Model OVERESTIMATED (actual < predicted) |
| What is **r²** (coefficient of determination)? | Percentage of variation in Y explained by the regression line |
| How to calculate r²? | Square the correlation: r² = (r)² |
| r = 0.8 → r² = ? | 0.64 = 64% of variation explained |
| What is **interpolation**? | Predicting y for x-values WITHIN the data range - TRUSTWORTHY |
| What is **extrapolation**? | Predicting y for x-values OUTSIDE the data range - UNTRUSTWORTHY |
| What does an ideal residual plot look like? | Random scatter around 0, no pattern, constant spread |
| Curved pattern in residual plot means? | Linear model is NOT appropriate (nonlinear relationship) |
| Fan/funnel shape in residual plot means? | Heteroskedasticity (non-constant variance) - problem! |
| Does switching x and y change the regression line? | **YES!** Unlike correlation, order matters in regression |

---

## COMMON MISTAKES TO AVOID

| FRONT (Mistake) | BACK (Correction) |
|---|---|
| Variance divides by n | **NO!** Sample variance divides by (n-1) |
| Right-skewed = peak on right | **NO!** Right-skewed = TAIL on right, peak on LEFT |
| Correlation = Causation | **NEVER!** Correlation only shows association |
| r = 0 means no relationship | **NO!** Could have strong NONLINEAR relationship |
| r = 0.7 means 70% relationship | **NO!** r is not a percentage; r² = 0.49 = 49% variation explained |
| Stratified and cluster are the same | **NO!** Stratified = homogeneous groups, sample ALL. Cluster = heterogeneous, sample SOME |
| Observational studies can show causation | **NEVER!** Only experiments can establish causation |
| Outliers don't affect correlation | **WRONG!** Outliers can drastically change r |
| Extrapolation is fine | **NO!** Predictions outside data range are untrustworthy |

---

## QUICK FORMULA REFERENCE

| Formula | Expression |
|---|---|
| Mean | x̄ = Σxᵢ / n |
| Sample Variance | s² = Σ(xᵢ - x̄)² / (n-1) |
| Sample SD | s = √s² |
| IQR | Q3 - Q1 |
| Outlier bounds | Q1 - 1.5×IQR and Q3 + 1.5×IQR |
| Correlation | r = [1/(n-1)] × Σ[(xᵢ-x̄)/sₓ × (yᵢ-ȳ)/sᵧ] |
| Regression slope | b₁ = r × (sᵧ/sₓ) |
| Regression intercept | b₀ = ȳ - b₁x̄ |
| Residual | e = y - ŷ |
| R-squared | r² = (correlation)² |
| Complement rule | P(Aᶜ) = 1 - P(A) |
| Addition rule | P(A or B) = P(A) + P(B) - P(A and B) |

---

**TOTAL CARDS: ~90**

**How to use:**
1. Cover the BACK column
2. Try to answer from memory
3. Check your answer
4. Make three piles: Know it / Kinda know it / Don't know it
5. Focus on "Don't know it" pile until empty
6. Shuffle and repeat!
