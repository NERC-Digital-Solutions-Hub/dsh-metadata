# Data for a study looking at the persistence of wet wipes in beach sand and the survival of E. coli on their surfaces

## Overview
- Mesocosm study conducted at the University of Stirling between May and August 2023.
- Aim: examine persistence of wet wipes in beach sand and survival of E. coli on wipe surfaces.
- Part of UKRI NERC-funded projects: "Microbial hitchhikers of marine plastics" and SPACES (grant numbers NE/S005196/1 and NE/V005847/1).

## Study design and setting
- Three commercial wet wipe brands representing different compostability categories:
  - A: non-compostable (contains plastic)
  - B: home compostable
  - C: commercially compostable
- Simulated journey from bathroom to beach: flushed down toilet → WWTP discharge → seawater → beach sand.
- Experimental conditions:
  - Wipes cut to 7 × 7 cm squares
  - Inoculated with E. coli (initial and additional inocula described)
  - Sequential incubation steps in water and WWTP effluent, then seawater
  - Beach sand mesocosms constructed from drainpipes (11 cm circumference, 30 cm long) filled with sand to 10 cm depth; covered with hessian and sand to limit washout.

## Data collection and timepoints
- Weekly sampling over 15 weeks.
- For each wipe type, four replicates per week sampled.
- E. coli quantified by:
  - Vortexing in PBS, vacuum filtration through 0.45 μm membranes
  - Membranes cultured on selective MLGA media; CFUs counted after 24 h at 37 °C
- Tensile strength of wipes measured weekly using a 50 N digital force meter after drying.

## Data types and contents
- Five CSV files (section 8 provides full description):
  1) Dry_weight_sand_used_in_wet_wipes_mesocosm.csv
     - Data on dry sand weight used for mesocosms
  2) Background_bacterial_concentrations_in_wet_wipes_mesocosm.csv
     - Background bacterial concentrations used in mesocosms
  3) Water_characteristics_used_in_wet_wipes_mesocosm.csv
     - Water characteristics of water types used
  4) Tensile_strength_of_wet_wipes_in_wet_wipes_mesocosm.csv
     - Tensile strength of wipes; sampled weekly
  5) Bacterial_concentrations_in_wet_wipes_mesocosm.csv
     - Bacterial concentrations of E. coli on wipes; sampled weekly
- Common structure:
  - Replicate (Rep), Week/Timepoint, Date
  - Wipe_type, Timepoint, Rep
  - For physical data: Tensile Strength (N)
  - For bacterial data: CFU per ml, CFU per wipe, Dilution (where applicable)
  - Water_type, pH, Salinity (for water-related data)
  - Additional measurements include sand weights (start/end), moisture-related differences, and percentage change

## Data quality and completeness
- Data checked for anomalous values and bounded outliers.
- No missing data reported in the dataset.

## Data management and authorship
- Responsible data collection and interpretation: Rebecca Metcalf.

## Purpose and provenance
- Primary purpose: assess whether sewage-associated plastic waste can act as reservoirs for faecal bacteria, potential human pathogens, and antimicrobial resistance genes.
- Aligns with grant requirements for the NERC-funded projects listed above.
- Data originate from a controlled mesocosm study at the University of Stirling (May–August 2023).

## Access and usage notes
- The dataset comprises five CSV files with standardized replicates and detailed variable descriptions.
- A full metadata description is provided in section 8 of the dataset documentation.
- Suitable for environmental health and policy monitoring analyses, including comparisons across wipe types, persistence over time, and correlations between physical/chemical conditions and bacterial concentrations.