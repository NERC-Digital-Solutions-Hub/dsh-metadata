# Fluxes of carbon dioxide, nitrous oxide and methane from winter wheat treated with organic and inorganic fertilisers

## Overview
- 2-hourly measurements of biogenic fluxes of CO2, N2O, and CH4 from winter wheat on mineral soil in the UK.
- Three fertiliser treatments with three replicates each: inorganic fertiliser (IF); pig slurry + inorganic fertiliser (PS+IF); pig slurry treated with plasma-induction + inorganic fertiliser (TPS+IF).
- Monitoring period: 83 days within the winter wheat growing season (20/03/2022–13/06/2022) using automated GHG flux chambers.

## Study site and experimental design
- Location: University of Leeds Research Farm field; long-term arable rotation since 1970.
- Climate: temperate oceanic; mean annual temp ~9.5°C, precipitation ~885 mm (1992–2022 data).
- Soil: well-drained loamy calcareous brown earth; pH 6.9; bulk density 1.3 g cm^-3; 0–30 cm soil carbon ~39.5 g kg^-1 and nitrogen ~2.3 g kg^-1.
- Crop and management: winter wheat planted 21/10/2021 at 440 seeds m^-2; harvested 27/07/2022.
- Treatments: IF, PS+IF, TPS+IF; all received 220–253 kg available N ha^-1; each with three replicates.

## Collection methods and fieldwork instrumentation
- Flux measurements every 2 hours from 20/03/2022 to 13/06/2022.
- Instruments: Eosense eosAC-LT chambers and Picarro G2508 gas analyser.

## Data processing
- Flux calculation performed offline with eos-AnalyzeMX/AC V3.5.0.
- CO2 flux derived from linear fit to raw CO2 concentrations; N2O and CH4 fluxes calculated accordingly.

## Quality control
- Outliers removed using a modified Elbers et al. (2011) approach.
- Uncertainty in CO2 fluxes quantified via threshold detection value (u*), measurement errors, and flux calculation uncertainties.

## Gap-filling
- N2O and CH4 gaps filled by linear interpolation.
- CO2 gaps filled by linear regression; daytime and nighttime data gap-filled separately.

## Details of data structure
- File: GHG_chamber_flux_data.csv
- Key columns:
  - Date_Time: start time of 2-hour measurement (dd/mm/yyyy HH:MM, GMT)
  - Chamber_Number: identifier for chamber
  - CO2: gap-filled CO2 exchange flux (μmol CO2 m^-2 s^-1)
  - N2O: gap-filled N2O exchange flux (nmol N2O m^-2 s^-1)
  - CH4: gap-filled CH4 exchange flux (nmol CH4 m^-2 s^-1)
  - Gap_Fill: indicator (1 = observed, 2 = gap-filled)
  - Treatment: fertiliser treatment (IF, PS, TPS)

## Acknowledgements
- Data collection funded by Leeds–York–Hull NERC Doctoral Training Partnership (DTP Panorama), grant NE/S007458/1.
- Recognition of field site access and assistance from named contributors.