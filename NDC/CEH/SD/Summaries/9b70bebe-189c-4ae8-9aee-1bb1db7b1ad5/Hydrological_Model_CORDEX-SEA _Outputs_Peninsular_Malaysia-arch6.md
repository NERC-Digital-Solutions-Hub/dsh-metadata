Historical (1971-2005) and projected (2006-2099) hydrological model (HMF-Malaysia) estimates of monthly mean and annual maximum river flows across Peninsular Malaysia driven by CORDEX-SEA projected climate data

## Overview
- Provides ensemble hydrological model estimates of monthly mean river flows and annual maximum daily river flows across Peninsular Malaysia on a 0.008333° × 0.008333° grid (~1 km) for historical (1971–2005) and projected future (2006–2099).
- Driven by CORDEX-SEA climate data; outputs include two artificial influence scenarios: current artificial influences (CAI) and planned future artificial influences (FAI).

## Data and what it includes
- Grid-based river flow estimates at ~1 km resolution for:
  - Monthly mean flows (m3 s−1)
  - Annual maximum of daily flows (m3 s−1)
- Coverage: Peninsular Malaysia (domain 1.2°–6.8° N, 99.5°–104.6° E)
- Temporal scope: Historical (1971–2005) and Future (2006–2099)
- Ensemble realizations:
  - 13 historical / 26 future realisations per composition of CORDEX-SEA models and RCPs
  - RCPs: 2.6, 4.5, 8.5 with multiple ensemble members

## Modelling framework
- Hydrological Modelling Framework - Malaysia (HMF-Malaysia): physically based, grid-based, distributed model.
- Configured to account for artificial influences (CAI and FAI) such as water transfers, diversions, and urban areas.
- Typically not calibrated to individual catchments; uses spatial datasets of physical/soil properties to configure hydrology for local conditions.
- Strength: consistent, spatially coherent flows across the national domain, including ungauged locations; limitation: potential lower accuracy at catchment level due to lack of catchment calibration.

## Driving data and climate scenarios
- Forcing data: CORDEX-SEA daily climate model outputs (precipitation, near-surface air temperature, daily max/min temperatures).
- PE (potential evaporation) derived from temperature via Oudin et al. (2005).
- Climate scenarios: 6 × RCP2.6, 7 × RCP4.5, 13 × RCP8.5 ensemble members.
- Time periods: baseline historical (1971–2005) and projections (2006–2099).
- Note: Simulations are driven by climate model realizations, not observed data; baseline flows are not direct observations but climate-reality realizations.

## Format and structure of the data
- Output format: NetCDF files (common for scientific data).
- Spatial resolution: 0.008333° × 0.008333° (~1 km × 1 km).
- Variables provided:
  - Monthly mean river flows (MM)
  - Annual maximum daily river flows (AM)
- Time coverage and calendar:
  - Some ensembles use 365/366-day Gregorian calendar or 360-day calendar; file lengths reflect calendar type.
- Metadata: NetCDF headers include necessary metadata; spatial dimensions = latitude, longitude, time.

## File naming conventions (examples)
- Monthly mean CAI: HMF-PM_MMFLOW_CAI_<model>_<HIST/RCP>_<period>.nc
- Monthly mean FAI: HMF-PM_MMFLOW_FAI_<model>_<RCP>_<period>.nc
- Annual maximum CAI: HMF-PM_AMFLOW_CAI_<model>_<HIST/RCP>_<period>.nc
- Annual maximum FAI: HMF-PM_AMFLOW_FAI_<model>_<RCP>_<period>.nc
- Example (historical CAI for RegCM4-3 with ICHEC-EC-EARTH, RCP8.5): HMF-PM_MMFLOW_CAI_RegCM4-3-ICHEC-EC-EARTH_HIST_197101-200512.nc

## How to use and interpret
- Use the full ensemble to assess range and uncertainty; no single member is deemed most reliable.
- Do not directly compare model-generated flows to observed historical river flows; comparisons should be made within the same CORDEX-SEA model across historical vs. future runs.
- Suitable for identifying spatial patterns and changes in river flows, including ungauged areas, but not for fine catchment-scale calibration.
- Practical considerations:
  - Data are large; online storage is impractical; use aggregated outputs (MM and AM) for analysis.
  - Tools: NetCDF-compatible software (ArcGIS, NCView, Xconv) or programming (Fortran, Python); conversion to ASCII is possible but results in very large files.
- Applications include planning for floods and droughts, state/catchment-level analyses, and flood-frequency analysis using AM flows with generalized extreme value distributions (subject to stationarity assumptions).

## Suggested applications
- Planning for future floods and drought scenarios at state/catchment and national scales.
- Analyzing climate-change impacts on river flows for specific rivers or states under multiple RCPs.
- Investigating extreme flood magnitudes via flood-frequency analyses using annual maximum data (GEV fitting and return period plotting).

## Data sources and access
- CORDEX-SEA driving data: precipitation, near-surface air temperature, daily max/min temperatures; PE derived from temperature.
- CORDEX-SEA data portal: https://cordex.org/domains/region-14south-east-asia-sea/
- Context: Output from the Malaysia-Flood Impacts Across Scales (FIAS) project funded by NERC (UK) and Malaysia’s Ministry of Higher Education.

## Acknowledgements and references
- Acknowledges the Malaysia-FIAS project and associated funders; references include works on the HMF framework, high-resolution river-flow modelling, and climate data sources and methodologies (e.g., Jenkinson 1955; Martens et al. 2017; Oudin et al. 2005; van Vuuren et al. 2011).