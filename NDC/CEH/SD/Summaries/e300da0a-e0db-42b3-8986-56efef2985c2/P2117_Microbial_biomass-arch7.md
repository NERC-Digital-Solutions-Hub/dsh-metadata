# Microbial biomass measurements from an upland grassland liming experiment [NERC Soil Biodiversity Programme]

## Context and Aim
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focusing on soil biota diversity and functional roles.
- Study location: Sourhope field site, Scottish Borders (grid reference NT8545019630), upland grassland at ~500 m a.s.l.
- Objective: measure soil microbial biomass, basal respiration, and metabolic quotient to understand microbial responses to liming and nitrogen treatments.

## Study Site and Experimental Design
- Materials: turfs (40 cm x 25 cm x 20 cm) removed from the Sourhope upland grassland.
- Experimental design: 5 blocks x 4 treatments (control, lime, N, lime + N) in a completely randomised layout; 20 turfs selected per site.
- Treatments: lime CaCO3 (0.6 kg m^-2) and NH4NO3 (12 g m^-2) applied annually; plots fenced and ungrazed since 1999.
- Soil and vegetation context: acid brown earths (pH 4.5–5.0) with about 40% clay in the 2 mm fraction; plant community includes 24 higher-plant species, many AM-mycorrhizal.

## Measurements and Key Variables
- Horizons sampled: FH and Ah.
- Measurements:
  - Soil microbial biomass carbon (Cmic) via substrate-induced respiration (SIR) after glucose addition.
  - Basal respiration rate (BASAL) from sealed core incubations.
  - Metabolic quotient (qCO2) calculated as basal respiration divided by Cmic.
- Methodology: Respicond automated respirometer; 10 g soil subsamples incubated at 22°C; SIR monitored to derive Cmic; Cmic used to compute qCO2.
- Reference materials and methods cited include foundational SIR and qCO2 methodologies.

## Data Format and Access (File 1081)
- File: P2117_SOIL_MICROBIAL_BIOMASS_1.csv (Soil microbial biomass 1.0).
- Key fields:
  - SAMPID (unique sample identifier)
  - SAMPLE_DATE (date of sampling)
  - BLOCK (block number, 1–5)
  - MAIN_PLOT (main plot letter A–F)
  - HORIZON (FH or Ah)
  - TREATMENT (plot treatment)
  - CMIC (soil microbial biomass carbon, mg C g soil dwt^-1)
  - BASAL (soil basal respiration, mg CO2 g soil dwt^-1 h^-1)
  - QC02 (metabolic quotient, mg CO2 g Cmic^-1 h^-1)
- Context: part of the broader dataset associated with the Sourhope field data handbook (2003) and related NERC publications.

## Geospatial Relevance for GIS
- Precise field location and grid reference enable spatial mapping of microbial biomass and respiration by horizon and treatment.
- Data structured by block, plot, horizon, and treatment suitable for map-based visualization and spatial analysis alongside other soil biodiversity datasets.
- Site-scale context (upland Sourhope, elevation, soil type) supports integration with environmental layers (pH, soil texture, lime application history).

## Data Quality and Usage Notes
- Quality control procedures include numeric range checks, formatting conformity, and logical integrity checks.
- NERC provides no warranty on data accuracy or fitness for a specific use and disclaims liability for outcomes from data use.
- When integrating with GIS analyses, harmonize units and align horizons and plots with any accompanying datasets (e.g., 2003 Sourhope Field Data Handbook).

## References and Related Materials
- Johnson, D., Leake, J. R., & Read, D. J. (2005). Liming and nitrogen fertilization affects phosphatase activities, microbial biomass and mycorrhizal colonisation in upland grassland. Plant and Soil, 271(1-2), 157-164.
- Anderson J.P.E. & Domsch K.H. (1978); Anderson T.-H. & Domsch K.H. (1993) on microbial biomass measurement and qCO2.
- Scott, R., Bell, J., Kenny, C., Jeffers, J., Buckland, S., & Burt-Smith, G. (2003). SOURHOPE FIELD DATA HANDBOOK 2003.
- Usher, M. B., Sier, A. R., Hornung, M., & Millard, P. (2006). Understanding biological diversity in soil: the UK's Soil Biodiversity Research Programme. Applied Soil Ecology.