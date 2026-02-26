# Growing-season eddy covariance measurements of carbon dioxide, energy and water fluxes from a bioenergy maize crop, Yorkshire, UK, 2021

## Overview
- 30-minute observations of land-atmosphere exchanges: net ecosystem CO2 exchange (NEE) and sensible (H) and latent heat (LE) fluxes.
- Measurements cover the growing season of a bioenergy maize crop in Yorkshire, UK, from 02/06/2021 to 10/10/2021.
- Includes accompanying weather and soil physics measurements.
- Data produced using micrometeorological eddy covariance (EC) method with quality control and gap-filling.

## Study Site
- Location: field at the University of Leeds Research Farm (coordinates: 53°51'56.26"N, 1°19'28.22"W).
- Climate: temperate oceanic; mean annual temperature ~9.5°C and ~885 mm annual rainfall (1992–2022).
- Soil: loamy calcareous brown earth, pH ~6.9, bulk density ~1.3 g cm^-3; soil carbon ~39.5 g/kg and nitrogen ~2.3 g/kg in 0–30 cm.
- Agriculture: rainfed, maize planted 02/06/2021 at 110,000 seeds ha^-1; harvested 10/10/2021; single inorganic fertilizer application at planting (22.5 kg N ha^-1).

## Collection Methods and Fieldwork Instrumentation
- Flux measurements: closed-path EC system mounted on an extendable mast; CO2/H2O analyzer LI-7200RS and Gill Windmaster 3D sonic anemometer; data at 10 Hz, aggregated to 30-minute means.
- Ancillary measurements: energy fluxes (Rnet, SWin, SWout, LWin, LWout), air temperature, relative humidity, soil temperature (Tsoil) and soil moisture (5 cm depth).
- Data logged as 30-minute means for all ancillary variables.

## Data Processing
- Fluxes calculated with EddyPro 7 (conditioning, angle-of-attack correction, lag correction, spectral correction).
- High-frequency data corrections applied to ensure data fidelity.
- Random uncertainty estimated following established methods.

## Quality Control
- Performed in R to ensure high-quality data; data removal criteria include:
  - Statistical outliers.
  - LI-COR signal > baseline by more than 10%.
  - Nonrepresentative footprints (>20% data outside site boundaries).
  - Unrealistic flux thresholds (H: 200–450 W m^-2; LE: -50 to 400 W m^-2; NEE: -60 to 30 μmol CO2 m^-2 s^-1).
  - Friction velocity u* < 0.14 m s^-1.

## Gap-filling and Flux Partitioning
- Gap filling and partitioning of NEE conducted with REddyProc (R) using marginal distribution sampling.
- Uncertainty of filled gaps quantified as the standard deviation of observations used for filling.

## Data Structure and Variables
- File: Yorkshire_Bioenergy_Maize_GS_2021.csv
- Key columns and descriptions:
  - Date and Time in GMT; NEE and NEE_unc; LE and LE_unc; H and H_unc; Tau and Tau_unc (momentum flux); CO2_strg, LE_strg, H_strg (storage terms).
  - Pa (barometric pressure); Tair; RH; VPD; SWin/SWin_rev (shortwave radiation); SWout/LWin/LWout; Rnet and PAR; G (soil heat flux).
  - Tsoil and Tsoilunc; VWC at 0–5 cm; windspeed and winddir; Ustar; TKE; Tstar; L and (z-d)/L (stability).
  - NEE_f and NEE_f_sd (gap-filled NEE and its SD); Reco (ecosystem respiration); GPP (gross primary productivity).
- Time stamps: Date in dd/mm/yyyy and GMT; Time in HH:MM:SS (GMT).

## GIS-Relevant Considerations
- The dataset provides detailed point-based flux measurements with a 30-minute temporal resolution, suitable for integration with GIS layers via footprint modeling and site-scale analyses.
- Includes both raw flux estimates and gap-filled/partitioned products, enabling continuous time-series analyses in spatial-temporal workflows.
- Geolocation is explicit for site-level mapping; data can be cross-referenced with soil, climate, and land-management layers.

## Access, Acknowledgments and References
- Funding: Leeds-York-Hull NERC Doctoral Training Partnership (grant NE/S007458/1).
- Acknowledges University of Leeds Research Farm and Rob Yardley for farm-management information.
- References provided for instruments, processing methods, and gap-filling techniques used.