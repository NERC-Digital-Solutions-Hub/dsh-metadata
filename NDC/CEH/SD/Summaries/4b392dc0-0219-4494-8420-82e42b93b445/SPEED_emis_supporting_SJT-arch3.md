# Emissions of metals and air pollutants in the UK, 1750 - 2100 (1km x 1km)

## Overview
- Provides 1km x 1km resolution estimates of seven air pollutants (CO, NH3, NOx, PM2.5, PM10, SO2, NMVOCs) and five metals (Cd, Cu, Ni, Pb, Zn) for the UK from 1750 to 2100.
- Data are organized by SNAP sectors (01–11) in the UK National Atmospheric Emissions Inventory (NAEI) framework and cover historical, contemporary, and future scenarios.
- Aims to support environmental health monitoring for policy scrutiny, evaluation, and informing future decisions.

## Contents (Pollutants and metals)
- Pollutants: CO, NH3, NOx, PM2.5, PM10, SO2, NMVOCs
- Metals: Cd, Cu, Ni, Pb, Zn
- Spatially distributed onto 1km x 1km grids across the UK (including Northern Ireland)

## Temporal coverage
- Historical: 1750–1960 (pre-1970 period)
- Contemporary: 1970–2018 (NH3 begins 1980)
- Future: 2040, 2070, 2100 (three time points across multiple SSP scenarios)

## Methodology by period

- Historical emissions (1750–1960)
  - Based on literature research for key fuels and processes; prioritises contributors to total emissions in the contemporary era.
  - Emission factors (EFs) adjusted over time to reflect technology and practice changes; metals linked to metal content in coal/oil and ash enrichment.
  - Spatial distribution using proxies (population, census employment, land use, proximity to features); NI data estimated via random forest due to limited pre-1950 data.

- Contemporary emissions (1970–2018)
  - Taken directly from the UK NAEI (2021) with NH3 starting in 1980.
  - Spatial distribution uses 2018 patterns back to 2000 for diffuse emissions; year-specific scaling for SNAP totals (1970–1995).
  - Metals distributed using 2018 diffuse+point surfaces scaled to UK totals back to 1970 (no direct NI point data).

- Future emissions (2040–2100)
  - UK-specific SSPs (SSP0–SSP5) with 18 indicator variables (e.g., population, fertiliser use, transport, livestock) adjusted to each SNAP sector.
  - Trends converted to scaling factors applied to 2018 UK emission values.
  - NH3 EF adjustments aligned with SSP projections; land-use inputs from CRAFTY-GB model.

## Spatial framework and units
- All emissions are in tonnes per square kilometre per year (t km^-2 a^-1).
- Data stored as GeoTIFF files with naming: Sxx_p_emis_SSPi_y_t_km2.tif
  - Sxx = SNAP sector (01–11)
  - p = pollutant/element code (cd/cu/ni/pb/zn/co/nh3/nox/pm10/pm25/sox/voc)
  - i = SSP scenario (0–5; 0 indicates past-to-present)
  - y = year (multiple years from 1750 to 2100)
- Total files: 3,688 (7 pollutants × 5 metals × 11 sectors × SSPs for future years)

## Data quality and validation
- QA/QC anchored to the NAEI framework for 1970–2018 totals.
- Visual mapping checks across the UK for deposition patterns; time-series comparisons with observations for metals.
- Full QA/QC performed for a selected year (2018) across multiple species.
- Uncertainties arise from historical EF estimates, proxy-based spatial allocations, and NI data gaps prior to 1950.

## Data structure and accessibility
- File structure: data/p/y/filename.tif
- No-data values represented as NA
- NI spatial distribution derived via random forest due to limited pre-1950 data

## Data provenance and references
- Historical EF sources include Bond et al. (2007), WebFIRE (EPA, 2021), EMEP/EEA guidelines (2019)
- Contemporary inventories: NAEI (2021); Garland et al. (2022)
- SSP framework and scenario development: Pedde et al. (2021); related land-use modeling (CRAFTY-GB)
- Supporting datasets and historical context: Shaw-Taylor et al. (2006)

## Implications for monitoring frameworks
- Demonstrates integrating long-term historical reconstructions, contemporary inventories, and future scenario modelling within a single high-resolution framework.
- Highlights the importance of robust metadata, data provenance, and transparent QC/QA processes for monitoring.
- Reveals challenges relevant to monitoring authors:
  - Reliance on EF-based historical reconstructions with uncertainties.
  - Dependence on proxies and modelling choices for spatial distribution.
  - Data gaps for Northern Ireland prior to 1950 and the need for clear data governance when sharing underlying data.
  - The need to maintain openness and data sharing while ensuring data quality and versioning.

## Relevance to policy and decision-making
- Provides a comprehensive historical-to-future emissions backbone to assess policy effectiveness, sector contributions, and potential health impacts.
- Supports scenario planning and monitoring of environmental health indicators under different SSP pathways.
- Enables stakeholders to scrutinise trends, identify data gaps, and refine monitoring strategies and governance mechanisms.