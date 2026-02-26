# Morphology phenotype data of 88 types of galls induced on oak trees by cynipid gallwasps from 6 sites in Hungary, 2000-2003: Supporting information

## Overview
- Dataset of quantitative and categorical phenotypic attributes for galls induced on Quercus spp. by cynipid gallwasps (Cynipidae: Cynipini).
- Galls collected from 6 sites in Hungary (2000–2003); mature galls assessed for internal and external structure.
- Separate scores for each sexual and asexual generation; totals: 31 sexual generation galls and 58 asexual generation galls across 69 cynipid species.
- Sampling: continuous measurements taken on samples of 10 galls per gall type across sites 1–5; continuous variables in mm or mm^3.

## Data collection and scope
- Phenotypic properties capture internal/external structure of mature galls.
- Data include binary, ordinal, and continuous variables.
- Data capture includes both sexual and asexual generations for each species where applicable.
- Units: continuous measurements in millimeters (mm) or cubic millimeters (mm^3).

## Data structure and variables
- 17 data columns, one row per cynipid species and generation, for the mature gall:
  1. Linnean species name
  2. Generation (Asexual or Sexual)
  3. Hair (binary: 1 = hairy, 0 = not)
  4. Dense_spines (binary)
  5. Sparse_spines (binary)
  6. Sticky (binary)
  7. Space (binary)
  8. Dummy (binary)
  9. Peduncle (binary)
  10. Nectar (binary)
  11. Dehisce (binary)
  12. Tough (ordinal, 1–4; higher = harder)
  13. Shape (cone, cylinder, sphere)
  14. Radius (mm)
  15. Height (mm) – not applicable to spherical galls
  16. Gall_Size (mm^3)
  17. Locularity (Unilocular or Multilocular)
- Missing data markers: -999 used for certain species/generations with no data.
- Note: Height not provided for spherical galls.

## Measurements and units
- Continuous variables: Radius (mm), Height (mm), Gall_Size (mm^3).
- Categorical/ordinal variables: Hair, Dense_spines, Sparse_spines, Sticky, Space, Dummy, Peduncle, Nectar, Dehisce, Tough (1–4), Shape, Locularity.
- All continuous measurements are linked to the mature gall being scored.

## Quality control and data validation
- Categorical variables: designed to be unambiguous for mature galls.
- Gall maturity confirmed by presence of fully mature larval/pupal gall in larval chambers.
- Toughness (Tough) validated with continuous penetration scores using a QTS-25 texture analyser (data not shown).
- Species identifications based on diagnostic external gall features by experienced field staff; where needed, confirmation via DNA barcoding (partial sequences of mitochondrial cytochrome b and nuclear ITS2).
- Data thoroughly checked for errors.

## Data limitations and notes
- Some Tough values are missing across certain gall types.
- Height missing for spherical galls; uses -999 placeholders where data are absent.
- Data availability includes a map of six sites (map not provided in the text).

## References
- Bailey, R. et al. (2009). Host niches and defensive extended phenotypes structure parasitoid wasp communities. PLoS Biology.
- Nicholls, J. A. et al. (2012). Mitochondrial barcodes are diagnostic of shared refugia but not species in hybridising oak gallwasps. Molecular Ecology.
- Roskam, J. C. (2019). Plant Galls of Europe.