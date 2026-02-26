# Fluxes of carbon dioxide, nitrous oxide and methane from winter wheat treated with organic and inorganic fertilisers

## Overview
- 2-hourly measurements of biogenic fluxes of CO2, N2O, and CH4 from a winter wheat crop on mineral soil in the UK.
- Experimental treatments: (i) inorganic fertiliser; (ii) pig slurry plus inorganic fertiliser; (iii) pig slurry treated with plasma-induction plus inorganic fertiliser.
- Timeframe: 83 days during the winter wheat growing season (20/03/2022–13/06/2022).
- Sampling method: automated GHG flux chambers.

## Study site and experimental design
- Location: University of Leeds Research Farm (field in continuous arable rotation since 1970).
- Climate: temperate oceanic; mean annual temperature ~9.5°C; mean annual rainfall ~885 mm.
- Soil: well-drained loamy calcareous brown earth; pH ~6.9; bulk density ~1.3 g cm-3; soil carbon ~39.5 g kg-1 and nitrogen ~2.3 g kg-1 (0–30 cm).
- Field setup: rainfed with no irrigation; winter wheat planted 21/10/2021 at 440 seeds m-2; harvested 27/07/2022.
- Treatments: IF, PS + IF, TPS + IF with three replicates each.

## Collection methods and fieldwork instrumentation
- Flux measurements every 2 hours from 20/03/2022 to 13/06/2022.
- Equipment: Eosense eosAC-LT flux chambers and Picarro G2508 analyser.

## Data processing
- Flux calculations performed offline with eos-AnalyzeMX/AC V3.5.0.
- CO2 flux calculated via linear fit to chamber concentration data; N2O and CH4 fluxes computed accordingly.
- References informing methods: Petrakis et al. (2018); Barba et al. (2019).

## Quality control
- Outliers identified and removed using a modified Elbers et al. (2011) approach.
- Uncertainty for CO2 fluxes quantified using threshold detection value (u*) and other error sources (measurement and flux calculation).

## Gap-filling
- N2O and CH4: missing values filled by linear interpolation.
- CO2: gap-filled by linear regression; separate gap-filling for daytime and nighttime data.

## Details of data structure
- File: GHG_chamber_flux_data.csv
- Columns:
  - Date_Time (dd/mm/yyyy HH:MM, GMT): start of the 2-hour measurement
  - Chamber_Number: identifier for the chamber
  - CO2 (μmol CO2 m-2 s-1): gap-filled CO2 exchange flux
  - N2O (nmol N2O m-2 s-1): gap-filled N2O exchange flux
  - CH4 (nmol CH4 m-2 s-1): gap-filled CH4 exchange flux
  - Gap_Fill: indicator if data is observed (1) or gap-filled (2)
  - Treatment: fertiliser treatment (IF = inorganic fertiliser; PS = pig slurry + inorganic fertiliser; TPS = pig slurry + inorganic fertiliser, plasma-induction treated)

## Acknowledgements and references
- Funding: Leeds-York-Hull Natural Environmental Research Council (NERC) DTP Panorama (grant NE/S007458/1).
- Acknowledgements: University of Leeds Research Farm and individuals who assisted with materials, fieldwork, farm management information, and fertiliser guidance.
- Key references related to methods and gap-filling: Elbers et al. (2011); Dorich et al. (2020); Lucas-Moffat et al. (2022); Petrakis et al. (2017); Barba et al. (2019).