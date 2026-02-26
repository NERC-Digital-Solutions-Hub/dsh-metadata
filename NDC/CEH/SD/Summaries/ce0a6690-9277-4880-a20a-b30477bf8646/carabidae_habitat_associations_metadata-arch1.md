# Habitat associations of ground beetles in Great Britain (phi coefficient of association)

## Overview
- Study of habitat associations for ground beetles (Carabidae) in Great Britain using the phi coefficient of association.
- Data sources: 100 m carabid location records from the NBN Atlas (2017) and CEH Land Cover Map 2015 (LCM2015).
- Outputs include habitat-associated scores (R, pR, Rg, pRG) for each species-habitat combination, with both weighted and unweighted versions and various presence thresholds.

## Data sources and scope
- Carabid data (NBN Atlas): presence records across Britain at 100 m resolution; initial filtering to species with at least 10 records (268 species).
- Land cover (LCM2015): 21 habitat classes aligned to UK Biodiversity Action Plan Broad Habitats.
- Purpose: infer habitat requirements, inform landscape-scale conservation planning, and assess impact of habitat changes.

## Data preparation and handling of absences
- Location construction: coordinates aggregated to 100 m grid cells; species names reconciled against NHM UK inventories and Luff (2007).
- Absence handling: NBN lacks true absence data; absence inferred using survey effort proxy (presence of other carabid species in a location).
  - Threshold chosen: 14 other species (5% of species pool) to define “true absence” locations, yielding about 556 potential absence grid cells.
  - Absence locations for a species are the remainder after excluding cells where the species is present.
- Habitat composition per location: intersect LCM2015 with 100 m squares; compute proportion of each habitat within each location.

## Correlation indices and methodological choices
- Unweighted analysis:DISCARD or select a single habitat per location when multiple habitats occur; discarding multi-habitat squares reduces data substantially.
- Weighted analysis: assign weights to habitats within multi-habitat locations to utilize more data; weighting is proportional to habitat proportion within the location.
  - Weighted phi (Φw) formula adjusts for habitat proportions; example provided to illustrate calculation.
- Group-equalised analysis: φg^w (group-equalised, weighted) to control for differences among habitat groups.
- Both original and uncertainty-weighted versions are computed; significance assessed via permutation tests (De Cáceres & Legendre, 2009).
- Confidence threshold: consider species reliable only if they have 50+ presence records in the analysis.

## Outputs and tools
- Recommended output: carabidae_habitat_associations_weighted14.csv (weighted analysis with 14-species absence threshold).
- Additional files for sensitivity and verification: 
  - carabidae_habitat_associations_unweighted07.csv
  - carabidae_habitat_associations_unweighted14.csv
  - carabidae_habitat_associations_unweighted28.csv
  - carabidae_habitat_associations_weighted07.csv
  - carabidae_habitat_associations_weighted28.csv
- Reproducibility and further analysis:
  - R package PhiCor (Chetcuti, 2018) for computing habitat associations; available at GitHub: https://github.com/Zabados/PhiCor
  - Related publication: A weighting method to improve habitat association analysis: tested on British carabids (Chetcuti et al., 2019)
- Computational workflow:
  - Data pre-processing and wide-format conversion performed with an R script.
  - Analyses and permutations run on the JASMIN computing cluster.

## Data fields and interpretation
- Habitats: 1–21 indicating the 21 LCM2015 habitat classes.
- R: non-group-equalised habitat association score (−1 to +1).
- pR: p-value for R (significance of non-group-equalised association).
- Rg: group-equalised habitat association score (−1 to +1).
- pRG: p-value for Rg (significance of group-equalised association).
- species: taxon name (aligned with NHM UK checklist or Luff 2007).
- AbsenceCut: threshold used to define absence locations.
- n: total number of presence locations used in the analysis.
- N: total number of locations (presence + absence) used in the analysis.
- Np w, np w: weighted totals used in the weighted correlation calculation.
- N p g, n g w: group-based equivalents for the group-equalised weighting.
- Table 2 (example input data) illustrates habitat proportions per location and binary presence for species.

## Analyses workflow and outputs
- Data processing: convert multi-record locations to a single presence/absence per species per location; create wide-format dataset for analysis.
- Analysis: compute original and weighted phi values; perform permutation tests to derive p-values.
- Output: multiple CSVs enabling comparison across thresholds (7, 14, 28) and weighting schemes (weighted vs unweighted); recommended weighting with 14-species absence threshold for robust inferences.

## Context and references
- Data sources and methodology draw on established ecological and statistical methods for habitat association analyses and presence-absence data handling.
- Key references include PhiCor package (Chetcuti, 2018), weighting methods for habitat association (Chetcuti et al., 2019), permutation-based inference (De Cáceres & Legendre, 2009), and supporting data/products (NBN Atlas, Rowland et al. 2015/2017; LCU/AWIFS Landsat-8 data; related ecological literature).