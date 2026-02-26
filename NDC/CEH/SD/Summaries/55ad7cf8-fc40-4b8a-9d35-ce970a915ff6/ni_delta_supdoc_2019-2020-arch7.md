# Monthly atmospheric ammonia, acid gas, inorganic aerosols and base cation concentrations from Northern Ireland DELTA gas and aerosol monitoring network, 2019-2020

## Overview
- Two CSV files compiling monthly atmospheric concentrations for 2019 and 2020 from four Northern Ireland DELTA gas and aerosol monitoring sites.
- Measured species: gases - ammonia (NH3), nitric acid (HNO3), sulfur dioxide (SO2); aerosols - ammonium (NH4+), nitrate (NO3−), sulfate (SO4^2−), chloride (Cl−), sodium (Na+), calcium (Ca^2+), magnesium (Mg^2+).
- Jointly operated by AFBI and UKCEH; funded by DAERA.
- Purpose: expand spatial coverage, study spatial/ seasonal trends, relate NH3 with acid gases and inorganic aerosol composition, test atmospheric transport models, and estimate nitrogen/sulfur budgets for Northern Ireland.
- Data suitable for GIS use: site locations, monthly concentrations, unit in µg m−3, and quality flags.

## Monitoring network and sites
- Four sites across NI: Hillsborough (AFBI25), Ballynahone (AFBI26), Coleraine (UoU Coleraine) (AFBI27), Sandholes (AFBI28).
- Start dates in 2019; coordinates provided to two decimals for confidentiality; inlet height 1.5 m.
- Rationale: increase spatial coverage and enable assessment of spatial variability and seasonal trends; concurrent gas and aerosol measurements support interpretation of relationships among components.

## UKCEH DELTA method
- DELTA® diffusion denuder system for long-term monitoring of NH3, HNO3, SO2 and related aerosols.
- Sampling: low-volume flow (0.2–0.4 L/min); monthly exposure cycles; gas meter readings used to convert to concentrations.
- Sample train and analysis: denuders and aerosol filters extracted and analyzed by IC, SEAL-AA3, and ICP-OES.
- Species captured and analysis:
  - Gases: NH3, HNO3, SO2 (HONO captured but not reported)
  - Aerosols: NH4+, NO3−, SO4^2−, Cl−, Na+, Ca^2+, Mg^2+ (with some NO3− and Cl− captured on separate filter fractions)
- Typical detection limits (per month exposure) provided for each ion/species.

## Data structure and units
- Concentrations are time-integrated monthly averages expressed in µg m−3.
- Dataset fields include site_id, site_name, network_id (AFBI), parameter_id, measurement_start/end dates and times, measurement value, unit, flags, verification status, and month/year.
- Parameter_id encodes gas vs. aerosol species and analytical method; outputs stored in the AAGA database and ratified in standardized templates with time-stamped versioning.

## Quality control and data flags
- Three-stage quality control:
  - Stage 1: automated checks and EBAS/EMEP-style flags (auto-flagging, handling of missing periods, flow rate checks, etc.).
  - Stage 2: manual review (laboratory blanks, ion balance, sampling malfunctions, missing/inconsistent data, outliers).
  - Stage 3: expert review by air quality scientists considering sites, trends, inter-site comparisons, and gas–aerosol relationships.
- Data flags drawn from EBAS/EMEP, grouped into missing, unknown, mechanical/instrumental, chemical, extreme/inconsistent values, and aggregated-dataset flags.
- Ratified data are produced as time-stamped, version-controlled outputs; missing or invalid data flagged accordingly (e.g., -9999).

## Relevance for GIS and spatial analyses
- Provides geolocated, monthly, multi-species atmospheric composition data across NI suitable for mapping and spatial trend analyses.
- Enables correlation of NH3 with acid gases and inorganic aerosols, and assessment of transport and source-receptor relationships.
- Confidentiality of coordinates at two decimal places should be considered in mapping at fine scales; dataset supports regional to sub-regional GIS analyses.

## Notes and references
- COVID-19 impacted sampling in 2020 (some sampling periods extended).
- References and resources include EN 17346 method, AGANet/NAMN networks, and EBAS flag documentation.
- Resource locators for network information and EBAS flags included in the original document.