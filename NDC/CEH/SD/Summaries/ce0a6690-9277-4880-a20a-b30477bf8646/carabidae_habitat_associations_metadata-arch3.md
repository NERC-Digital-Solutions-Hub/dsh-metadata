# Habitat associations of ground beetles (Carabidae) in Great Britain

## Overview
- Examines habitat associations (phi coefficient of association) of ground beetles in Great Britain using 100 m grid data.
- Aims to support landscape-scale conservation planning, including assessing habitat losses, fragmentation, dispersal, connectivity, and foraging/movement modelling.
- Provides multiple output formats and thresholds to help users gauge confidence in habitat–species associations.

## Data sources
- Carabid presence data: National Biodiversity Network (NBN) atlas (2017), with presence records at 100 m grid resolution; initial filter of at least 10 records per species; species name standardisation against NHM UK inventories.
- Absence data: NBN does not include true absence data; absences inferred using a survey-effort proxy (number of other carabid species found per location) with a threshold to designate likely true absences.
- Habitat data: CEH Land Cover Map 2015 (LCM2015) with 21 land-cover classes, derived from Landsat-8 and AWIFS classifications; habitats intersected with NBN 100 m grid cells to compute habitat proportions per location.

## Data preparation
- Location processing: Coordinates converted to 100 m grid cells; presence/absence boolean per species created.
- Handling multi-habitat locations: unweighted analysis excludes multi-habitat squares (reducing data); a weighted approach uses habitat proportions to include those locations.
- Absence designation: determined using 14-species threshold (5% of species pool) across 556 potential absence cells; sensitivity analyses performed with other thresholds.
- Data format: transformed into wide format with binary presence indicators for each species per location.

## Measures and methods
- Correlation indices:
  - Unweighted (single-habitat per location) Phi.
  - Weighted Phi (accounts for habitat proportions within locations with multiple habitats).
  - Group-equalised variants (to control for differing habitat frequencies across species/habitats).
- Calculation details:
  - Equations provided for weighted and group-equalised indices.
  - p-values obtained via permutation tests (De Cáceres & Legendre, 2009).
- Output variants and thresholds:
  - Unweighted07, Unweighted14, Unweighted28
  - Weighted07, Weighted28
  - Absence threshold and weighting strategies explained in accompanying sections (2.1, 2.1. and 2.2.1).

## Data quality and thresholds
- Confidence in associations recommended for species with 50 or more presence records used in the analysis.
- Thresholds help users evaluate robustness of habitat associations; multiple versions enable cross-checking of results.

## Outputs and reproducibility
- Recommended output file: carabidae_habitat_associations_weighted14.csv (habitat-weighted analysis with 14-species absence threshold).
- Additional outputs available: carabidae_habitat_associations_unweighted07.csv, carabidae_habitat_associations_unweighted14.csv, carabidae_habitat_associations_unweighted28.csv, carabidae_habitat_associations_weighted07.csv, carabidae_habitat_associations_weighted28.csv.
- Analytical tools:
  - R package PhiCor (for replicating weighting methods) available at GitHub.
  - Analyses performed on the JASMIN computing cluster; permits permutation testing and handling large datasets.

## Implications for monitoring frameworks
- Provides a replicable, data-driven approach to identify habitat associations that can inform conservation prioritization, corridor design, and landscape planning.
- Highlights the value of weighting approaches to make use of locations with multiple habitats and varying survey effort.
- Supports transparent reporting of data sources, processing steps, and uncertainty (through p-values and multiple index variants).

## Practical challenges and considerations for policymakers
- Data limitations: incomplete absence data in NBN; potential data gaps and metadata quality issues; need for timely access and data updates.
- Data governance: publicly sharing underlying data can be a barrier; robust metadata and data management standards essential.
- Silos and interoperability: integrating carabid data with land-cover and other environmental datasets requires governance to avoid duplication and ensure consistency.
- Communication: translating complex habitat association metrics into actionable conservation decisions requires clear visualization and interpretation strategies.

## References and tools for implementation
- PhiCor R package (for replication of weighting methods).
- Foundational methods and related work cited (De Cáceres & Legendre 2009; Chetcuti, Kunin, & Bullock 2019; related ecological and habitat-association literature).
- Datasets: NBN Atlas (carabid records); Land Cover Map 2015 (LCM2015).