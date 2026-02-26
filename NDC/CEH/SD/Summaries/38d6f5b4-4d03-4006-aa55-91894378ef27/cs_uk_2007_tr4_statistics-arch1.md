# Countryside Survey 2007: Statistical Methodology

## Executive Summary
- Describes the statistical methodology used to analyse Countryside Survey (CS) data and outlines changes introduced for CS in 2007.
- Old methods were robust but produced inconsistencies: stock estimates used all data from a survey, while change estimates used only repeated measurements, causing mismatches between stock and change.
- Modelling with CS Broad Habitat data showed that consistent estimation is feasible and robust; differences from old methods were generally small.
- The 2007 CS adopts a modelling approach for both stock and change to achieve consistency and efficiency, using all available information.
- The modelling approach requires additional distributional assumptions, prompting validation checks against the previous methodology, especially for small data subsets.
- Benefits include more precise estimates and improved use of all information; estimates for earlier surveys can be updated as new data arrive, though changes are usually small.
- Implementation is technically challenging and computationally intensive, involving iterative model fitting rather than formula-based calculations; practical issues stem from CS’s complex sampling.
- The new approach has been applied to Broad Habitats and soil data, and found to be feasible across both square and plot levels, leading to a decision to adopt it for CS 2007.

## 1. Introduction
- This technical report provides an overview of CS sampling and analysis procedures, reviews the previous methodology, explains the changes for CS 2007, and discusses limitations and implications.
- References to fuller expositions of CS sampling and estimation are provided (Barr et al. 1993).

## 2. Overview of Previous CS Methodology
- CS Field Survey data come from a stratified sample of 1 km squares on a 15 km GB grid; two levels of sampling within each square (square-level and within-square plots).
- Land Classification stratification evolved: GB 32 classes originally; CS2000 expanded to 42; CS 2007 to 45 classes (England, Wales, Scotland with country-specific classifications).
- Estimation: previous method calculated means and standard errors for each Land Class and then combined them (weighted by land area) to yield regional/national estimates. Assumptions included independence of Land Class estimates.
- Bootstrapping: significance testing for square-level data used bootstrap due to concerns about normality (CS2000 onward).

## 3. Reasons for Modifications to CS Methodology
- Inconsistencies: prior reporting showed stock and change estimates that could not be reconciled (stock from all squares vs. change from repeated measurements).
- Causes: missing information due to new squares being added over time, landowner refusals, and other non-repeated data between survey pairs.
- Evaluation of approaches: considered three options to achieve consistency (all-squares stock with change from repeats, repeated-squares stock with change from repeats, or modelling approaches). Modelling offered consistent and robust estimates for both square and plot data.
- Decision: adopt modelling for consistency and efficiency, despite requiring stronger distributional assumptions.

## 4. Modelling Basics
- Incomplete data techniques (EM algorithm, etc.) underlie the modelling approach; models use data from all surveys to produce consistent stock and change estimates.
- Models involve fixed effects (stock/change values by survey) and random effects (reflecting sampling structure and variability).
- Distributional assumptions are necessary; robustness of fixed effects is a key strength, but variance/covariance components require careful specification.
- Two main data levels addressed: square-level and plot-level data, each with appropriate mixed-effect/repeated-measures modelling.

## 4.3 Square Level Data
- Treated as a repeated measures model with two components:
  - Fixed effects: land-class means for each survey (regression of the variable on year/survey as a categorical variable).
  - Random effects: square-level deviations within land classes; correlated successive survey deviations.
- When scaled by land-class area, fixed effects yield stock estimates; differences between successive fixed effects give change estimates, ensuring consistency.

## 4.4 Plot Level Data
- Plot-level data within squares present a hierarchy not fully exploited in earlier CS analyses.
- Approaches varied (square-level aggregation, treating plots as independent); risks included biased standard errors.
- The recommended practice uses mixed models that include square-level random variation and, optionally, plot-level residuals; both options can be bootstrapped to obtain robust SEs.

## 4.5 Model Specification
- General square-level model: y_ijk = a_ik + s_ij + e_ijk
  - a_ik: fixed effects (land-class means for survey k)
  - s_ij: square random effect within land class i
  - e_ijk: repeated-measures residual
- Distributional assumptions:
  - s_ij ~ N(0, τ_i^2) varies by land class
  - e_ijk ~ N(0, σ_ik^2) with covariances between surveys varying by land class and pair of surveys
- Parameter considerations:
  - For K surveys, there are K fixed effects per land class but many random-effect parameters (variances and covariances), leading to potential instability with many land classes and limited squares.
- Reducing random effects:
  - Common approach is to assume variance parameters do not vary across surveys (σ_i common across surveys).
  - Use AR1 (autoregressive) structure to model covariances across surveys, reducing repeated-measures parameters to one per land class.
- Estimation and inference:
  - Fixed effects are relatively robust to mis-specification of random effects; variances/covariances are more sensitive.
  - Bootstrap can be used to obtain robust standard errors.
  - AR1 model with bootstrap was investigated as a practical, robust solution.

## 4.6 Model Testing – Broad Habitats
- Previous CS output included stock and change for Broad Habitats (from 1984, 1990, 1998; 1978 not directly comparable).
- Past approach produced inconsistencies when comparing stock vs. change (based on different data subsets).
- Modelling (AR1) applied to these datasets yields consistent estimates; changes across periods align with stacked differences in stock estimates.
- Comparisons show that most differences between old and new methods fall within the existing discrepancies of the old approach; estimates remain within prior error bounds.
- Additional checks included applying the modelling approach to soil data (1978, 1998) and plot-level data, confirming feasibility of consistent estimates across data scales.

## 5. Limitations and Implications
- While feasible, model-based analysis with bootstrapping is computationally intensive; fitting full parameterised models is slow, so a practical AR1 model is preferred for automated, large-scale analysis.
- Fixed-effects estimates (stock/change) are robust, but variance/covariance estimates require careful handling; bootstrap improves reliability.
- Transformations to non-original scales can complicate interpretation due to back-transformations involving random effects.
- In some variables with highly non-normal distributions (e.g., freshwater standing water), the new method may converge to local maxima; in such cases, the old method may be retained for that variable.
- Overall benefits: more precise estimates by exploiting all available information and correctly representing the data hierarchy.
- Implications for reporting: because new information updates estimates for earlier surveys, results may shift slightly over time; this reflects genuine learning rather than misreporting.
- Practical outcome: a standard AR1 modelling approach with bootstrap is adopted for CS 2007 to balance accuracy, robustness, and practical feasibility.

## 6. References
- Barr et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, Laird, Rubin (1977). EM algorithm for incomplete data.
- Efron, Tibshirani (1993). Bootstrap methods.
- Haines-Young et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott (2002). Maximum likelihood estimation with empirical Fisher information.
- Additional CS documentation and project communications cited in the report.