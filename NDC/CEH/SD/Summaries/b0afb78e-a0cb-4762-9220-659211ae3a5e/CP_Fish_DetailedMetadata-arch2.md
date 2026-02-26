# Data output supporting information document

- A comprehensive open data product from ChemPop WP1 detailing a time‑series dataset of fish abundance, habitat, water quality, flow and climate variables in English rivers (1975–2017) for 1180 fish sites, linked by a unique site identifier and complemented by covariates and regional splits.

## Aim and scope (Analysts’ perspective)
- Demonstrates environmental condition in a consistent, scrutinisable format for temporal health and policy performance.
- Provides standardized outputs (fish abundances, covariates, and derived metrics) for open modelling and environmental assessment.
- Highlights data provenance, quality assurance steps, and explicit processing workflows to enable reuse and integration with other datasets.

## Dataset content and structure
- Time series of species-specific fish abundances with covariates for 1180 English river sites; sites require at least 10 annual fish surveys (1975–2017) from the National Fish Population Database (NFPD).
- Covariates include: habitat quality (RHS, HABSCORE, HMS, HQA), land use (Land Cover Map 2015), wastewater concentration (EDF), altitude, climatic variables (GSI, NAOI), water temperature (Degree Days), river discharge, and chemical determinants.
- Data organized into multiple linked tables, regionally split (Anglian, Midlands, Northeast, Northwest, Southern, Southwest, Thames) and accompanied by data management files describing collection/processing.
- Primary data outputs and data tables:
  - NFPD Fish Data Table (site, survey, species, densities, HQS/HQS-type habitat covariates)
  - Fish Site Table (site coordinates, covariates, region-specific variables)
  - Fish Species Table (Chempop vs EA species codes)
  - Hydrology Stats (per-site river flow metrics; includes RF_Matched_Feature_ID)
  - Land Cover (percentage and area upstream of each site for 4 macro-categories)
  - RHS/HMS/HQA (habitat metrics matched to fish sites)
  - HABSCORE (habitat quality scores for salmon/trout life stages)
  - WIMs Data (chemical determinants by site/date; 41 determinands)
  - EDF (Effluent Dilution Factor per site)
  - Altitude (IHDTM-based elevations)
  - Climatic covariates (GSI, NAOI)
  - Degree Days (cumulative degree days over 12°C prior to survey)
  - Data dictionaries and notes

## Data sources and covariates
- Fish abundance and site data: Environment Agency’s National Fish Population Database (NFPD).
- Habitat metrics: River Habitat Survey (RHS; RHS, HMS, HQA), HABSCORE (Atlantic salmon and brown trout).
- Land cover: UKCEH Land Cover Map 2015.
- Water quality and chemical determinants: UK Water Quality Archive (41 determinands) and Region FISHWIMSStats DET files.
- Hydrology: UKCEH National River Flow Archive (NRFA); daily river flows and Base Flow Index (BFI).
- Water temperature: CHESS-Met (CEH/UK Met Office) for daily air temperature; gauged water temperature data; degree-day calculations.
- EDF (effluent dilution): LF2000-WQX model extension to estimate wastewater contributions (sites contributing to 95% of dry weather flow in a catchment).
- Altitude: UKCEH Integrated Hydrological Digital Terrain Model (IHDTM).
- Climate indices: Gulf Stream Index (GSI, Plymouth Marine Laboratory) and North Atlantic Oscillation Index (NAOI, NCAR dataset).
- Temporal scope: 1975–2017 (fish surveys and covariates aligned to ecologically relevant timeframes).

## Data processing workflow (end-to-end)

- Fish abundance (NFPD-based dataset)
  - Select sites with ≥10 surveys (1975–2017); remove juvenile-only datasets.
  - Convert raw fish counts to densities (per unit area) to standardize sampling effort.
  - Handle semi-quantitative and first-catch counts; apply processing steps for logarithmic scales to derive density estimates.
  - Harmonise species codes to Chempop codes; aggregate variants to one code per species when needed.
  - Document processing steps and convert to a site-centric data structure with a site table and per-survey data.

- River Habitat Survey (RHS) and HABSCORE
  - RHS: match RHS survey sites to fish sites within 5 km along the river using ArcGIS IRN extension; extract HMS and HQA scores for matched RHS sites.
  - HABSCORE: obtain HQS scores for salmon/trout life stages where available; acknowledge incomplete data coverage due to data access limitations.

- Land cover
  - Rasterize Land Cover Map 2015 to 50 m grid; align to IHDTM.
  - Use GRASS r.accumulate to create per-upstream-catchment raster layers by land cover type.
  - Extract percentages and areas upstream of each fish site; group 21 land cover categories into four macro-categories: Woodlands, Arable, Seminatural, Urban.
  - Validate aggregation to ~100% coverage per catchment.

