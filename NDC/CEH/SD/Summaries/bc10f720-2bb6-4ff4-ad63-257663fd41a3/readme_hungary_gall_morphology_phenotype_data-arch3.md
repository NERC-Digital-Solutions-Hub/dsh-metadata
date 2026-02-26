# Morphology phenotype data of 88 types of galls induced on oak trees by cynipid gallwasps from 6 sites in Hungary, 2000-2003: Supporting information

## Overview
- Quantitative and categorical phenotype data for 88 gall types induced on Quercus spp. by cynipid gallwasps (Cynipidae: Cynipini).
- Data collected from 6 sites in Hungary between 2000 and 2003, with separate scoring for sexual and asexual generations.
- Dataset includes 31 sexual-generation galls and 58 asexual-generation galls across 69 cynipid species.

## Data collection and scope
- Mature galls were collected and measured; samples include 10 galls per gall type.
- Measurements captured across sites 1–5 with continuous variables measured using digital calipers.
- For some attributes, additional validation included texture analysis for variability in hardness.
- Species identifications based on diagnostic external gall features by experienced field staff; DNA barcoding used in some cases for confirmation (mitochondrial cytochrome b and ITS2).

## Data structure and variables
- 17 data columns per record, each corresponding to a phenotype attribute of the mature gall.
- Data types included: categorical, ordinal, and continuous; all continuous values in mm or mm^3.
- Variables (key examples):
  - Linnean species name
  - Generation (Asexual or Sexual)
  - Hair (binary: 1 = hairy, 0 = not)
  - Dense_spines (binary)
  - Sparse_spines (binary)
  - Sticky (binary)
  - Space (binary)
  - Dummy (binary)
  - Peduncle (binary)
  - Nectar (binary)
  - Dehisce (binary)
  - Tough (ordinal, 1–4)
  - Shape (cone, cylinder, sphere)
  - Radius (continuous, mm)
  - Height (continuous, mm; not applicable to spherical galls)
  - Gall_Size (continuous, mm^3)
  - Locularity (categorical: Unilocular or Multilocular)
- Data gaps are indicated with -999 for missing values; some generations/types lack data for certain variables.

## Quality control and data verification
- Gall maturity confirmed by presence of fully mature larvae/pupae in larval chambers.
- Rich metadata and variable definitions provided to support reproducibility.
- Categorical scores are straightforward; ordinal scores validated with supplementary continuous measurements (e.g., texture data).
- Gall identifications verified with diagnostic features; molecular barcoding used where necessary.
- Data have been carefully checked for errors and consistency across records.

## Data accessibility and governance considerations for monitoring frameworks
- Demonstrates a structured data schema that integrates categorical, ordinal, and continuous measurements across multiple sites and generations.
- Highlights the importance of:
  - Clear metadata and variable definitions to ensure interpretability and comparability.
  - Provenance and validation steps (field identifications, molecular confirmation) for data reliability.
  - Handling missing data with explicit codes (-999) to support downstream analyses.
  - Metadata sharing and data governance to promote openness while maintaining data quality.
- Relevant for monitoring frameworks aiming to establish standardized environmental health indicators, cross-site data aggregation, and transparent data sharing while ensuring data quality and traceability.

## References
- Bailey, R., Schönrogge, K., Cook, J. M., Melika, G., Csóka, Gy., Thúróczy, Cs., & Stone, G. N. (2009). Host niches and defensive extended phenotypes structure parasitoid wasp communities. PLoS Biology, 7(8): e1000179.
- Nicholls, J. A., Challis, R. J., Mutun, S., & Stone G. N. (2012). Mitochondrial barcodes are diagnostic of shared refugia but not species in hybridising oak gallwasps. Molecular Ecology, 21, 4051-4062.
- Roskam, J. C. (2019). Plant Galls of Europe (KNNV Uitgeverij, Amsterdam), 2201 pp.