# NW_N2O.csv

- Overview
  - Dataset of N2O emissions from a grassland fertiliser trial (2016) at North Wyke Research Station (Rothamsted Research).
  - 6 columns and 608 rows; N2O fluxes measured with manual static chambers.
  - Time column records date and time of sampling.

- Data structure (columns)
  - Time: Date & time of N2O sampling
  - N_app: 1|2|3 indicating fertiliser applications; 1st & 2nd applications at 90 kg N ha-1, 3rd at 60 kg N ha-1
  - Block: 1|2|3|4 blocking factor of randomized block design
  - Plot: Experimental unit
  - Treatment: AN (ammonium nitrate), IU (inhibited urea), U (urea), C (0N Control)
  - Flux_N2O: N2O flux for each chamber measurement, in g N2O-N ha-1 day-1
  - Note: Flux data with R2 < 0.6 and all negative Flux_N2O values replaced with 0

- Data quality and processing
  - Flux measurements filtered to exclude poor fits (R2 < 0.6); negative Flux_N2O values set to 0
  - Data prepared to support aggregation or comparison across plots, blocks, treatments, and application events

- GIS-oriented uses
  - Link Plot and Block identifiers to plot-level GIS geometries to create map-based visualisations
  - Map spatial distribution of treatments (AN, IU, U, C) and succession of N_app events over time
  - Create time-enabled maps or animations of Flux_N2O across sampling dates
  - Combine with other spatial datasets (soil, climate, management) at the plot/block level for integrated analyses

- Context and provenance
  - Part of CINAg experiments documentation; supplement to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
  - Source: North Wyke grassland fertiliser trial, 2016 (N2O flux via static chambers)