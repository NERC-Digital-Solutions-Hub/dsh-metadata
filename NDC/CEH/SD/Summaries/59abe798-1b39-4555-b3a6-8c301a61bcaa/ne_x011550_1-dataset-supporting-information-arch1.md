# A systematic map of studies testing the relationship between temperature and animal reproduction

## Aim
- Compile and provide data to assess how temperature affects animal reproduction, enabling univariate and multivariate meta-analyses and the development of predictive insights about temperature impacts.

## What the dataset covers
- Meta-analysis dataset examining temperature effects on reproduction, with additional data on longevity.
- Scope includes 339 studies covering 308 invertebrate species.
- Focused on studies that report temperature effects on both reproduction and longevity/survival within the same species.

## Data generation and collection methods
- Systematic literature search to identify relevant studies.
- Data extracted from papers reporting temperature effects on both reproduction and longevity.
- Data collection involved 30 researchers, coordinated to extract relevant effect size information.

## Data types and structure
- all_data.csv: Each row is a single comparison, containing effect sizes (es) and variances (v) for reproduction or longevity, used for univariate meta-analyses. Key metric: standardized mean difference between a reference temperature and an experimental temperature.
- multivariate_data.csv: Subset where both reproduction and longevity were recorded for the same individuals; each row includes two effect sizes (reproduction and longevity) used for multivariate meta-analyses.
- reproduction_tree.nexus: Phylogenetic tree for species with reproduction data.
- longevity_tree.nexus: Phylogenetic tree for species with longevity data.
- Column-level metadata: 40+ fields describing studies and species (e.g., Paper.code, Publication.year, Species.latin, Habitat, Sex.exposed, Thermoregulation, Exposure.duration, Life.stage, reftemp, treattemp, es_reproduction, es_longevity, etc.).

## How data are structured and used
- es and v columns provide effect sizes and their uncertainties for analyses.
- es_reproduction and v_reproduction for reproduction-focused analyses; es_longevity and v_longevity for longevity-focused analyses.
- diff, reftemp, treattemp, and warm.cool summarize temperature contrasts.
- Trait and contextual metadata (e.g., Lab.or.field, Habitat, Class/Family, Mobility) enable subgroup analyses and exploration of moderators.

## Quality control
- Dependence on authors to report accurate data; extracted data were checked by Fay Frost (FF) or LRD before analysis.

## Access and usage considerations
- Enables replication of meta-analyses and exploration of temperature-reproduction relationships across taxa.
- Analyses can incorporate phylogenetic structure via the provided reproduction and longevity trees.
- Rich metadata supports sensitivity analyses by study design, environment, and species traits.

## Limitations and considerations
- Predominantly invertebrate species (308 across 339 studies), which may limit generalization to vertebrates.
- Variability in study design, environments (lab vs. field), and reporting standards across studies.
- Data quality depends on original reporting; some studies may have incomplete metadata.
- Potential biases from selective reporting and cross-study heterogeneity in temperature treatments and life-history measurements.

## Reference
- Dougherty, L. R., Frost, F., Maenpaa, M. I., Rowe, M., Cole, B. J., ... Price, T. A. R. (2024). A systematic map of studies testing the relationship between temperature and animal reproduction. Ecological Solutions and Evidence, 5(1), e12303. doi: 10.1002/26888319.12303