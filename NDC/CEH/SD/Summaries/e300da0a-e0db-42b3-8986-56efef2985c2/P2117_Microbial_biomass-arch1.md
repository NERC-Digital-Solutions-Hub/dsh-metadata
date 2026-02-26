# Microbial biomass measurements from an upland grassland liming experiment [NERC Soil Biodiversity Programme] Johnson, D., Leake, J. R., & Read, D. J. University of Sheffield

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (1999): intensive study of a large field experiment at Sourhope, Scottish Borders.
- Aimed to understand soil biodiversity and the functional roles of soil biota in key ecological processes.
- Report focuses on measurements of soil microbial biomass carbon (Cmic), basal respiration, and metabolic quotient (qCO2) in relation to liming and nitrogen fertilization.

## Study site and experimental design
- Location: Sourhope field site, Kelso, Scotland; upland grassland, 500 m above sea level; soil: acid brown earths (pH 4.5–5.0), 40% clay in the 2 mm fraction.
- Vegetation: mixed higher-plant species with extensive arbuscular mycorrhizal fungi (AMF) associations.
- Design: 5 blocks × 4 treatments in a completely randomized layout using 20 turfs per experimental area.
- Treatments: control, lime (CaCO3; 39% Ca; 0.5% ash soluble in HCl; 0.6 kg m^-2), nitrogen (NH4NO3; 12 g m^-2), and lime + nitrogen.
- Turfs (40 cm × 25 cm × 20 cm deep) were relocated from plots to the experimental setup and maintained outdoors; grazing excluded since 1999.

## Measurements and methods
- Microbial activity metrics:
  - Basal respiration: measured in soil cores using a sealed Respicond system; samples incubated at 22°C; respiration logged over 8 hours.
  - Microbial biomass carbon (Cmic): determined by substrate-induced respiration; 10 g soil incubated with glucose (10 mg g^-1 soil dwt) and respiration tracked; Cmic calculated from the maximum rate within the first 4 hours.
  - Metabolic quotient (qCO2): calculated as basal respiration divided by Cmic.
- AMF evaluation: seedlings of Agrostis capillaris L. used to assess AMF colonization and root phosphatase activity in response to perturbations.
- Horizon separation: intact 4 cm cores separated into FH and Ah horizons for analysis.
- Data output: CMIC (mg C g^-1 soil dwt), BASAL (mg CO2 g^-1 soil dwt h^-1), QC02 (mg CO2 g^-1 Cmic h^-1).

## Data output and structure
- Dataset: 1081: Soil microbial biomass 1.0 (CSV)
- Key fields:
  - SAMPID: unique sample identifier
  - SAMPLE_DATE: sampling date
  - BLOCK: block number (1–5)
  - MAIN_PLOT: main plot identifier (A–F)
  - HORIZON: soil horizon (FH, Ah)
  - TREATMENT: applied treatment (control, lime, N, lime + N)
  - CMIC: microbial biomass carbon (mg C g soil dwt^-1)
  - BASAL: basal respiration rate (mg CO2 g soil dwt^-1 h^-1)
  - QC02: metabolic quotient (mg CO2 g Cmic^-1 h^-1)

## Quality control and data provenance
- Quality control: numeric range checks, formatting checks, and logical integrity checks performed.
- Limitations: data are subject to quality assurance procedures but no guarantee of accuracy or fitness for a particular use; liability disclaimer applies.
- Provenance: part of Project 2117, “The effect of mycorrhizal mycelium on the diversity, biomass and functioning of soil microbial communities and its role in carbon and nutrient cycles”; references include foundational methods and the Sourhope field data handbook.