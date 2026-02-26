# Fluxes of carbon dioxide, nitrous oxide and methane from winter wheat treated with organic and inorganic fertilisers

## Overview of the dataset
- 2-hourly observations of biogenic fluxes of CO2, N2O, and CH4 from a winter wheat crop on mineral soil in the UK.
- Treatments: (i) inorganic fertiliser; (ii) pig slurry with inorganic fertiliser; (iii) pig slurry treated with plasma-induction with inorganic fertiliser.
- Monitoring period: 83 days during the winter wheat growing season (20/03/2022–13/06/2022) using automated GHG flux chambers.
- Data file: GHG_chamber_flux_data.csv with 2-hourly flux measurements.

## Study site and experimental design
- Location: University of Leeds Research Farm (temperate oceanic climate).
- Field history: continuous arable rotation since 1970.
- Soil: loamy calcareous brown earth, pH 6.9, bulk density 1.3 g cm-3; 0–30 cm soil carbon 39.5 g kg-1 and nitrogen 2.3 g kg-1.
- Climate context: mean annual temperature 9.5°C, mean annual precipitation 885 mm.
- Crop management: winter wheat planted 21/10/2021 at 440 seeds m-2; harvested 27/07/2022; no irrigation.
- Fertiliser treatments (3 replicates each): IF, PS+IF, TPS+IF; all received 220–253 kg available N ha-1.

## Collection methods and fieldwork instrumentation
- Measurements taken every 2 hours from 20/03/2022 to 13/06/2022.
- Instruments: Eosense eosAC-LT chambers and Picarro G2508 analyser.

## Data processing
- Fluxes calculated offline with eos-AnalyzeMX/AC V3.5.0.
- Method: linear fit to raw CO2 concentration; fluxes for CO2, N2O, and CH4 derived from fit.

## Quality control
- Outliers identified/removed using a modified Elbers et al. (2011) approach.
- Uncertainty quantified for CO2 fluxes via threshold u*, statistical screening, measurement errors, and flux calculation uncertainties.

## Gap-filling
- N2O and CH4: gap-filled by linear interpolation.
- CO2: gap-filled by linear regression, with separate gap-filling for daytime and night-time data.

## Details of data structure
- File: GHG_chamber_flux_data.csv
- Columns (described):
  - Date_Time: date and start time of the 2-hour measurement (GMT), format dd/mm/yyyy HH:MM.
  - Chamber_Number: identifier for the chamber used.
  - CO2: gap-filled CO2 exchange flux (μmol CO2 m-2 s-1).
  - N2O: gap-filled N2O exchange flux (nmol N2O m-2 s-1).
  - CH4: gap-filled CH4 exchange flux (nmol CH4 m-2 s-1).
  - Gap_Fill: indicator (1 = observed, 2 = gap-filled).
  - Treatment: fertiliser treatment (IF = inorganic fertiliser, PS = pig slurry + inorganic fertiliser, TPS = treated pig slurry + inorganic fertiliser).

## Acknowledgements
- Funded by Leeds-York-Hull Natural Environmental Research Council (NERC) DTP Panorama (grant NE/S007458/1).
- Acknowledges University of Leeds Research Farm and individuals for assistance with materials, fieldwork, farm management information, and fertiliser guidance.

## References
- Methodological and contextual references related to greenhouse gas flux measurement, gap-filling, and data processing are provided for further detail and replication.