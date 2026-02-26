# Emissions of metals and air pollutants in the UK, 1750 - 2100 (1km x 1km)

## Overview
- Provides 1km x 1km resolution estimates of emissions for seven air pollutants (CO, NH3, NOx, PM2.5, PM10, SO2, NMVOCs) and five metals (Cd, Cu, Ni, Pb, Zn) in the UK from 1750 to 2100.
- Emissions are reported using the 11 SNAP sectors (consistent with UK National Atmospheric Emissions Inventory, NAEI).
-3 temporal blocks: historical (1750–1960), contemporary (1970–2018), and future scenarios (2040–2100).

## Pollutants and metals
- Air pollutants: CO, NH3, NOx, PM2.5, PM10, SO2, NMVOCs.
- Metals: Cd, Cu, Ni, Pb, Zn.

## Temporal coverage and data structure
- Historical emissions (1750–1960): built from literature on key fuels/processes; emission factors (EFs) adjusted over time with S-shaped diffusion curves; metals linked to coal/oil content and ash enrichment.
- Contemporary emissions (1970–2018): from UK NAEI (2021); NH3 starts in 1980; spatial distributions back-cast 2018 patterns to earlier years using sector totals and proxies.
- Future emissions (2040–2100): modelled for three time points (2040, 2070, 2100) across five SSP scenarios; SSP-based indicator trends applied to 2018 baselines; NH3 EFs aligned with SSP projections.
- Units: tonnes per km² per year (t km⁻² a⁻¹); no-data values are NA.

## Spatial distribution and data proxies
- Grid: 1km x 1km, OSGB projection; SNAP sectors used for consistency with NAEI.
- Distribution method: spatial proxies including population surfaces, census employment, land use, proximity to water/roads, and digitised data.
- Northern Ireland: proxies estimated via random forest due to limited pre-1950 data.

## Data sources and modelling approach
- Historical period: emission factors adjusted for coal/coke/oil use; S-curves to represent technology development; metals linked to fuel content and ash enrichment.
- Contemporary period: direct NAEI data; spatial back-casting uses 2018 distributions and UK totals back to 1970 (NH3 follows historical modelling for early years).
- Future period: SSP narratives with 18 indicator variables; scaling factors applied to 2018 UK emissions; land-use inputs from CRAFTY-GB model for diffuse sources.

## Quality control and validation
- QA/QC aligned with NAEI methods; atmospheric chemistry transport model used for validation.
- Visual UK-wide checks for pollutant deposition; time-series comparisons with observations where available.
- Full QA/QC performed for 2018 across multiple species.

## File structure and data catalog
- File naming convention: Sxx_p_emis_SSPi_y_t_km2.tif
  - Sxx: SNAP sector (01–11)
  - p: pollutant code (cd/cu/ni/pb/zn/co/nh3/nox/pm10/pm25/sox/voc)
  - i: SSP scenario (0–5; 0 = past to present)
  - y: year (ranging from 1750 to 2100 at specified intervals)
- Total files: 3,688 (7 pollutants + 5 metals across 11 SNAP sectors; all 2040/2070/2100 data modelled for SSPs; 1750–2018 data in SSP0 for continuity).
- Folder structure: data/p/y/filename.tif
- Coverage notes: no-data values indicated as NA; 2018 data linked to NAEI; future years generated under SSP scenarios.

## Acknowledgements and references
- Acknowledges data sources and supporting studies (e.g., Bond et al. 2007; EPA WebFIRE; EMEP/EEA guidebook; NAEI 2021; SSP literature; UK data archives).
- References supplied for method and data provenance.

## Implications for data leadership and reuse
- Data lineage: combines historical literature, national inventories, and forward-looking scenario modelling; complex transformations and normalisations across centuries.
- Metadata considerations: explicit temporal coverage, SSP scenario, pollutant/metal codes, units, spatial resolution, and data gaps.
- Reuse potential: suitable for long-term atmospheric modelling, historical exposure analysis, and cross-era policy assessments.
- Limitations to note: early-period data gaps in Northern Ireland; reliance on proxies for historical spatial distribution; future projections depend on scenario assumptions and modelling tools.