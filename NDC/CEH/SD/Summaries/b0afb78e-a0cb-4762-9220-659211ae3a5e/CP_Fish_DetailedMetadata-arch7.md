# Data output supporting information document

- The document describes the Fish abundance, habitat, water quality, flow and climate in English rivers 1975-2017 dataset, a time-series collection for 1180 English river sites. It explains dataset structure, covariates, data sources, processing workflows, and coding/processing details used to create an open data product for environmental analyses.

## Dataset scope, structure and content

- Time span: 1975–2017.
- Coverage: 1180 fish sites in English rivers (selected from EA National Fish Population Database with at least 10 annual surveys between 1975 and 2017; juvenile sites removed for the fish dataset; raw surveys converted to densities).
- Core data tables and files (organized by region where applicable):
  - CP_Fish_DataTable and region-specific variants (fish abundances, site/date/species densities; region CSVs).
  - CP_Fish_SiteTable and region-specific site variables (location, RHS/HABSCORE covariates, land cover, altitude, etc.).
  - CP_Fish_SpeciesTable (Chempop species codes linked to EA species codes).
  - CP_Fish_HydrologyStats_Region (hydrology statistics by site and date).
  - CP_Fish_ChemicalDeterminand (region-specific WIMS data files for 41 determinands).
  - Region-specific data files for RHS, HABSCORE, land cover, WQ, hydrology, EDF, deg_days, GSI/NAOI, altitude, and other covariates.
- Data relationships: linked by a unique fish site identifier; site-level covariates are linked to survey records and species densities.

## Covariates and data sources (covariates by theme)

- Habitat and habitat quality
  - RHS (River Habitat Survey) and HMS (Habitat Modification Score) and HQA (Habitat Quality Assessment).
  - HABSCORE habitat assessments for Atlantic salmon and brown trout (density-based HQS estimates).
- Land use and landscape context
  - Land Cover Map 2015 (woodlands, arable, semi-natural, urban; upstream catchment areas).
- Hydrology and climate
  - Water temperature (gas produced via degree days; CHESS-Met data; baseflow index, BFI).
  - River discharge/flow statistics (NRFA UK data; 3/6/12-month summaries).
  - Climate indices (Gulf Stream Index, GSI; North Atlantic Oscillation Index, NAOI).
  - Altitude (IHDTM-based elevations at fish sites).
- Water quality and chemical determinants
  - 41 chemical determinands from UK Environment Agency Water Quality Data Archive (WQ determinands) via the LF2000 LFQX/EDF pathway.
  - Effluent Dilution Factor (EDF) derived from LF2000-WQX model to estimate wastewater contributions to river flows.
- Fish abundance data
  - NFPD (Environment Agency) freshwater fish survey data; site, survey date, species, and counts; processed into densities and linked covariates (HQS, RHS, etc.).
- Data sources (examples)
  - NFPD (EA) for fish counts.
  - HABSCORE data from EA regional offices.
  - RHS habitat data via River Habitat Survey portal.
  - Land Cover Map 2015 from UKCEH.
  - CHESS-MET (UKCEH CEH) for air temperature interpolation.
  - NRFA (UKCEH) for baseflow and river flow data.
  - GSI/NAOI from Plymouth Marine Laboratory and UCAR NCAR databases.
  - Water Quality Archive for determinands, EDF LF2000-WQX model data.

## Processing workflows (key modules and steps)

- Fish abundance data (NFPD)
  - Select sites with ≥10 surveys (1975–2017); remove juvenile sites.
  - Convert raw counts to densities (per unit area).
  - Treat semi-quantitative and first-catch data; address logarithmic-scale estimates (midpoints, fixed values for “Present”, handling of “Best Run” and “Survey” suffixes).
  - Map species to Chempop codes; aggregate where multiple EA codes map to one Chempop code.
  - Retain surveys with zero captures to preserve sampling effort.
  - Workflow summary:
    - Download NFPD counts.
    - Filter sites by survey count.
    - Remove juveniles; convert counts to densities.
    - Reconcile species codes; sum densities where needed.
    - Produce site-level data with covariates.
- River Habitat Survey (RHS), HMS, HQA
  - Use ArcGIS with IRN extension to match RHS sites to fish sites within 5 km along the river network.
  - Extract HMS and HQA scores for matched RHS sites; treat unmatched as missing data.
  - RHS/HMS/HQA data comprise a single RHS sample per site; recent RHS data used.
