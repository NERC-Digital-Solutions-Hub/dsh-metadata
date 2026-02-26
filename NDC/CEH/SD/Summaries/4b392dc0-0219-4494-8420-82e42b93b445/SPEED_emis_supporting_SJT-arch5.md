# Emissions of metals and air pollutants in the UK, 1750 - 2100 (1km x 1km)

## Overview
- Dataset of estimated emissions for seven air pollutants (CO, NH3, NOx, PM2.5, PM10, SO2, NMVOCs) and five metals (Cd, Cu, Ni, Pb, Zn) in the UK from 1750 to 2100 at 1km x 1km resolution.
- Emissions are organized using the SNAP (11 sectors) framework consistent with the UK National Atmospheric Emissions Inventory (NAEI).
- Combines historical research, contemporary inventories, and future scenario modelling.

## Data content and scope
- Pollutants: CO, NH3, NOx, PM2.5, PM10, SO2, NMVOCs.
- Metals: Cadmium (Cd), Copper (Cu), Nickel (Ni), Lead (Pb), Zinc (Zn).
- Spatial framework: 1km x 1km grid, OSGB projection; 11 SNAP sectors (01–11).
- Temporal coverage:
  - Historical: 1750–1960 (estimates constructed from literature and sectoral proxies).
  - Contemporary: 1970–2018 (NH3 starts in 1980); based on UK NAEI 2021 data.
  - Future: 2040, 2070, 2100 across five Shared Socioeconomic Pathways (SSPs; SSP0–SSP5).

## Spatial resolution and units
- Values reported as tonnes of pollutant per km² per year (t km⁻² y⁻¹).
- Northern Ireland proxy data estimated with a random forest approach due to limited pre-1950 data.
- 3,688 individual files cover 7 pollutants and 5 metals across 11 SNAP sectors; 2040/2070/2100 data include all SSPs.

## Data structure and access
- File naming convention: Sxx_p_emis_SSPi_y_t_km2.tif
  - Sxx: SNAP sector (01–11)
  - p: pollutant/metal code (cd/cu/ni/pb/zn/co/nh3/nox/pm10/pm25/sox/voc)
  - i: SSP (0–5; 0 = past to present)
  - y: year (1750–1960 timeline; 2018; 2040/2070/2100)
- Folder structure: data/p/y/filename.tif
- Data are tied to QAQC processes within NAEI; time series and spatial checks performed against observations where available.

## Methodology and data provenance
- Historical period (1750–1960): emissions inferred from literature; emission factors adjusted over time to reflect technology changes; metals linked to coal/oil content and ash enrichment.
- Contemporary period (1970–2018): APs distributed using 2018 diffuse/point distributions scaled to UK totals; NH3 distribution linked to historical modelling for 1970; metals distribution scaled from 2018 to 1970 totals.
- Future period (2040–2100): SSP-based projections using 18 key indicators (e.g., population, fertiliser use, transport, livestock) converted to scaling factors applied to 2018 UK emissions; NH3 EF adjustments aligned with SSP projections; diffuse land-use inputs derived from the CRAFTY-GB model.
- Data values are prepared for use in atmospheric chemistry transport modelling; linked to NAEI datasets for traceability.

## Quality assurance and validation
- QAQC methods anchored to UK NAEI procedures; overall totals validated against NAEI 2021 data (1970–2018).
- Visual mapping checks for pollutant deposition across the UK; time-series comparisons with observations where available.
- Full QA/QC conducted for a selected year (2018) across multiple species.

## Data governance and stewardship considerations
- Comprehensive provenance: historical literature, government records, EPA WebFIRE (for APs), NAEI inventories, and SSP-based scenario work.
- Metadata and file naming conventions support reproducibility and interoperability across GIS and environmental modelling workflows.
- Clear scope on data availability: 1750–2018 represented on a single historical timeline; 2040/2070/2100 provided for SSPs; certain years or SSPs may be absent if not modelled.
- Practical implications for data stewards:
  - Manage and document model assumptions, especially for historical EF adjustments and NI spatial estimations.
  - Maintain alignment with SNAP sector definitions and OSGB projection to ensure interoperability with other UK emissions datasets.
  - Plan for updates as SSPs are refined or new inventory updates become available; preserve versioning and lineage.

## Limitations and caveats
- Some periods rely on proxy-based distributions and literature-derived factors, introducing uncertainty.
- Northern Ireland data for early years are statistically estimated due to limited pre-1950 data.
- No-data values are explicitly indicated as NA where emissions are not modelled.
- Future projections depend on SSP narratives and semi-quantitative trend lines, which carry inherent uncertainty.

## Acknowledgements and references
- Acknowledges data sources and methodological references including Bond et al. (2007), EPA WebFIRE (2021), EMEP/EEA guidebooks (2019), NAEI (2021), Pedde et al. (2021), and others cited in the dataset documentation.