- Water temperature
  - Obtain daily water temperature data from gauging stations (≥3 years of continuous data); supplement with CHESS-MET 1 km gridded air temperature data.
  - Compute deg days: cumulative degree days (days with water temperature ≥12°C) for the year prior to each survey.
  - Model water temperature with GAMMs stratified by Base Flow Index (BFI) ranges (0.3–0.99; seven bands). Use Model 1 (month, time, air temperature) as the best-performing structure, with ARMA error structures.
  - Predict site-specific water temperatures; convert to degree days for the year prior to survey dates.

- Hydrology
  - Snap NRFA gauging stations to the river network; assign distance along the river between each fish site and nearest gauging station.
  - Extract 3, 6, 12-month summary statistics prior to each survey; manual GIS checks to confirm nearest-station matches.
  - Use as potential explanatory variables for fish densities.

- EDF (Effluent Dilution Factor)
  - Apply LF2000-WQX model; select significant wastewater treatment works (WWTWs) contributing to 95% of catchment DWF.
  - Link each biota site to the closest reach on the model river network; if distance ties occur, assign the corresponding EDF value.
  - Produce EDF summary metrics: mean, standard deviation, 90th and 95th percentiles (EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95).

- Water quality determinands
  - Match fish sites to the nearest three chemical determinand sites using ArcGIS Near Table; apply suitability filters (sampling frequency, inter-site connectivity, time overlap, river size, etc.).
  - Extract 41 chemical determinands from EA Water Quality Data Archive; align to 12-month pre-survey window where possible.
  - Apply data quality checks (maximum thresholds for metals, LOQ handling scenarios); compute summary statistics for the antecedent period; remove licensing-restricted sites from final dataset.

- Altitude
  - Extract site elevations from IHDTM using the centre of each IHDTM cell for fish site coordinates.

- Climatic covariates
  - Gulf Stream Index (GSI): annual mean values (1975–2017) sourced from Plymouth Marine Laboratory.
  - North Atlantic Oscillation Index (NAOI): annual values (1975–2017) from NCAR climate data guide.
  - Include annual covariates per site/year; align to fish survey timing.

- Data assembly and outputs
  - Combine site information, abundance data, and covariates into region-specific data structures.
  - Provide accompanying metadata, notes on data provenance, and data processing workflows for reproducibility.

## Tools, code and workflows
- Software used: ArcGIS (various versions), Excel, Python 3.x, R (R Studio), GRASS GIS, GRASS, GRASS r.accumulate, DataLab notebooks.
- Key processing steps mapped to workflows:
  - Matching and linking sites (RHS, NRFA, WQ determinands, EDF) via GIS operations and river networks.
  - Data transformations (densities from counts; handling of semi-quantitative and catch-based data).
  - Modelling: GAMMs for water temperature; degree-day calculations; QA/QC steps for LOQ and thresholds.
- Codes and scripts are provided in project documentation (Python and R scripts for temperature modelling, degree-day calculations, and data extraction).

## Outputs, files and data availability
- Data outputs are organized by dataset type and region, with named files such as:
  - CP_Fish_DataTable_Region.csv
  - CP_Fish_SiteVariables_Region.csv
  - CP_Fish_SpeciesTable
  - CP_Fish_HydrologyStats_Region.csv
  - Region_FISHWIMSStats_DET.csv (41 determinands per region)
  - ENG_Fish_LC2015.csv (Land Cover 2015)
  - 20200622_NFPD_Fish_England_PrioritySitesOnly_SiteTablewithBFI.csv
  - GSI and NAOI data files
  - EDF_CP outputs (EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95)
  - Cumulative degree days (Deg_days) files
- Output structure supports cross-dataset linkage via unique site identifiers; region-specific datasets enable scalable analyses and policy monitoring.

## Data quality, limitations and notes
- Some RHS/HABSCORE data may be incomplete due to data access constraints; HABSCORE data are regional and sometimes not fully alignable to Chempop fish sites.
- Spatial matching relies on nearest-site approaches along river networks; some fish sites may lack proximate RHS data within 5 km.
- Land cover aggregation achieves approximately 100% downstream catchment coverage, though rasterization and alignment choices may introduce minor discrepancies.
- Differences between Fish_Easting/Northing values across site and data tables are acknowledged; exact survey locations may vary slightly.
- LOQ handling decisions and licensing restrictions affect determinant data inclusion; some WQ determinand sites are omitted in final datasets.

## Relevance for environmental monitoring and policy analysis
- The dataset provides a harmonised, auditable foundation for tracking environmental health over 1975–2017 in English rivers and supports modelling of fish populations under habitat, hydrological, water quality, and climatic drivers.
- By exposing data lineage, processing steps, and modelling choices, the work enables robust evaluations of environmental policy performance and the integration of these data into broader environmental health dashboards and analyses.