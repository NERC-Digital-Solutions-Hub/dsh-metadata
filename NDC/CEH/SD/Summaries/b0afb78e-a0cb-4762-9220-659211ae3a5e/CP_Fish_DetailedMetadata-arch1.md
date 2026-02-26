# Data output supporting information document

- Comprehensive, time-series dataset of fish abundances and environmental covariates for English rivers (1975–2017), developed under the ChemPop WP1 project.
- Aimed at enabling data-driven analyses of how habitat, water quality, flow, and climate influence fish populations.

## Overview of the dataset

- Time series of species-specific fish abundances and covariates for 1180 English river sites.
- Site selection: only sites with at least ten annual surveys in Environment Agency’s National Fish Population Database (NFPD) between 1975–2017.
- Covariates include: habitat quality (RHS, HABSCORE), land use, wastewater content (EDF), altitude; time-bound covariates include fish abundances, climate indices (Gulf Stream Index, NAOI), water temperature (degree days), river discharge, and 41 chemical determinands.
- Structured as multiple linked tables, regionally partitioned (Anglian, Midlands, Northeast, Northwest, Southern, Southwest, Thames) and accompanied by data management and processing files.

## Core data components and structure

- Main datasets and tables
  - CP_Fish_DataTable: site-level fish survey data and densities by species.
  - CP_Fish_SiteTable: site metadata (location, covariates such as RHS/HABSCORE, land cover, altitude).
  - CP_Fish_SpeciesTable: species codes and Latin/EA names.
  - CP_Fish_HydrologyStats_Region: hydrology statistics by site and survey.
  - CP_Fish_ChemicalDeterminand: region-specific chemical determinands.
  - Region-specific files for each data type (e.g., CP_Fish_DataTable_Region.csv, CP_Fish_SiteVariables_Region.csv, Region_FISHWIMSStats_DET.csv).
- Data sources and covariates
  - Fish abundance: National Fish Population Database (NFPD, EA).
  - Habitat metrics: River Habitat Survey (RHS) and HABSCORE (EA/University of Hull).
  - Land cover: Land Cover Map 2015 (UKCEH).
  - Hydrology and climate: Base Flow Index (BFI) from NRFA; Degree Days; Gulf Stream Index (GSI); NAOI; CHESS-MET air temperature data.
  - Water quality and effluent: Water Quality Archive; LF2000/WQX-based effluent dilution factor (EDF) estimates.
  - Altitude: UKCEH Integrated Hydrological Digital Terrain Model (IHDTM).

## Data sources and covariates in detail

- Fish abundance data
  - Source: NFPD, EA; files include Freshwater Fish Counts (all species) and Salmonid age-bands.
  - Processing: sites with ≥10 surveys; juvenile sites removed; raw counts converted to densities; semi-quantitative data used where appropriate; handling of logarithmic abundance scales; unify to single Chempop species codes.
- Habitat and habitat-quality covariates
  - RHS: habitat type and site matching; HMS (Habitat Modification Score) and HQA (Habitat Quality Assessment) values matched to fish sites via ArcGIS IRN extension within 5 km.
  - HABSCORE: habitat quality scores for salmon/trout size classes; data requested from EA offices; not available for all sites due to data access limitations.
- Land cover
  - Upslope land cover upstream of fish sites calculated from LCM 2015; processed with ArcGIS/GRASS/QGIS and Python to derive four macro-categories (Woodlands, Arable, Seminatural, Urban) and their areas (km²).
- Water temperature
  - Degree days: modeled as cumulative days with water temperature ≥12°C in the year prior to each survey.
  - Modeling: GAMM-based temperature predictions stratified by BFI (0.1 increments); CHESS-MET air temperature data used as inputs; long-term, site-specific temperature estimates used to compute degree days.
- Hydrology
  - Data: NRFA daily discharge data; matched to fish sites with river-network snapping; 3-, 6-, and 12-month antecedent periods extracted; distances between sites and gauging stations calculated along river network; manual checks performed to ensure accurate matches.
- Effluent dilution factor (EDF)
  - Based on LF2000-WQX model; only significant WWTWs (covering 95% of dry-weather flow) included.
  - Process: nearest river reaches assigned to fish sites; EDF values aggregated to EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95.
- Water quality determinands
  - 41 determinands extracted from EA Water Quality Data Archive; nearest three determinand sites considered; matching criteria include sampling frequency, temporal overlap with fish surveys (±2 years allowed), proximity, and absence of intervening sewage works when not appropriate.
  - Data processing includes handling below LOQ values (various LOQ schemes) and QA steps; some determinands removed due to licensing restrictions.
- Altitude
  - Elevation at fish sites derived from IHDTM; altitude values assigned via Extract Multi Values to Points in ArcGIS.