- HABSCORE
  - Request EA HABSCORE data; extract relevant site/date values; merge with fish site data where available.
  - Note limitations: incomplete match due to data access constraints; not all sites have HABSCORE values.
- Land cover
  - Combine 2015 Land Cover Map with IHDTM to quantify upstream land cover.
  - Rasterize land cover to 50 m grid; assign dominant category per cell; compute upstream proportions via GRASS r.accumulate.
  - Python-based extraction of percentages and areas for each fish site; group 21 classes into four macro-categories: Woodlands, Arable, Seminatural, Urban.
  - Outputs: Percent and area (km2) upstream for each macro-category.
- Water temperature
  - Gather water temperature gauging data (EA archive; supplemented by University of Hull) and CHESS-MET daily air temperature for fish sites and gauges.
  - Compute degree days (≥12°C) for the year prior to surveys.
  - Baseflow-dependent GAMMs (GAMM) built in R to predict water temperature; seven BFI strata (0.1 increments) using models with month, time, and/or air temperature, with ARMA error structures; model selection by RMSE, NRMSE, scatter index.
  - Outputs: predicted water temperature at each fish site; convert to cumulative degree days for study year prior to survey.
- Hydrology
  - NRFA flow data (NERC/UKCEH NRFA API).
  - Snap gauging stations to river network; compute nearest network distance; calculate 3/6/12-month flow summaries before survey dates.
  - Manual checks in GIS to validate automated matches.
  - Outputs: 3/6/12-month flow statistics per fish site; used as explanatory covariates.
- EDF (Effluent Dilution Factor)
  - LF2000-WQX model to estimate wastewater contributions; include only WWTWs accounting for 95% of catchment DWF contributions.
  - Associate fish sites with 1:50k river network; when distances tie, use the distributed EDF value; report mean, SD, and 90th/95th percentiles (EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95).
  - Exclude sites with data gaps or network mismatches.
- Water quality determinands
  - Identify nearest three chemical determinand sites to each fish site via Near Table in ArcGIS; manual suitability screening (sampling frequency, inter-site blocking by sewerage works, river size considerations, and time overlap with fish surveys).
  - Extract determinand data from Water Quality Archive for the preceding 12 months before fish survey.
  - Handle LOQ issues (options for below LOQ); apply thresholds for some metals (e.g., max value rules).
  - Compute summary statistics for the 12-month window; exclude licensing-restricted sites.
- Altitude
  - Extract site elevations from IHDTM using ArcGIS Extract Multi Values to Points.
- Climatic variables (GSI, NAOI)
  - GSI: Annual mean values from Gulf Stream Data; NAOI: Annual values from NCAR Climate Data Guide.
  - Use annual means for the study period; align to fish survey years.
- Data integration and outputs
  - All covariates linked to the fish site table and fish survey records; constructed as a comprehensive data product for environmental analyses and modelling.

## Data tables and fields (high-level overview)

- Fish Site Table (CP_Fish_SiteVariables_region.csv)
  - Fish_SiteID, Fish_Name, Fish_River, Catchment, Easting, Northing
  - HQA_Score, HMS_Score (habitat covariates)
  - Fish_Altitude
  - Land cover percentages and areas (Woodland, Arable, Seminatural, Urban; upstream)
  - BFI, EDF_Mean, EDF_SD, EDF_Q90, EDF_Q95
  - Missing data codes: -9999
- Species Table (CP_Fish_SpeciesTable.csv)
  - Fish_SpeciesCode, EA_SpeciesCode, Latin_Name, Common_Name
- NFPD Data Table (CP_Fish_DataTable_region)
  - Fish_SiteID, Fish_SurveyID, Fish_Easting, Fish_Northing
  - Fish_SurveyDate,Fish_SpeciesCode, Fish_Densities
  - HQS_Bt_Small, HQS_Bt_Med, HQS_Bt_Large, HQS_Sal_Small, HQS_Sal_Large
  - GSI, NAOI, Degree_Days
  - (HV: habitat covariates)
- Hydrology Stats (CP_Fish_HydrologyStats_Region.csv)
  - RF_Matched_Feature_ID, alternate flow stats (means, quantiles, CV, etc.)
  - Period statistics (RF_Mean, RF_Q50, RF_STD, RF_COV, RF_Q5_Mean, RF_Q95_Mean)
  - Threshold statistics (3M/6M/12M, precper/POI, 5/25/75/95 percentiles, threshold/duration_exceeded/n_exceedences/avg_patch_length)
