# Countryside Survey 2007: Statistical Methodology

- Purpose: Describe the statistical methods used to analyze Countryside Survey (CS) data, summarize previous methodologies, and explain the changes adopted for CS2007 to improve consistency, precision, and use of available information.

## Executive summary of the methodological changes

- Previous methods were robust but produced inconsistencies: stock (all data in a survey) versus change (repeat measurements) could yield non-matching estimates.
- Investigations showed modelling (consistent estimation) was feasible and robust, and differences from old methods were generally within existing inconsistencies.
- CS2007 adopts a modelling approach that uses all available data to produce more precise stock and change estimates.
- Modelling requires additional distributional assumptions; results were validated by comparing with previous methods, especially for small subsets.
- The modelling approach improves efficiency and consistency across surveys but requires more computer time and careful model checking.

## Introduction and scope

- The document outlines sampling and analysis procedures for CS data, reviews the previous methodology, details changes for 2007, and discusses limitations and implications.
- Full technical details of earlier CS sampling and estimation are referenced (Barr et al., 1993).

## Sampling design

- Data come from a stratified sample of 1 km squares at the intersection of a 15 km GB grid.
- Two levels of sampling: square level (covering the whole square) and plot level (within squares) for more detailed measurements.
- Measurements include binary and continuous variables (e.g., vegetation, soils).
- Land Classification (ITE) stratification evolved: 32 classes originally, then 42 (CS2000) for Scotland reporting, and 45 classes (CS2007) to accommodate Wales reporting; in practice, each country has its own related set of classes.

## Estimation – old approach

- Regional/national estimates: compute means and standard errors by Land Class, then weight by land area to obtain region estimates.
- Stock estimates used all data from a survey; change estimated from repeated measurements only.
- Assumptions: independence between Land Classes and between class estimates; minimal distributional assumptions, with bootstrap used for significance testing in some cases.

## Why try modelling for consistency

- Inconsistencies arose because stock and change were derived from different data subsets (all data vs repeated data).
- Three potential consistent approaches (conceptually) exist; modelling offers a unified, consistent framework for both square and plot level data, with improved precision.

## Modelling basics

- Modelling deals with incomplete data via mixed effects/repeated measures models, enabling stock and change to be estimated from all available data.
- Models include fixed effects (means by Land Class over time) and random effects (accounting for sampling structure and repeated measures).
- Models require distributional assumptions for random effects; robustness of fixed-effect estimates is emphasized.

## Square level data modelling

- Treats data as a repeated measures/mixed model within Land Classes.
- Simple fixed effect: land-class means across surveys; stock estimates are the fixed effects scaled by land area.
- Random effects: square-level deviations and within-square (survey-to-survey) correlations.
- Correlation structures allow for repeated measurements across surveys within squares.

## Plot level data modelling

- Plot-level measurements within squares are incorporated to better utilise hierarchical structure.
- Earlier approaches either summarised to square level or treated plots as independent, risking biased SEs.
- Current approach extends the square-level model to include an additional plot-level random effect, with bootstrapping used to obtain robust SEs.

## Model specification and parameter reduction (AR1 approach)

- General square-level model: y_ijk = a_i_k + s_ij + e_ijk
  - a_i_k: fixed effects (land-class means for survey k)
  - s_ij: square-level random effect
  - e_ijk: repeated-measures residual
- Random effects are assumed normally distributed with land-class-specific variances; repeated-measures covariances vary by land class and survey pair.
- To keep models stable and computationally feasible with many surveys and land classes, random-effect parameters are reduced using:
  - Common within-land-class variance across surveys (σ_i)
  - Autoregressive AR1 structure for repeated-measures covariance (one parameter per land class, per survey, plus a single autocorrelation parameter)
- Result: three random-effect parameters per survey per land class, regardless of the number of surveys.
- Fixed effects estimation is robust to some mis-specification of random effects; bootstrap is recommended for standard errors due to potential non-normality or complex variance structures.

## Model testing – Broad Habitats

- Historically, Broad Habitat stocks and changes were estimated separately; inconsistencies between stock-derived change and repeat-squares-derived change were evident.
- Using AR1 mixed models (square-level data) across 1984, 1990, and 1998 showed that modelling produced consistent estimates, with changes equal to differences in stock estimates or sums of inter-survey changes.
- Comparisons between old and new methods showed no estimates outside old-method error bounds; most differences were small relative to existing inconsistencies.

## Limitations and practical implications

- Bootstrapped SEs with AR1 models are computationally intensive; fully parameterised models can be slow.
- AR1 model provides a good balance of stability, speed, and robustness for fixed effects; however, variance/covariance estimates can be sensitive to distributional assumptions.
- Very non-normal data can cause convergence issues (e.g., standing water in CS freshwater data); in some cases, old methodology results may be preferred.
- Analyses use data from all surveys; as new data are added, previous survey estimates may be updated, meaning past results are not fixed in stone across reporting occasions.
- Automated, standard modelling approaches were favored to enable application to large numbers of variables.

## Implications for monitoring frameworks

- More efficient use of data and a consistent framework across time improves comparability and precision of environmental health indicators derived from CS data.
- Data updates with new surveys will refine earlier estimates, which is conceptually acceptable as more information becomes available.
- Adoption of a standard AR1-based mixed model with bootstrap SEs provides robust, scalable outputs suitable for informing policy and monitoring.

## References (selected)

- Barr, C.J. et al. (1993). Countryside Survey 1990 Main Report.
- Dempster, A.P. et al. (1977). Maximum likelihood from incomplete data via EM algorithm.
- Efron, B. & Tibshirani, R.J. (1993). An introduction to the bootstrap.
- Haines-Young, R.H. et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Scott, W.A. (2002). Maximum likelihood estimation using the empirical Fisher information matrix.