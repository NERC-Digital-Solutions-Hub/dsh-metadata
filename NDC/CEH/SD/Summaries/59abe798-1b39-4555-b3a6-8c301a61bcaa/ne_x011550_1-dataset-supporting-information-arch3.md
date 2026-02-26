# A systematic map of studies testing the relationship between temperature and animal reproduction

## Overview
- Purpose: Provide a dataset to assess how temperature affects animal reproduction, enabling scrutiny of policy implications and informing future decisions.
- Scope: Systematic extraction from 339 studies spanning 308 invertebrate species; focuses on temperature effects on both reproduction and longevity/survival within the same species.
- Team: 30 researchers contributed to data extraction; quality control by project leads Fay Frost (FF) and L.R.D. (LRD).

## Data outputs and structure
- Files included
  - all_data.csv: Contains single-row comparisons with standardized mean difference (es) for reproduction or longevity between a reference temperature and a treatment temperature (univariate analyses).
  - multivariate_data.csv: Subset where both reproduction and longevity were recorded for the same individuals (two effect sizes per row; used for multivariate analyses).
  - reproduction_tree.nexus: Phylogenetic tree for species with reproduction data.
  - longevity_tree.nexus: Phylogenetic tree for species with longevity data.
- Core measures
  - es: Standardized mean difference in life-history traits between reference and treatment temperatures.
  - v: Variance of the effect size.
  - es_reproduction / v_reproduction: Reproduction-specific effect size and variance.
  - es_longevity / v_longevity: Longevity-specific effect size and variance.
- Metadata and data structure
  - 46+ columns capturing study and species details, experimental conditions, and data specifics (e.g., Paper.code, Paper, Publication.year, Species.latin, Habitat, Lab.or.field, Exposure.duration, Life.stage.of.animal, Treatment.temp, Reference.temp, diff, reftemp, treattemp, warm.cool, es_reproduction, es_longevity, etc.).

## Methods and data collection
- Study identification: Systematic search for studies reporting temperature effects on reproduction and longevity/survival in the same species.
- Data extraction: Means and variances of relevant life-history traits extracted per temperature treatment.
- Verification: Data checked by FF or LRD prior to analysis.
- Coverage: Data aggregated from published papers; 339 studies contributed data across a broad range of taxa (primarily invertebrates).

## How this supports monitoring frameworks
- Provides standardized quantitative measures of how temperature affects reproduction and survival across species, useful for trend analysis and policy assessment.
- Rich metadata supports data provenance, verification, and reproducibility, aligning with data governance best practices.
- The explicit data structure (univariate and multivariate datasets; phylogenetic trees) facilitates integration into monitoring dashboards, dashboards, and evidence-informed decision making.

## Practical considerations for policymakers and managers
- Data openness: Fully described datasets enable public sharing and re-use, addressing transparency and governance needs.
- Metadata depth: Comprehensive fields help in evaluating data applicability to local monitoring contexts and ensuring metadata sufficiency for interpretation.
- Data transformation: Standardized effect sizes (SMDs) allow cross-study comparability, aiding synthesis for environmental health indicators.
- Limitations and caveats: Relies on published data and relies on original study quality; downstream analyses depend on ongoing data updates and completeness of metadata.

## Reference
- Dougherty, L. R., Frost, F., Maenpaa, M. I., Rowe, M., Cole, B. J., et al. (2024). A systematic map of studies testing the relationship between temperature and animal reproduction. Ecological Solutions and Evidence, 5(1), e12303. DOI: https://doi.org/10.1002/26888319.12303