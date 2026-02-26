# A systematic map of studies testing the relationship between temperature and animal reproduction

## Overview
- Purpose: Dataset accompanying a meta-analysis to assess how temperature affects animal reproduction, enabling replication and exploration of results.
- Scope: Data derived from 339 studies spanning 308 invertebrate species; used to examine effects on reproduction and longevity under different temperatures.
- Output intended for reproducible analyses and data products (e.g., dashboards, reports).

## Data contents
- all_data.csv
  - Univariate dataset with one row per study comparison.
  - Key metric: standardized mean difference in reproduction or longevity between a reference temperature and an experimental temperature (es); associated variance (v).
- multivariate_data.csv
  - Subset where both reproduction and longevity were measured in the same individuals.
  - Each row contains two effect sizes (es_reproduction, es_longevity) and their variances (v_reproduction, v_longevity).
- reproduction_tree.nex
  - Phylogenetic tree for species with reproduction data.
- longevity_tree.nex
  - Phylogenetic tree for species with longevity data.

## Data structure and metadata
- Columns cover study and species information, experimental conditions, and outcomes. Selected examples:
  - Paper.code, Paper.number, Paper, Publication.year, Title, DOI
  - Species.latin, Family, Class, Phylum
  - Life.stage.of.animal, Sex.exposed, Exposure.duration
  - Habitat, Mobility, Thermoregulation
  - Lab.or.field, Animal.origin, Stressor.variation
  - Reproductive traits and longevity traits (Trait.category, Trait)
  - Rearing.temperature, treattemp, reftemp, diff, warm.cool, c_treattemp
  - es, v (and es_reproduction/v_reproduction, es_longevity/v_longevity for respective datasets)
- Several fields describe experimental design and context (e.g., constant vs fluctuating temperatures, acclimation, agricultural relevance).

## Collection and quality control
- Data collection
  - Systematic literature search identifying studies reporting temperature effects on both reproduction and longevity/survival for the same species.
  - Data extracted from 339 studies across 308 invertebrate species.
  - Involvement of 30 researchers in data extraction.
- Quality control
  - Authors’ reported data were used; extracted data quality-checked by Fay Frost or LRD prior to analysis.

## Practical use for data support
- Reproducibility
  - Raw effect sizes and variances enable replication of univariate and, when using multivariate_data.csv, multivariate meta-analyses.
  - Phylogenetic trees support phylogenetic comparative analyses.
- Data exploration and product development
  - Rich metadata allows filtering by taxon, life history, habitat, experimental conditions, and temperature regimes.
  - Enables creation of dashboards, pivot tables, and other self-serve data products.
- Documentation and provenance
  - Comprehensive column-level descriptions (e.g., Paper.code, es, v, reftemp, treattemp) support transparent data use and traceability.
- Citation and reuse
  - Data tied to a published systematic map: Dougherty et al. 2024, Ecological Solutions and Evidence, 5(1), e12303.

## Limitations and considerations
- Heterogeneity across studies (experimental designs, measurement scales, and taxonomic breadth).
- Reliance on authors’ reported data; potential inconsistencies or missing details in some studies.
- Patchy data coverage for certain taxa or temperature ranges; careful filtering may be needed for robust analyses.

## How to access and cite
- Files provided for download:
  - all_data.csv
  - multivariate_data.csv
  - reproduction_tree.nex
  - longevity_tree.nex
- Primary reference for context and methodology: Dougherty, L. R., et al. (2024). A systematic map of studies testing the relationship between temperature and animal reproduction. Ecological Solutions and Evidence, 5(1), e12303. doi:10.1002/26888319.12303