# Data output supporting information document

- Timeframe: 1975–2017
- Scope: Fish abundance, habitat, water quality, flow and climate in English rivers; 1180 fish sites; open data product intended for wide reuse
- Purpose: Consolidate multi-source covariates and life-history data to support environmental analyses and modelling (ChemPop context)

## Dataset contents and structure

- Primary outputs:
  - Fish abundance and covariates tables (site-level and regionally broken)
  - Species-level mappings and codes
  - Hydrology, land cover, habitat, water quality determinands, and related covariates
  - Climate covariates (Gulf Stream Index, NAOI)
  - Derived metrics: degree-days, EDF (effluent dilution factor)
- Key tables and files (examples):
  - CP_Fish_DataTable and CP_Fish_SiteTable (region-specific csvs)
  - CP_Fish_SpeciesTable
  - CP_Fish_HydrologyStats_Region.csv
  - Region_FISHWIMSStats_DET.csv (41 chemical determinands)
  - Land Cover: ENG_Fish_LC2015.csv
  - RHS scores: RHS scores_V2.xls
  - HABSCORE data (regional EA data)
  - Altitude: 20201110_NFPD_Fish_ENG_Altitude
  - EDF: CP_0101_FISH_England_keys_v1_figures.csv and related EDF_Sites
  - WIMS: Region_FISHWIMSStats_DET.csv per region
  - Degree days: NFPD_CumulativeDegreeDays.csv
- Data sources and access
  - National Fish Population Database (NFPD)
  - River Habitat Survey (RHS) and HABSCORE (EA/UK sources)
  - Land Cover Map 2015 (UKCEH)
  - Water quality data archive (Environment Agency) and LF2000-WQX model (EDF)
  - Hydrology: NRFA (UKCEH)
  - Climate: Gulf Stream Index (GSI) and NAOI
  - CHESS-MET (air temperature) and CHESS data
- Data management notes
  - Covariates are aligned to fish site locations via spatial matching (nearest or network-based)
  - Data are regionally partitioned and linked by a unique fish site identifier

## Covariates and data sources (highlights)

- Habitat and habitat quality
  - RHS: Habitat Modification Score (HMS) and Habitat Quality Assessment (HQA)
  - HABSCORE: salmon/trout habitat quality by size/species
- Land use
  - Land Cover Map 2015: Woodland, Arable, Semi-natural, Urban (upstream catchment)
  - Calculations done with GIS tools and Python, aggregating to four macro-categories
- Water temperature and climate
  - Water temperature: degree-days above 12C (annual; prior year)
  - CHESS-MET data for air temperature; baseflow effects via BFI
  - GAMM-based temperature predictions by BFI range
- Hydrology
  - River discharge and flows from NRFA; 3, 6, 12 months prior to surveys
  - Distances and network snapping between fish sites and flow gauges
- Water quality and effluent
  - 41 determinations (chemical concentrations) from WQ data archive
  - EDF (effluent dilution factor) estimated with LF2000-WQX model; association to fish sites
  - Determinand site selection criteria (nearest three candidates; sampling frequency; timing overlap)
  - LOQ handling and data quality thresholds for metals and other determinands
- Altitude
  - Altitude from IHDTM (cell-centre values; bilinear interpolation)
- Climatic indices
  - Gulf Stream Index (GSI): annual mean values
  - North Atlantic Oscillation Index (NAOI): annual values

## Data processing and analytical workflows

- General approach
  - Spatial alignment: match variables to fish sites using nearest-neighbour or river-network-based methods
  - Temporal alignment: ensure covariates align with survey dates (or year prior for degree-days)
  - Quality control and data cleaning: apply thresholds, handle LOQ, exclude unsuitable data
  - Data integration: assemble multi-table linkage via unique Fish_SiteID

- Fish abundance and covariates (NFPD-derived)
  - Select sites with at least 10 surveys (1975–2017)
  - Remove juvenile-only sites
  - Convert raw counts to densities; handle semi-quantitative and first-catch estimates
  - Normalize species codes to a single Chempop code; sum densities for variants when needed
  - Retain all surveys even if no fish were captured for sampling effort context

