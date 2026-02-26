# A systematic map of studies testing the relationship between temperature and animal reproduction

## Overview
- A dataset assembled to assess how temperature affects animal reproduction and longevity, enabling reproducible meta-analyses and cross-study comparisons.
- Contains all data needed to repeat the meta-analyses: two CSV files with effect size data and two phylogenetic trees showing species relationships.

## What the dataset contains
- Meta-analysis outputs on temperature effects across studies and species.
- Extracted data from 339 studies covering 308 invertebrate species.
- For each study, means and variances for relevant life-history traits are provided for each reported temperature treatment.
- Two complementary data subsets:
  - All data for univariate meta-analyses.
  - Subset where reproduction and longevity were measured in the same individuals for multivariate analyses.

## Scope and data sources
- Systematic literature search identified studies reporting temperature effects on both reproduction and longevity/survival for the same species.
- Data extraction performed by a team of 30 researchers.
- Final dataset enables both univariate and multivariate meta-analyses of temperature effects on life-history traits.

## Files included
- all_data.csv: Contains the full set of effect size data (standardized mean difference in reproduction or longevity between a reference temperature and an experimental temperature). Each row represents one comparison.
- multivariate_data.csv: Subset with data from treatments where both reproduction and longevity were recorded in the same individuals; each row has two effect sizes (one for reproduction, one for longevity).
- reproduction_tree.nexus: Phylogenetic tree for species with reproduction data.
- longevity_tree.nexus: Phylogenetic tree for species with longevity data.

## Data structure and key fields (examples)
- Study and paper identifiers: Paper.code, Paper.number, Paper, Publication.year, DOI, Title.
- Species and taxonomy: Species.latin, Family, Class, Phylum.
- Experimental and biological details: Lab.or.field, Animal.origin, Habitat, Reproductive.mode, Sex.exposed, Exposure.duration, Life.stage.of.animal, Temperature-related fields (reftemp, treattemp, diff, es, v, es_reproduction, es_longevity, etc.).
- Trait and effect size: Trait.category, Trait, es/reproduction, v/reproduction, es/longevity, v/longevity.
- Treatment specifics: Reference temperature, Treatment temperature, warm.cool, c_treattemp, Lowest.temp.below.10.C, Constant.or.fluctuating, Acclimated.

## Quality control
- Data relied on authors to report measurements; extracted data were checked by Fay Frost (FF) or LRD before analysis.
- Aims to ensure accurate, transparent, and repeatable data for subsequent analyses.

## How the data can be used
- Supports replication of meta-analyses examining how temperature influences reproduction and longevity across a wide range of species.
- Enables cross-study comparisons and integration with other environmental monitoring datasets.
- Provides a standardised, openly structured dataset suitable for informing environmental health assessments and policy performance over time.

## Authors and provenance
- Project authors span multiple institutions, reflecting a collaborative effort to compile and quality-check a large, multispecies dataset.
- Based on a systematic map published in Ecological Solutions and Evidence (2024): A systematic map of studies testing the relationship between temperature and animal reproduction.