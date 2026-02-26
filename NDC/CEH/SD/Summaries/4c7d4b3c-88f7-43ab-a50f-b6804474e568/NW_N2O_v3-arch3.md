# Details of data structure to ' NW_N2O.csv '

## Overview
- Supplement to the supporting documentation for data series detailed in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- NW_N2O.csv contains N2O emissions data: 6 columns, 608 rows
- Data originate from a grassland fertiliser trial conducted in 2016 at North Wyke Research Station (Rothamsted Research)

## Dataset structure and content
- Measurement method: N2O fluxes measured using manual static chambers
- Columns and meaning:
  - Time: Date & time of N2O sampling
  - N_app: 1|2|3 denotes fertiliser application (1st & 2nd applications of 90 kg N ha-1, 3rd application of 60 kg N ha-1)
  - Block: 1|2|3|4 blocking factor of a randomised block design
  - Plot: Experimental unit
  - Treatment: AN|IU|U|C representing N fertiliser type
    - AN = ammonium nitrate (Nitram)
    - U = urea
    - IU = inhibited urea (agrotain)
    - C = 0N Control
  - Flux_N2O: N2O flux for each chamber measurement (g N2O-N ha-1 day-1)
- Data quality refinement:
  - Flux_N2O values with R^2 < 0.6 are treated as unsuitable
  - All negative Flux_N2O values are replaced with 0

## Context and provenance
- Data sourced from the 2016 grassland fertiliser trial at North Wyke Research Station, part of Rothamsted Research
- Purpose of the dataset snippet: to define and communicate the data structure for integration with supporting documentation and subsequent analyses

## Implications for monitoring frameworks
- Clear variable definitions and units support transparency and reproducibility
- The explicit data cleaning rule (R^2 threshold and zeroing negatives) demonstrates an QA step that may affect trend interpretation and requires documentation for auditability
- The structured design (Time, N_app, Block, Plot, Treatment) facilitates stratified analyses across applications, blocks, and treatments, aiding policy-relevant monitoring and evaluation efforts