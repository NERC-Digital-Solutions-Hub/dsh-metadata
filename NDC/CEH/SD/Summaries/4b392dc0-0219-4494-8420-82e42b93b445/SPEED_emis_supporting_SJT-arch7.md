# Emissions of metals and air pollutants in the UK, 1750 - 2100 (1km x 1km)

##Overview
- Dataset of emissions estimates for seven air pollutants (CO, NH3, NOx, PM2.5, PM10, SO2, NMVOCs) and five metals (Cd, Cu, Ni, Pb, Zn) across the UK at 1 km x 1 km resolution.
- Time span: 1750–2100, with three temporal pillars:
  - Historical emissions (1750–1960) modeled from literature and proxies.
  - Contemporary emissions (1970–2018) from NAEI; NH3 starts 1980.
  - Future emissions (2040, 2070, 2100) across 3 time points under UK SSP-based scenarios (SSP0–SSP5).
- Values expressed as tonnes per km^2 per year (t km^-2 a^-1); NA indicates no data.
- Data organized by 11 SNAP sectors used in the UK inventory.

##Spatial and data structure
- Projection: OSGB (1 km x 1 km grid).
- Data format: 3,688 GeoTIFF files with naming convention Sxx_p_emis_SSPi_y_km2.tif.
  - Sxx: SNAP sector (01–11)
  - p: pollutant code (cd/cu/ni/pb/zn/co/nh3/nox/pm10/pm25/sox/voc)
  - SSPi: SSP scenario (0–5; 0 covers past to present)
  - y: year (1750–1960 timeline; 1970–2018; 2040/2070/2100)
- Folder structure: data/p/y/filename.tif
- Files per pollutant/sector/year: 3,688 total; 2040/2070/2100 data present for all pollutants under SSPs; earlier years mapped to SSP0 timeline.

##Temporal coverage and data sources
- Historical (1750–1960): externally sourced emission factors adjusted over time; spatial allocation via diverse proxies (population surfaces, census data, land use, proximity to features); NI spatial data estimated with a random forest approach due to limited pre-1950 data.
- Contemporary (1970–2018): derived from UK NAEI 2021; NH3 distribution anchored to 2018 baseline for diffuse and point emissions; proxies used to distribute emissions spatially back to 2000 and 1970 where necessary.
- Future (2040–2100): based on UK-specific SSPs with 18 indicators (population, fertilizer use, transport, livestock, etc.) converted to scaling factors relative to 2018 emissions; NH3 EF adjustments aligned with SSP narratives; land-use inputs from CRAFTY-GB model.

##Data quality and validation
- Totals tied to NAEI (2021) with QAQC methods from NAEI.
- Visual checks across the UK for deposition patterns; time-series comparisons with observations where available.
- Full QA/QC performed for 2018 data; NI pre-1950 spatial allocations rely on statistical estimation due to sparse historic data.

##Notes for GIS use
- Units: tonnes per km^2 per year; 1 km resolution enables integration with other GIS layers (land use, population, infrastructure).
- Data is split across 11 SNAP sectors and multiple pollutants; can be aggregated by pollutant, sector, or year for analysis.
- Gaps and uncertainties:
  - Historical pre-1970 emissions rely on modeled proxies and EF adjustments; early-period uncertainty is higher.
  - NI and some early-year dispersions rely on statistical estimation rather than direct data.
  - Future projections reflect SSP scenario assumptions and carry scenario-specific uncertainties.

##Potential GIS workflows
- Create time-series maps of a single pollutant or metal to visualize spatial trends.
- Overlay with population density, land use, or health exposure datasets for risk assessment.
- Compare emissions with atmospheric deposition or concentration models to assess transport and deposition patterns.
- Use 1 km resolution to align with other gridded environmental datasets and facilitate multi-layer analyses.