- River Habitat Survey (RHS) and HMS/HQA
  - GIS-based matching: align RHS sites to fish sites within 5 km along the river using IRN extension
  - Extract HMS and HQA values from matched RHS sites
  - HQA adjustments: adapt 1994 data to be comparable with later data
  - Note: RHS/HMS/HQA data availability may be partial due to data access limits

- HABSCORE
  - Request and integrate regional HABSCORE data where available
  - Acknowledge potential gaps due to data distribution and site matching

- Land cover
  - Rasterize Land Cover Map 2015 to 50 m grid; align with IHDTM
  - Use GRASS GIS to create category rasters; extract upstream catchment proportions
  - Group 21 land-cover types into four macro-categories (Woodlands, Arable, Seminatural, Urban)
  - Sum percentages and areas upstream of each fish site; verify totals near 100%

- Water temperature and degree days
  - Temperature data: from gauging stations (3+ years) plus CHESS-MET daily mean temperatures
  - Base Flow Index (BFI) classification (0.1 increments) to handle groundwater-influenced regimes
  - Develop seven GAMM models per BFI band; evaluate using RMSE, nRMSE, scatter index
  - Predict site-specific water temperature; compute cumulative degree days for the year prior to each survey

- Hydrology (river flow)
  - Snap NRFA gauging stations to the river network; compute distance along river between fish site and gauges
  - Extract 3/6/12-month flow statistics prior to survey dates
  - Manual checks for matching discrepancies in GIS

- Effluent Dilution Factor (EDF)
  - Use LF2000-WQX to model wastewater contributions (top 95% of DWF within catchments)
  - Associate EDF to fish sites via nearest 1:50,000 river network reach
  - Report EDF metrics: EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95
  - Flag data gaps where network matching is ambiguous

- Water quality determinands
  - Identify nearest three determinand sites via Near Table; manual suitability checks (sampling frequency, timing overlap, proximity to sewage works, river size)
  - Extract 41 chemicals from Water Quality Archive; apply LOQ handling and maximum thresholds for some determinands
  - Compute summary statistics for 12 months prior to survey
  - Exclude certain determinands/sites due to licensing restrictions

- Altitude
  - Extract site elevations from IHDTM using Extract Multi Values to Points
  - Use the centre of IHDTM cells for elevation values

- Climatic covariates
  - GSI and NAOI data retrieved; annual means used to represent climate context
  - GSI annual data sourced from Gulf Stream data; NAOI from NCAR Climate Data Guide
  - Align annually with fish survey windows

## Data handling, quality, and notes

- Location discrepancies
  - Minor differences between site coordinates in different data tables; acknowledged in data notes
- Data licensing and accessibility
  - Some WQ and RHS data restricted or variably accessible; licensing may affect inclusion
- Data integrity checks
  - Manual verification steps to confirm nearest-neighbour matches and appropriate covariate alignment
-Processing tools and coding
  - ArcGIS (10.6–10.8.x or Pro), QGIS, GRASS GIS
  - Python 3 for data extraction, transformation, and statistics
  - R (mgcv, dplyr, ggplot2, etc.) for GAMMs and degree-day calculations
  - Excel used for some tabular data processing

## Notes on data tables and metadata

- Site and survey identifiers
  - Fish_SiteID, Fish_SurveyID; coordinates and catchment context
- Covariate tables and variables
  - Land cover percentages/areas; BFI values; EDF metrics
  - GSI, NAOI; Degree Days; Hydrology statistics
- Data notes and caveats
  - Some RHS/HQS/HABSCORE data may be missing for particular sites
  - Certain determinands and EDF data may be blank where data are unavailable or licensing prevents inclusion

## Data access and provenance

- The dataset is designed as an open data product to enable environmental analyses and modelling across a broad user base
- Documentation includes comprehensive workflow steps, data sources, and processing notes to support reproducibility and reuse