Meteorology, soil physics, and eddy covariance measurements of carbon dioxide, energy, and water exchange from a distributed network of sites across England and Wales, 2023 to 2024

## Overview
- Time series dataset of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE), plus supporting meteorological and soil physics data.
- Collected at six eddy covariance (EC) flux tower sites across England and Wales.
- Includes data processing to derive net ecosystem exchange (NEE) and its partitioning into gross primary production (GPP) and ecosystem respiration (Reco); ancillary data and metadata support quality and interpretability.
- Data are prepared for clear reporting and visualization via reports, charts, or dashboards; metadata and data governance are emphasised.

## Study sites
- Six flux monitoring sites with diverse land uses: three croplands (peat and mineral soils), one grassland on peat, one lowland fen under conservation management, and a relatively intact upland raised bog.
- Elevational range from -2 m to 565 m above sea level; mean annual temperatures (MAT) 5–10°C; mean annual precipitation (MAP) 534–1815 mm.
- Site metadata captured in UK-SCAPE_Y6_Site_Metadata.csv, describing descriptions, file names, sampling intervals, land use, soil type, climate, coordinates, measurement heights, and instrument models.

## Sampling regime and flux data acquisition
- Automated, continuous flux, meteorological, and soil physics measurements for each site during the specified START_DATE to END_DATE.
- Fluxes measured above the canopy with open-path EC systems using:
  - Sonic anemometer (wind components, sonic temperature) and LI-7500 IRGA (CO2 and water vapour densities).
  - Sampling at 20 Hz; data logged on a CR3000 Micrologger and telemetered to a secure server.
- Observations include height-specific configurations and instrument separations; measurement heights (Zm) fixed at most sites, with adjustments for maize production in croplands.

## Ancillary data and vegetation measurements
- Ancillary meteorological data: air temperature (TA), relative humidity (RH), barometric pressure (PA), net radiation (NETRAD) and components (SW_IN/OUT, LW_IN/OUT), soil heat flux (G), soil moisture (SWC) and temperature (TS), precipitation (P).
- Water table depth at peatlands where possible.
- Vegetation data: canopy height, leaf area index (LAI), biomass; destructive sampling for carbon allocation where applicable.

## Data processing, quality control, and gap filling
- Flux calculations via EddyPro software (v7.0.6) with 30-minute flux averages.
- QC steps include:
  - Outlier removal using median absolute deviation.
  - Stationarity and turbulence tests; friction velocity (U*) thresholds to filter low-turbulence periods.
  - Footprint analysis to ensure >80% flux originates from the target ecosystem.
  - Visual inspection and manual corrections for clearly erroneous values.
- Data processing choices align with established EC methodology (e.g., angle-of-attack corrections, coordinate rotation, cospectral corrections, density corrections).
- Gap filling and flux partitioning:
  - Gap filling with Marginal Distribution Sampling (Reichstein et al., 2005).
  - NEE partitioned into GPP and Reco using day/night methods (Lasslop et al., 2010); implemented with REddyProc in R.
  - Ancillary data gap-filled where possible using COSMOS-UK sites.
- Data are quality assured, with details documented in data processing references and accompanying metadata.

## Data structure and access
- Time series delivered as separate CSV files for each of the six EC sites.
- Each file follows the schema described in UK-SCAPE_Data_Dictionary.csv and covers the complete interval defined in UK-SCAPE_Y6_Site_Metadata.csv.
- Missing records are encoded as -9999; TIMESTAMP_START and TIMESTAMP_END may appear in scientific notation in some software.

## Metadata and documentation
- Site-level metadata described in UK-SCAPE_Y6_Site_Metadata.csv (site name, file name, dates, land use, soil type, climate, coordinates, instrument models, measurement heights).
- Variable definitions and units provided in UK-SCAPE_Data_Dictionary.csv.
- Vegetation data provided as non-continuous time series; details also referenced in the data dictionary.

## Data governance and acknowledgments
- Data collection funded by the NERC UK-SCAPE programme; collaboration with landowners and partner organizations acknowledged.
- Data quality and processing follow established, peer-reviewed methodologies; source instruments and processing steps are clearly documented to enable scrutiny, replication, and reuse.

## Relevance for monitoring frameworks and policy decisions
- Provides standardized, quality-assured flux measurements across multiple site types and climates, enabling cross-site comparisons and trend assessments.
- Includes comprehensive metadata, QC, and gap-filling protocols, aligning with data governance needs for monitoring programs.
- Supports evaluation of land–atmosphere interactions, energy balance closure, and carbon flux dynamics under diverse land uses, informing policy decisions on land management, climate adaptation, and environmental health monitoring.