- Climatic variables
  - Gulf Stream Index (GSI): annual mean values (GSI data sourced from Plymouth Marine Laboratory).
  - North Atlantic Oscillation Index (NAOI): annual values (NCAR data).
  - Data limited to 1975–2017; used as covariates to capture climatic context.

## Data processing workflows (highlights)

- Fish abundance workflow
  - Download Freshwater Fish Counts from NFPD; retain sites with ≥10 surveys (1975–2017).
  - Remove juvenile-only sites; convert counts to densities; exclude surveys without sampling effort or with unclear counts.
  - Normalize abundance data when counts are provided as ranges or logarithmic categories by applying midpoints or defined rules; map to Chempop species codes; sum densities when multiple EA codes map to a single Chempop code.
  - Retain surveys with zero catches to preserve sampling effort.
- River Habitat Survey (RHS) workflow
  - Align RHS site locations with fish sites using ArcGIS IRN to locate nearest RHS site within 5 km along the river.
  - Extract HMS and HQA values for matched RHS sites; adjust 1994 RHS data via harmonized flow-type and vegetation rules to enable comparability.
- HABSCORE workflow
  - Request and integrate regionally stored HABSCORE data; not always fully matchable to chempop fish sites due to data availability.
- Land cover workflow
  - Rasterize Land Cover Map 2015 to 50 m cells; compute proportion of each land-cover type upstream of each fish site via IHDTM alignment and GRASS r.accumulate; group into four macro-categories; verify total coverage approaches 100%.
- Water temperature workflow
  - Collect long-term water-temperature gauging data; extract daily mean air temperature (CHESS-MET) for fish sites and gauging stations; compute degree days (≥12°C) for the year prior to each survey.
  - Fit GAMMs for temperature with stratification by BFIs; assess model performance with RMSE, normalized RMSE, and scatter index; select best models per BFI range to predict site-specific water temperature.
- Hydrology workflow
  - Snap NRFA gauging stations to river network; compute river-path distances to fish sites; extract 3-, 6-, and 12-month discharge statistics; manually validate matches.
- EDF workflow
  - Apply LF2000-WQX to identify significant WWTWs (top contributors); associate fish sites to nearest 1:50,000 river network reach; assign EDF values, with blank where data gaps exist; report EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95.
- Water quality determinands workflow
  - Use ArcGIS Near Table to identify the nearest three chemical determinand sites to each fish site; manual suitability checks (sampling frequency, absence of intervening sewage works, overlapping timeframes, reasonable river size/dilution) before data extraction.
  - Extract 41 chemical determinand values for the antecedent 12 months; apply LOQ handling and QA thresholds; exclude determinands with licensing restrictions.
- Altitude workflow
  - Use ArcGIS Extract Multi Values to Points to fetch IHDTM-based altitude at each fish site.
- Climatic covariates workflow
  - Retrieve annual GSI and NAOI values; extract relevant years; align with fish survey dates.

## Data notes and limitations

- Data gaps and access issues
  - HABSCORE data availability is uneven; not all sites can be matched to HABSCORE data.
  - Some location coordinates differ slightly between Fish SiteTable and DataTable due to survey location variation.
  - Licensing restrictions caused removal of some chemical determinand data from the final dataset.
- Data integration challenges
  - Matching covariates from disparate sources required spatial proximity along the river network and careful temporal alignment.
  - Stratification by hydrological regime (BFI) was necessary to account for varying temperature regimes (e.g., chalk/high groundwater rivers).
- Model usage
  - No predictive models were created directly for this output; the data provide inputs for analyses and modelling elsewhere (e.g., GAMMs for temperature, EDF-based exposure measures).

## Practical uptake for analysts

- The dataset provides a richly linked, regionally structured set of fish densities and a broad suite of ecological covariates across four decades.
- Key tables to join for analysis:
  - NFPD-based fish densities (CP_Fish_DataTable_region, Fish_SiteID, Fish_SurveyDate, Fish_SpeciesCode, Fish_Densities).
  - Site covariates (CP_Fish_SiteTable_region; RHS/HMS/HQA, land-cover upstream metrics, altitude, BFI).
  - Hydrology and climate covariates (CP_Fish_HydrologyStats_Region, WIMS/FISHWIMSStats_DET, CHESS-MET-derived temperature, NRFA-derived discharge, GSI, NAOI, Degree_Days).
  - EDF and water quality determinands (EDF CSVs and 41 WQ determinands from the Water Quality Archive).
- Use cases include assessing temporal trends in fish communities, evaluating habitat and water-quality drivers, or informing management actions with integrated habitat–climate–pollution covariates.