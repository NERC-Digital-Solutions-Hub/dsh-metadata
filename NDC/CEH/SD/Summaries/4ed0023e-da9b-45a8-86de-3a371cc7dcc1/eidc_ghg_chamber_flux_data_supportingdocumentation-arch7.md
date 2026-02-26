# Fluxes of carbon dioxide, nitrous oxide and methane from winter wheat treated with organic and inorganic fertilisers

## Overview
- 2-hourly observations of biogenic fluxes of CO2, N2O and CH4 from a winter wheat crop on mineral soil in the UK.
- Fertiliser treatments: i) inorganic fertiliser; ii) pig slurry + inorganic fertiliser; iii) pig slurry treated with plasma-induction + inorganic fertiliser.
- Measurements span 83 days during the winter wheat growing season using automated GHG flux chambers.

## Study site and experimental design
- Location: University of Leeds Research Farm (provided coordinates).
- Field history: continuous arable rotation since 1970; temperate oceanic climate; soil type and baseline properties (pH 6.9; bulk density 1.3 g cm^-3; 0–30 cm carbon 39.5 g kg^-1; nitrogen 2.3 g kg^-1).
- Crop management: winter wheat planted 21/10/2021, harvested 27/07/2022; rainfall-fed (no irrigation).
- Treatments: IF, PS+IF, TPS+IF with three replicates per treatment; all received 220–253 kg available N ha^-1.

## Collection methods and fieldwork instrumentation
- Flux measurements every 2 hours from 20/03/2022 to 13/06/2022.
- Instrumentation: Eosense eosAC-LT chambers and Picarro G2508 analyser.

## Data processing
- Fluxes computed offline with eos-AnalyzeMX/AC V3.5.0 by applying a linear fit to CO2 concentration to derive fluxes for CO2, N2O, and CH4.

## Quality control
- Outliers identified and removed using a modified Elbers et al. (2011) approach.
- Uncertainties for CO2 fluxes quantified from threshold detection value (u*), measurement errors, and flux calculation uncertainties.

## Gap-filling
- N2O and CH4: gap-filled via linear interpolation.
- CO2: gap-filled via linear regression with separate daytime/night-time gap-filling.

## Details of data structure
- File: GHG_chamber_flux_data.csv
- Key columns:
  - Date_Time: dd/mm/yyyy HH:MM (GMT, start of 2-hour measurement)
  - Chamber_Number: chamber ID
  - CO2: μmol CO2 m^-2 s^-1 (gap-filled)
  - N2O: nmol N2O m^-2 s^-1 (gap-filled)
  - CH4: nmol CH4 m^-2 s^-1 (gap-filled)
  - Gap_Fill: 1 = observed, 2 = gap-filled
  - Treatment: IF, PS, TPS
- Descriptions and units provided for each field.

## Acknowledgements
- Funded by Leeds-York-Hull NERC Doctoral Training Partnership (DTP Panorama), grant NE/S007458/1.
- Acknowledges field site support and contributions from named individuals.

## References
- Includes methodological and supporting references for flux measurement, gap-filling, and data processing methods.

## GIS relevance and potential data products
- Spatial and temporal context:
  - Site coordinates and chamber-based sampling units enable spatial mapping of fluxes at field scale.
  - 83-day time series with 2-hour resolution supports fine-grained temporal analyses.
  - Associated soil properties and management practices accompany the flux data for contextual GIS analyses.
- Potential map-based data products:
  - Time-series maps of CO2, N2O, and CH4 fluxes by chamber across the measurement period.
  - Treatment-based comparative maps showing spatial patterns of flux responses to fertiliser regimes.
  - Integrated maps combining flux data with soil properties (pH, carbon, nitrogen) and weather data.
- Data integration and quality considerations:
  - Gap-filled data are flagged, enabling transparent handling in GIS workflows.
  - Quality control steps documented, supporting confidence in spatial visualizations and analyses.
  - Chamber-level data (Chamber_Number) serves as the primary spatial sampling unit for GIS representations.