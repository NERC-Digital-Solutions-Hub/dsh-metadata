# Emissions of metals and air pollutants in the UK, 1750 - 2100 (1km x 1km)

## Summary
- A 1km x 1km gridded dataset of UK emissions for seven air pollutants (CO, NH3, NOx, PM2.5, PM10, SO2, NMVOCs) and five metals (Cd, Cu, Ni, Pb, Zn) from 1750 to 2100, aligned to 11 SNAP sectors used in the UK National Atmospheric Emissions Inventory (NAEI).
- Combines historical reconstructions (1750–1960), contemporary inventories (1970–2018) and future scenario modelling (2040–2100).
- Outputs are expressed as tonnes per km2 per year (t km-2 y-1) for every 1km2 cell; missing data are NA.
- Data designed for integration with atmospheric models and for monitoring environmental health and policy performance over time.

## Contents by period and data scope
- Historical emissions (1750–1960)
  - Based on literature for key fuels, processes, and sectors; uses calibration of emission factors (EFs) over time (including S-shaped curves where EFs change pre-1970).
  - Metals emissions tied to coal/oil content and ash enrichment; spatial distribution via proxies (population, land use, proximity to water/roads).
  - Northern Ireland data proxyed with random forest due to limited pre-1950 data.
- Contemporary emissions (1970–2018)
  - Informed directly by NAEI (UK emissions inventory, 2021); NH3 starts in 1980.
  - Spatial distributions anchored to 2018 data, back-cast to earlier years (e.g., 2000) by scaling to UK totals.
- Future emissions (2040–2100)
  - Five UK-specific SSP scenarios (SSP0–SSP5) across three target years (2040, 2070, 2100).
  - 18 indicator variables (e.g., population, fertiliser use, transport, livestock) scaled to each SNAP sector and converted to factors applied to 2018 baselines.
  - NH3 EFs adjusted to SSP projections; diffuse emissions use land-use inputs from CRAFTY-GB model.

## Pollutants, metals, and units
- Pollutants: CO, NH3, NOx, PM2.5, PM10, SO2, NMVOCs.
- Metals: Cd, Cu, Ni, Pb, Zn.
- Units: tonnes per km2 per year (t km-2 y-1) for every 1km2 cell; NA indicates no data.

## Data structure and access
- Files: 3,688 total, covering 7 pollutants and 5 metals across 11 SNAP sectors.
- File naming convention: Sxx_p_emis_SSPi_y_t_km2.tif
  - xx = SNAP sector (01–11)
  - p = pollutant code (cd/cu/ni/pb/zn/co/nh3/nox/pm10/pm25/sox/voc)
  - i = SSP scenario (0–5; 0 = past to present)
  - y = year (ranging from 1750–1960s to 2100, including 2018, 2040, 2070, 2100)
- Folder structure: data/p/y/filename.tif
- Temporal coverage representation
  - 1750–2018 represented on a single timeline (SSP0 for continuity)
  - 2040/2070/2100 modeled for all five SSPs

## Spatial and methodological notes
- 1km x 1km spatial grid uses OSGB projection.
- Contemporary diffuse and point emission patterns are aligned to 2018 baseline for continuity back to 2000.
- Historical period relies on proxies and literature-based EF adjustments to reflect technology changes; NI data pre-1950 rely on statistical estimation.
- QA/QC linked to NAEI; full QA/QC performed for 2018 across multiple species; model outputs validated against atmospheric observations where possible.

## Quality control and validation
- Emissions totals (1970–2018) anchored to NAEI 2021; QA/QC methods inherited from NAEI.
- Visual mapping checks across the UK for pollutant deposition; time-series comparisons with observations where available.
- Full QA/QC conducted for selected year (2018) across multiple species.

## Data structure details and acknowledgements
- Data files include historical, contemporary, and future projections; future years modelled for all SSPs whereas 1750–2018 data are consolidated.
- Acknowledgements include data sources drawn from historical records, population data, land-use modeling, and SSP-related frameworks.
- References include key methodology and data sources for historical emission factors, EPA WebFIRE, EMEP/EAA guides, NAEI reports, and SSP co-design work.

## Relevance to environmental monitoring and analysis
- Enables trend analysis of emissions over more than 250 years at high spatial resolution, supporting monitoring of environmental health and policy performance.
- Provides a consistent, openly structured dataset suitable for atmospheric modelling and scenario planning.
- Highlights challenges in maximizing dataset value through data integration and ensuring broad data accessibility for downstream users.