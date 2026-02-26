# Data output supporting information document

- This document describes the Chempop WP1 data product: Fish abundance, habitat, water quality, flow and climate in English rivers from 1975 to 2017.
- It provides a time-series dataset for 1180 English river sites, using sites with at least 10 annual fish surveys between 1975 and 2017.
- Covariates and ancillary data cover habitat quality (RHS, HABSCORE, HMS, HQA), land cover upstream of sites, water quality determinants, effluent dilution, hydrology (river discharge, baseflow), temperature (degree days), climate indices (Gulf Stream Index, NAOI) and altitude.
- The dataset is designed as an open data product to support environmental data analyses and modelling, with site-level linkage via unique fish site identifiers across multiple region-specific files.

## Data contents and structure

- Time-series data: species-specific fish abundances (densities per unit area) at 1180 fish sites from 1975–2017.
- Covariates and ancillary data:
  - River Habitat Survey (RHS) and Habitat Quality Scores (HMS, HMS Class, HQA; HMS/HQA linked to fish sites via nearest RHS within 5 km).
  - HABSCORE habitat data for Atlantic salmon and brown trout where available.
  - Land cover upstream of each fish site (Woodland, Arable, Seminatural, Urban) and corresponding areas (km2).
  - Water quality determinants and outputs from 41 determinands (via WIMS data) with handling of LOQ and threshold policies.
  - Hydrology statistics and discharge data from NRFA; nearest gauging stations matched to fish sites.
  - Effluent Dilution Factor (EDF) estimates from the LF2000-WQX model, linked to fish sites.
  - Altitude data derived from the IHDTM (cell-centre values).
  - Water temperature proxies: cumulative degree days (≥12°C) calculated for year prior to each survey; temperature modelling via GAMMs stratified by Base Flow Index (BFI).
  - Climate covariates: Gulf Stream Index (GSI) and North Atlantic Oscillation Index (NAOI) with annual values.
- File and data organization (regionally split and linked by a central site identifier):
  - CP_Fish_DataTable and CP_Fish_DataTable_Region.csv
  - CP_Fish_SiteTable and CP_Fish_SiteVariables_Region.csv
  - CP_Fish_SpeciesTable.csv
  - CP_Fish_HydrologyStats_Region.csv
  - Region-specific WIMS stats: Region_FISHWIMSStats_DET.csv (per chemical determinand)
  - Covariates and auxiliary tables: RHS scores, Land Cover Map ENG_Fish_LC2015.csv, GSI/NAOI data, Deg Days, IHDTM altitude
- Metadata and data sources are documented within the dataset and includes validation/workflow notes and processing steps.

## Data sources and accessibility

- Fish abundances and site data: Environment Agency National Fish Population Database (NFPD); open-access data portal provided with site-level survey counts.
- Habitat data: River Habitat Survey (RHS) and HABSCORE (EA regional data; access restricted in some regions and requested for Chempop matching).
- Habitat quality and structure: RHS, HMS, H QA, and HABSCORE provide habitat-related covariates.
- Land cover: UKCEH Land Cover Map 2015; upstream catchment calculations via IHDTM and GIS/python workflows.
- Water quality: UK Environment Agency Water Quality Data Archive; 41 determinands accessed via WIMS/EDF workflow with data licensing considerations.
- Hydrology: NRFA (UKCEH) daily river flow data; matching fish sites to gauging stations along the river network.
- Temperature and climate: CHESS-MET (UKCEH), GSI (Plymouth Marine Laboratory), NAOI (NCAR climatedataguide).
- Altitude: IHDTM-based elevation data.

## Processing workflow (overview by data domain)

- Fish abundance (NFPD data processing)
  - Download Freshwater Fish Counts for all species; retain sites with ≥10 surveys (1975–2017).
  - Remove juvenile-only datasets; convert raw counts to densities (per unit area).
  - Handle semi-quantitative surveys and first-catch during quantitative surveys; exclude qualitative surveys or calibrations lacking effort data.
  - Align species coding to Chempop codes; aggregate to single code per species where possible.
  - Document workflow steps for traceability (download, filter, convert to densities, standardise species codes).

