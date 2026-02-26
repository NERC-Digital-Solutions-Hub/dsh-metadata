# Emissions of metals and air pollutants in the UK, 1750 - 2100 (1km x 1km)

- Purpose and scope
  - Provides 1km x 1km spatial estimates of emissions for seven air pollutants (CO, NH3, NOx, PM2.5, PM10, SO2, NMVOCs) and five metals (Cd, Cu, Ni, Pb, Zn) in the UK.
  - Time span from 1750 to 2100 across three temporal regimes: historical (1750–1960), contemporary (1970–2018; NH3 begins 1980), and future (2040, 2070, 2100).
  - Emissions are represented per 1km2 cell and per year in tonnes per km2 per year; missing data are NA.
  - Data organized within 11 SNAP sectors (consistent with UK National Atmospheric Emissions Inventory).

- Pollutants, metals and sectors
  - Pollutants: CO, NH3, NOx, PM2.5, PM10, SO2, NMVOCs.
  - Metals: Cd, Cu, Ni, Pb, Zn.
  - Spatial grid: 1km x 1km across Great Britain and Northern Ireland; OSGB projection.

- Data sources, methodology and scaling
  - Historical emissions (1750–1960): literature-based estimates, emission factors (EFs) adjusted for coal/oil combustion; S-shaped interpolation to 1970; metal emissions tied to coal/oil metal content and ash enrichment; spatial distribution via proxy data (population, census, land use, proximity to features).
  - Northern Ireland: proxies estimated with a random forest approach due to limited pre-1950 data.
  - Contemporary emissions (1970–2018): directly from UK NAEI 2021; diffuse and point emissions distributed with 2018 patterns back to 2000 for APs; NH3 distribution from historical modelling for earlier years; metals scaled to UK totals.
  - Future emissions (2040–2100): modelled using UK-specific Shared Socioeconomic Pathways (SSPs) with 18 indicator variables (e.g., population, fertiliser use, transport, livestock); SSP-based scaling applied to 2018 baselines; NH3 EFs adjusted via Defra’s Scenario Modelling Tool to align with SSPs; land-use inputs from CRAFTY-GB for distributing diffuse sources.

- Data structure and access
  - File naming: Sxx_p_emis_SSPi_y_t_km2.tif
    - xx = SNAP sector (01–11)
    - p = pollutant code (cd/cu/ni/pb/zn/co/nh3/nox/pm10/pm25/sox/voc)
    - i = SSP scenario (0–5; 0 represents past to present)
    - y = year (1690s through 2100; includes 1750, 1760, …, 2018, 2040, 2070, 2100)
  - Folder structure: data/p/y/filename.tif
  - Total files: 3,688 (7 pollutants × 5 metals × 11 SNAP sectors × SSP/time combinations)
  - Data coverage notes:
    - 1750–2018 presented on a single timeline (SSP0 for continuity)
    - 2040/2070/2100 provided across 5 SSP scenarios
    - No-data values represented as NA
  - Unit and projection: tonnes per km2 per year (t km-2 a-1); OSGB projection

- Quality assurance and validation
  - 1970–2018 totals anchored to UK NAEI (2021) with QAQC methods from NAEI
  - Visual mapping checks for deposition across the UK
  - Time-series comparisons of atmospheric concentrations against observations where available
  - Full QA/QC performed for 2018 for multiple species

- Practical notes for data support and use
  - Intended for researchers and analysts to examine historical, current, and future emissions and to support atmospheric modelling and data-visualisation products
  - Some data, especially for Northern Ireland and pre-1970 historical periods, rely on proxies and modelling assumptions
  - NH3 data availability differs (begins in 1980 for historical period; otherwise modelled)
  - Outputs are designed to support self-service data exploration and integration with related inventories (e.g., NAEI)

- Acknowledgements and references
  - Key sources and methodologies include Bond et al. (2007); EPA WebFIRE (2021); EMEP/EEA (2019); NAEI (2021); Pedde et al. (2021); Shaw-Taylor et al. (2006); Levy et al. (2018); Nalbandian (2012); and related data products and models (e.g., CRAFTY-GB)