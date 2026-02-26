# Fluxes of carbon dioxide, nitrous oxide and methane from winter wheat treated with organic and inorganic fertilisers

## Purpose and scope
- Provides 2-hourly observations of biogenic fluxes of CO2, N2O, and CH4 from a winter wheat crop on mineral soil under three fertiliser regimes.
- Time span: 83 days during the winter wheat growing season (20/03/2022–13/06/2022).
- Treatments: i) inorganic fertiliser; ii) pig slurry + inorganic fertiliser; iii) pig slurry with plasma-induction + inorganic fertiliser.
- Automated flux chambers used to quantify greenhouse gas fluxes.

## Study site and experimental design
- Location: University of Leeds Research Farm, field with long-term arable rotation (since 1970).
- Climate: temperate oceanic.
- Soil: loamy, calcareous brown earth, pH 6.9, bulk density 1.3 g cm-3; 0–30 cm soil C 39.5 g/kg and N 2.3 g/kg.
- Management: rainfed field; winter wheat planted 21/10/2021 (density ~440 seeds m-2) and harvested 27/07/2022.
- Experimental setup: three fertiliser treatments with three replicates each; all received 220–253 kg available N ha-1.

## Collection methods and field instrumentation
- Flux measurements every 2 hours using Eosense eosAC-LT chambers and a Picarro G2508 analyser.
- Measurement period: 20/03/2022–13/06/2022.

## Data processing
- Fluxes calculated offline with eos-AnalyzeMX/AC V3.5.0.
- CO2 fluxes derived from a linear fit to raw CO2 concentrations; N2O and CH4 fluxes calculated accordingly.

## Quality control
- Outliers identified and removed using a modified Elbers et al. (2011) approach.
- Uncertainty in CO2 fluxes quantified by considering threshold acceptance (u*), measurement errors, and flux calculation uncertainties.

## Gap-filling
- N2O and CH4: gap-filled by linear interpolation.
- CO2: gap-filled by linear regression, with separate daytime and nighttime gap-filling.

## Data structure and variables
- File: GHG_chamber_flux_data.csv
- Key fields:
  - Date_Time: dd/mm/yyyy HH:MM (GMT) for start of the 2-hour measurement.
  - Chamber_Number: identifier for each chamber measurement.
  - CO2: μmol CO2 m-2 s-1; gap-filled value.
  - N2O: nmol N2O m-2 s-1; gap-filled value.
  - CH4: nmol CH4 m-2 s-1; gap-filled value.
  - Gap_Fill: indicator (1 = observed, 2 = gap-filled).
  - Treatment: IF = inorganic fertiliser; PS = pig slurry + inorganic; TPS = treated pig slurry + inorganic.

## Data accessibility and provenance
- Data collection funded by the Leeds-York-Hull NERC Doctoral Training Partnership (DTP Panorama), grant NE/S007458/1.
- Acknowledgements to the University of Leeds Research Farm and individuals who assisted with materials, fieldwork, and fertiliser management.

## Implications for environmental monitoring and data reuse
- Standardised, time-resolved GHG flux dataset suitable for integration with other environmental datasets.
- Documented data processing, QC, and gap-filling enable robust cross-study comparisons and long-term monitoring.
- Data are prepared for storage and sharing through appropriate portals, supporting broader access to underlying data for policy and research scrutiny.