- River Habitat Survey (RHS) and HABSCORE
  - Match RHS site locations to fish sites within 5 km along the river network using ArcGIS IRN extension.
  - Extract HMS (habitat modification score) and HQA (habitat quality assessment) values for matched RHS sites.
  - For HABSCORE, request data from EA and attach to relevant fish-site surveys where available; note limited coverage.

- Land cover
  - Use LCM2015 (25 m) raster, IHDTM alignment; rasterise to 50 m grid; compute upstream land cover proportions via GRASS r.accumulate.
  - Extract woodland, arable, seminatural, and urban percentages and areas upstream of each fish site; aggregate to four macro-categories.
  - Validate that aggregated macro-categories sum to ~100%.

- Water temperature
  - Compile water temperature data from gauging stations (≥3 years of data) and supplement with CHESS-MET daily air temperature data.
  - Compute cumulative degree days (DD) for days ≥12°C in the year prior to each survey.
  - Implement GAMM-based temperature predictions with seven models (BFI-based stratification; ARMA error structures) and select models by RMSE, normalized RMSE, and scatter index.
  - Model temperature per 0.1 increment of BFI; calculate site-specific water temperature and then degree-days.

- Hydrology
  - Integrate NRFA flow data with fish sites; snap gauging stations to the nearest line of the river network.
  - Compute network-distance between fish sites and gauges; extract 3-, 6-, and 12-month flow statistics prior to survey dates.
  - Perform manual QA in GIS to resolve discrepancies.

- Effluent Dilution Factor (EDF)
  - Use the LF2000-WQX model to estimate wastewater contribution (significant WWTWs only; 95% of DWF coverage).
  - Associate each fish site to the nearest reach on the 1:50,000 river network; assign EDF values where distances are unique or resolve ties.
  - Report EDF metrics as mean, standard deviation, 90th and 95th percentiles (EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95).
  - Flag gaps where segments are omitted due to network issues.

- Water quality determinands
  - Identify nearest three chemical determinand sites per fish site using ArcGIS Near Table; apply suitability checks (sample counts, time overlap, absence of intervening sewage works, river size considerations, etc.).
  - Extract determinand data for the 41 chemicals from the Water Quality Data Archive for the antecedent 12 months before each fish survey.
  - Apply LOQ handling (various LOQ options) and maximum thresholds for some metals; compute summary statistics per determinand site.
  - Exclude sites due to licensing constraints; document data quality checks.

- Altitude
  - Link fish site coordinates to IHDTM altitude values via ArcGIS Extract Multi Values to Points.
  - Record cell-centre altitude values for each site.

- Climatic variables (GSI and NAOI)
  - Download annual GSI (mean values) and annual NAOI values; extract relevant years.
  - Attach GSI and NAOI covariates to fish-site records.

## Data notes and caveats

- Location coordinates may differ slightly between Fish Site Table and Data Table; exact survey points may vary.
- HABSCORE data has incomplete regional coverage and may not be fully matchable to every fish site.
- Some WQ determinand data are licensed or restricted; certain sites are excluded from final datasets.
- The dataset emphasizes longitudinal comparability by filtering survey counts, standardising species codes, and aligning covariates upstream of survey points.

## Key considerations for data leaders

- Provenance and traceability: detailed, domain-specific processing steps and data provenance are documented to enable reproducibility.
- Data integration: multiple disparate data sources (ecology, habitat, land use, hydrology, chemistry, climate) are harmonised around common fish-site identifiers and river-network geometry.
- Data quality and gaps: explicit handling of LOQ, thresholds, licensing restrictions, and matching limitations; manual QA steps are described.
- Governance and accessibility: structured region-specific files with clear metadata; open-data intent with linked sources and processing notes.
- Applications: dataset supports ecological modelling, trend analysis, habitat assessment, and environmental management decisions across England’s river basins.