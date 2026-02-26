# Statistical methodology used for the analysis of Countryside Survey data

- Purpose and scope
  - Describes the statistical methodology for analysing Countryside Survey (CS) data.
  - Documents why changes were made to estimation procedures for CS2007 and outlines the modelling-based approach to achieve consistent stock and change estimates over time.
  - Compares new modelling methods with the previous, more ad hoc approaches and discusses limitations and implications.

- Background: previous CS methodology
  - Earlier methods estimated stock (using all data in a survey) and change (from repeated measurements across surveys), leading to inconsistencies where stock and change did not align.
  - Stock and change could be inconsistently estimated due to mismatches in data used for each quantity, particularly with missing information and new squares entering the survey over time.
  - Reporting focus shifted from adjacent-survey changes to timelines spanning multiple surveys, motivating a move toward consistency.

- Why modifications were made (the rationale)
  - Inconsistencies between stock and change estimates were recognized as a consequence of using different data subsets for stock and change.
  - Consistent, efficient estimation could be achieved with modelling that uses all available information and properly handles missing data.
  - Modelling approaches can provide more precise estimates, though they require stronger distributional assumptions and greater computational resources.
  - For CS2007, a modelling approach was adopted and validated by comparing results with the old methodology to ensure compatibility.

- The modelling approach to consistent estimation
  - Concepts
    - Uses mixed effects and repeated measures models to exploit data from all surveys.
    - Fixed effects represent land-class means across surveys; random effects capture survey-to-survey and within-square (or plot) variability.
    - Stock and change are derived from fixed-effect estimates after fitting the model.
  - Data structure
    - Two levels: 1 km squares (square-level data) and plots within squares (plot-level data).
    - Land classification by country (England, Wales, Scotland) with 45 classes in CS2007, effectively country-specific classifications.
  - Estimation framework
    - Square-level data: treated as repeated measures within land classes; a mixed model is used to estimate stock and change consistently.
    - Plot-level data: extended modelling to include plot-level random effects in addition to square-level effects; can be embedded within bootstrapping.
  - Model specification and reductions
    - General form for square-level data: y_ijk = a_ik + s_ij + e_ijk
      - a_ik: fixed effects (land class means by survey)
      - s_ij: square random effects
      - e_ijk: repeated measures effects
    - Random effects are assumed normally distributed with land-class-specific variances; covariances modelled across surveys.
    - To keep models tractable, random-effect parameterization is reduced using:
      - AR1 (first-order autoregressive) structure for covariances (covariances depend on adjacent surveys; non-adjacent values conditionally independent given intervening surveys).
      - Common variance parameters across surveys within a land class (σ_i) and common autoregressive structure.
    - The combination (AR1 with bootstrap SEs) yields three random-effect parameters per land class per survey, irrespective of the number of surveys.
  - Estimation of uncertainty
    - Bootstrap used to obtain standard errors and confidence intervals, accommodating non-normal data distributions and ensuring robustness of fixed-effect estimates.

- Practical considerations and outputs
  - Implementing the AR1 model with bootstrap SEs was chosen for practicality, robustness, and automation across many variables.
  - The modelling approach tends to update previous survey estimates as new data become available, leading to small revisions in historical figures.
  - The method leverages all available information and respects the data hierarchy, improving precision over the old approach.

- Model testing and results (Broad Habitats example)
  - Re-examined data from seven Broad Habitats across 1984, 1990, and 1998 to assess feasibility before full adoption.
  - Old method showed inconsistencies between stock and change; the AR1 modelling approach produced estimates that matched the logical differences between stock and change (consistency by construction).
  - Differences between old and new methods were generally within the old method’s own error bounds; most differences were small, with no large outliers.
  - The modelling approach also extended to plot-level and soil data, indicating broader applicability and consistency.

- Limitations and implications
  - Computational demands are higher; AR1 bootstrap analyses are slower than the old methods, but feasible for large numbers of variables.
  - Model selection is constrained by the need for automation; fixed-effect estimates are robust, but variance/covariance parameter estimates are more sensitive to distributional assumptions.
  - Very non-normal data can pose convergence issues (e.g., standing water in CS freshwater data led to reliance on the old method for that variable).
  - When adopting consistent estimation, estimates for any one survey can be influenced by information from all surveys, meaning that results for earlier surveys may be revised as new data are added.
  - The approach improves efficiency and use of information, and provides a coherent framework for comparing data across time and across data levels (square and plot).

- Implications for data users and data sharing
  - Consistent estimation facilitates better integration with other datasets and allows scrutiny of environmental health and policy performance over time.
  - Enhanced data transparency and robustness support more reliable trend analyses and decision-making.
  - Because earlier surveys can be revised with new data, users should treat historical figures as subject to update rather than fixed absolutes.

- Key takeaway for Analysts Monitoring the Environment
  - A modelling-based, consistent estimation framework (AR1 mixed models with bootstrap) improves precision and coherence of stock and change estimates across multiple CS surveys.
  - This approach uses all available data, respects data hierarchy (square and plot levels), and reduces inconsistencies between different output measures.
  - While more computationally intensive and reliant on distributional assumptions, the method provides robust results and enables more reliable long-term environmental monitoring and policy evaluation.