# Details of data structure to ' HF_soil_minN.csv '

## Overview
- Supplement to the supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Dataset comprises 11 columns and 608 rows
- Contains soil NH4-N and NO3-N + NO2-N concentrations, soil moisture contents, soil pH, and soil electrical conductivity (EC)
- Data stem from a grassland fertiliser trial conducted in 2016 at Henfaes Research Station ( Bangor University)
- Structured to support standardized environmental monitoring and cross-dataset comparability

## Dataset structure and columns
- Date: sampling date
- N_app: fertiliser application index (1|2|3) where 1st & 2nd applications are 90 kg ha-1 and 3rd application is 60 kg ha-1
- Block: blocking factor of the randomized block design (1–4)
- Plot: plot identifier (1–16)
- Treatment: fertiliser type (AN|U|IU|C)
  - AN = ammonium nitrate
  - U = urea
  - IU = inhibited urea (agrotain)
  - C = 0N control
- Soil_NH4_mgNkg: ammonium concentration in soil (mg NH4-N kg-1) on a dry weight basis
- Soil_NO3_mgNkg: nitrate concentration in soil (mg NO3-N kg-1) on a dry weight basis
- moisture_dry: soil moisture on a dry weight basis (g H2O g dry soil-1)
- moisture_wet: soil moisture on a wet weight basis (g H2O g wet soil-1)
- pH: soil pH
- EC: soil electrical conductivity (µS cm-1)

## Sampling design and measurement methods
- Soil sample depth: 0–10 cm, collected with a 1 cm diameter corer
- Per plot: 6 samples were collected and bulked
- Extraction: 5 g soil extracted with 25 ml 0.5 M K2SO4, shaken 30 min at 200 rpm
- N measurements: nitrate via colorimetric method (Miranda et al., 2001); ammonium via method (Mulvaney, 1996)
- Moisture determination: dried for 24 hours at 105°C
- pH and EC: measured with standard electrodes using a 1:2.5 soil-to-deionised water suspension

## Context and purpose
- Part of a 2016 grassland fertiliser trial evaluating nitrogen dynamics under different fertiliser types and application rates
- Data structured to enable integration with other monitoring datasets and to support policy-relevant environmental assessments

## Data quality and stewardship (implied)
- Based on established sampling, extraction, and analytical protocols with explicit units and methods
- Designed for clarity and standardisation to facilitate verification, reuse, and potential upload to appropriate data portals or repositories