- Land Cover (ENG_Fish_LC2015.csv)
  - SITE_ID, full_easting, full_northing
  - Perc_woodlands, Perc_arable, Perc_seminatural, Perc_urban
  - Area_sq_km_woodlands, Area_sq_km_arable, Area_sq_km_seminatural, Area_sq_km_urban
- RHS Scores (RHS scores_V2.xls)
  - Fish Site, RHS_Survey, RHS_SiteID, X, Y, SurveyDate, HMS Score/Class, Habitat Quality Assessment
- HABSCORE (HABSCORE data)
  - Site-specific HQS per species/size; data often incomplete due to access limitations
- EDF (CP_0101_FISH_England_keys_v1_figures.csv)
  - EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95, ED_SITE_ID, SITE_ID
- Deg Days (NFPD_CumulativeDegreeDays.csv)
  - SiteID, SurveyDate, Date_1, Deg_days
- Water Quality Determinand (WIMS and DET files)
  - WIMS region files; includes W1_SMPT_REF, LOQ handling (Min_LOQ, Max_LOQ, Median/Mean/Std LOQ options), WQ_Counts
  - Selected WQ determinand sites by ArcGIS near match; computed 12-month statistics prior to survey
- GSI and NAOI
  - Gulf Stream Index (Year, Annual)
  - NAOI (Year, Annual)

## Tools, code and software used

- GIS and spatial processing
  - ArcGIS (versions 10.6.1 or later, Pro) for land cover processing, hydrology matching, RHS matching, and near-site selections.
  - IRN extension in ArcGIS for RHS–fish site matching within 5 km.
  - GRASS GIS (for land cover raster processing) and QGIS (as needed).
- Scripting and statistical modelling
  - Python 3.x (for extraction, data wrangling, LOQ handling, and EDF/water quality data processing).
  - R (R Studio) for GAMM modelling of water temperature; degree-day computations; model selection; temperature predictions.
- Data management and processing notes
  - Excel used for initial data processing and organization of some source files.
  - DataLab Python workflows used for land cover extraction and categorization steps.
  - Documentation notes emphasize data provenance, matching criteria, and potential gaps.

## Data notes, caveats and quality considerations

- Spatial alignment and matching
  - Differences can exist between coordinates in different tables (Fish_Easting/Northing vs DataTable coordinates); location accuracy varies by data source.
  - RHS–fish site matching uses a 5 km river-network distance constraint; some fish sites may have no suitable RHS match (treated as no data).
- Data completeness and access
  - HABSCORE data availability varies by region; not all sites can be matched to HABSCORE results.
  - Some WQ determininand sites are license-restricted and excluded from the final dataset.
- Data processing assumptions
  - Fish counts converted to densities using area conversions; semi-quantitative and first-catch data treated separately due to sampling-effort differences.
  - Logarithmic-scale abundances converted using mid-points; present and “survey” suffixes interpreted with pre-defined rules.
  - EDF relies on selected reach data with 95% catchment contribution; ties are handled to assign EDF values; missing network data leads to blanks.
- Temperature and hydrology modelling
  - Temperature predictions are stratified by BFI; separate GAMMs for chalk/high groundwater bodies; model selection based on standard error metrics.
  - Degree days are computed for the year prior to each survey date and used to assess growth/recruitment potential.
- Climate indicators
  - GSI and NAOI are annual means; high natural variability can affect year-to-year linkages with river conditions.
- Documentation and reproducibility
  - The workflow describes explicit steps, data sources, and software versions to enable reproduction and auditing of the dataset.

## Access and reference points

- Fish data sources and NFPD references:
  - NFPD freshwater fish survey relational datasets: https://data.gov.uk/dataset/d129b21c-9e59-4913-91d2-82faef1862dd/nfpd-freshwater-fish-survey-relational-datasets
- Water quality and EDF modelling:
  - UK Environment Agency Water Quality Data Archive: https://environment.data.gov.uk/water-quality/view/landing
  - LF2000-WQX model references (Williams et al., 2009)
- Land cover and IHDTM:
  - UKCEH Land Cover Map 2015 and IHDTM data
- Climate indices:
  - Gulf Stream Index (GSI) data: Plymouth Marine Laboratory
  - NAOI data: NCAR Climate Data Guide
- Species and site metadata
  - EA NFPD datasets and site tables (as referenced within the document)
- Habitat surveys and RHS
  - River Habitat Survey documentation and resources: http://www.riverhabitatsurvey.org/rhs-doc/habitat-assessment/