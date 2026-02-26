# A systematic map of studies testing the relationship between temperature and animal reproduction

## Overview
- A dataset describing the results of a meta-analysis on how temperature affects animal reproduction.
- Contains data necessary to replicate the meta-analyses: two CSV files (univariate and multivariate) and two phylogenetic trees (reproduction and longevity).

## Data Scope and Purpose
- Scope: 339 studies across 308 invertebrate species, with data contributed by 30 researchers.
- Purpose: to quantify temperature effects on reproduction and longevity across species, enabling univariate and multivariate meta-analyses.
- Key output: standardized mean differences in life-history traits between reference and treatment temperatures, with associated variances.

## Data Collection and Curation
- Methods: systematic literature search to identify studies reporting temperature effects on both reproduction and longevity/survival for the same species; extracted relevant effect sizes.
- Data extraction: means and variances for life-history traits at each reported temperature treatment.
- Quality control: data checked for accuracy by two researchers (FF and LRD) prior to analysis.
- Data provenance: 339 studies, with detailed study and species metadata captured in structured fields.

## Data Structure and Variables
- Core data files:
  - all_data.csv: univariate dataset; one row per comparison; key columns include effect size (es) and variance (v) for reproduction or longevity.
  - multivariate_data.csv: subset where both reproduction and longevity were recorded for the same individuals; each row contains two effect sizes (one for reproduction, one for longevity) and their variances.
- Phylogenetic context:
  - reproduction_tree.nexus: phylogenetic relationships for species with reproduction data.
  - longevity_tree.nexus: phylogenetic relationships for species with longevity data.
- Column examples (46+ fields):
  - Paper.code, Paper.number, Paper, Publication.year, Title, DOI
  - Species.latin, Family, Class, Phylum
  - Sex.exposed, Fertilisation.mode, reproductive.mode
  - Agricultural.importance, Lab.or.field, Animal.origin
  - Stressor.variation, Habitat, Habitat2, Mobility, Thermoregulation
  - Country.of.origin, Continent.of.origin, Ocean.sea.of.origin
  - Exposure.duration, Life.stage.of.animal, Lowest.temp.below.10.C
  - Constant.or.fluctuating, Acclimated
  - Effect.size.code, Experiment.code
  - Trait.category, Trait, Sex, Rearing.temperature
  - es, v, diff, reftemp, treattemp, warm.cool, c_treattemp
  - es_reproduction, v_reproduction, es_longevity, v_longevity
- Data notes: They capture both the experimental temperature treatment and the reference temperature, with centered temperature values and various contextual fields.

## Files Included
- all_data.csv: all effect-size data for univariate analyses; each row corresponds to a single study comparison.
- multivariate_data.csv: subset with simultaneous reproduction and longevity data; each row contains two effect sizes (reproduction and longevity).
- reproduction_tree.nexus: phylogenetic tree for species with reproduction data.
- longevity_tree.nexus: phylogenetic tree for species with longevity data.

## Quality, Provenance, and Reproducibility
- Data provenance: compiled from published studies via a systematic map; data extraction performed by a large team of researchers.
- Reproducibility: designed specifically to enable full replication of the meta-analyses and to reuse phylogenetic contexts.
- Metadata richness: extensive per-study and per-species fields to support data discovery, screening, and replication.
- Limitations acknowledged implicitly by design: reliance on reported data and potential variability across studies; some fields may be incomplete depending on source reports.

## Access, Usage, and Governance
- Intended for data leaders to assess data system design, discoverability, and governance needs for cross-study synthesis.
- Supports cross-study integration, comparison across taxa, and phylogenetic analyses of temperature effects on reproduction and longevity.
- Provides a structured foundation for maintaining metadata standards, data quality checks, and provenance in collaborative, multi-author projects.