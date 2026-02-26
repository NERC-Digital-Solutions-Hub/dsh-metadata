# Details of data structure to ' NW_N2O.csv '

- This document supplements the supporting documentation for data series detailed in 'Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf'.
- Dataset origin: N2O emissions data from a grassland fertiliser trial conducted in 2016 at North Wyke Research Station (Rothamsted Research).
- Data collection method: N2O fluxes measured using manual static chambers.
- Dataset size and scope: 6 columns, 608 rows; contains N2O flux measurements.
- Purpose: Used to understand N2O emissions under different fertiliser applications and treatments.

Dataset structure and contents

- Time: Date & time of N2O sampling
- N_app: 1|2|3 denotes fertiliser application; 1st & 2nd applications of 90 kg N ha-1, 3rd application of 60 kg N ha-1
- Block: 1|2|3|4 blocking factor of a randomised block design
- Plot: Experimental unit
- Treatment: AN|IU|U|C represents N fertiliser type
  - AN = ammonium nitrate (Nitram)
  - U = urea
  - IU = inhibited urea (agrotain)
  - C = 0N Control
- Flux_N2O: N2O flux for each chamber measurement (g N2O-N ha-1 day-1)

Data processing notes

- Flux_N2O values with R2 < 0.6 are considered unreliable and are included with the other data.
- All negative Flux_N2O values are replaced with 0.