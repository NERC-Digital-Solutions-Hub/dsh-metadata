# Data output supporting information document

- The dataset supports the ChemPop WP1 work on Fish abundance, habitat, water quality, flow and climate in English rivers from 1975-2017.
- It compiles fish abundance time series and covariates across English rivers, linking multiple data sources into a single open data product for environmental data and modelling analyses.

## Aim and scope (Data Steward perspective)

- Provides a time-resolved, site-based dataset to enable discovery, reuse and modelling of fish populations and their environmental drivers.
- Integrates governance-relevant elements: provenance, metadata, cross-dataset linking, and documentation of processing steps.
- Addresses data governance challenges such as disparate data formats, variable site matching, and data availability limitations.

## Key data components and coverage

- Fish abundance data
  - Time series of species-specific abundances and covariates for 1,180 sites (English rivers), 1975–2017.
  - Source: Environment Agency National Fish Population Database (NFPD); open data portal.
  - Selection: sites with ≥10 annual surveys (1975–2017); juvenile-only sites removed.
  - Covariates: habitat (RHS, HABSCORE), land use, wastewater content, altitude; climate (GSI, NAOI); water temperature (degree days); river discharge.
  - Structure: linked by a unique fish site identifier; region-specific files.
  - Processing: counts converted to densities; semi-quantitative data used with first-catch handling rules; species codes harmonised to ChemPop codes; multiple EA species codes reconciled; data retained even when no fish were captured to preserve sampling effort.

- River Habitat Survey (RHS) and habitat quality
  - RHS provides Habitat Modification Score (HMS) and Habitat Quality Assessment (HQA).
  - HMS/HQA matched to fish sites within 5 km along the river network using ArcGIS IRN extension.
  - HABSCORE data (habitat quality for salmon/trout) included where available; limited by data availability.

- Land cover
  - Upstream catchment land cover (woodlands, arable, semi-natural, urban) derived from Land Cover Map 2015.
  - Outputs: percentages and areas (km^2) upstream of each fish site; macro-categories aggregated for analysis.
  - Tools: ArcGIS, Python; Lands cover raster processing and catchment extraction.

- Water temperature
  - Temperature driver: degree days (days with water temperature ≥12°C in the prior year).
  - Data sources: water temperature gauging stations (CEH/EA) supplemented by CHESS-Met; baseflow index (BFI) used to stratify models.
  - Modelling: Generalised Additive Mixed Models (GAMMs) with a separate model for each 0.1 BFI range (0.3–0.99); model selection via RMSE, normalised RMSE, scatter index.
  - Outputs: predicted water temperature and cumulative degree days per survey date.

- Hydrology (river flow)
  - Daily flow data from NRFA, matched to fish sites and used to derive 3-, 6-, and 12-month flow statistics prior to surveys.
  - Distance-based nearest-flow-gauge matching along the river network; manual checks for mismatches.

- Effluent Dilution Factor (EDF)
  - Estimation of wastewater contribution to river flows (EDF) using LF2000-WQX model.
  - Approach: associate each fish site to the nearest reach of the 1:50,000 river network; include WWTWs contributing to 95% of dry-weather flow.
  - Outputs: EDF_Mn, EDF_SD, EDF_Q90, EDF_Q95, with blanks for gaps or discrepancies.

- Water quality determinands
  - 41 chemical determinands (1960–2017) from EA Water Quality Archive.
  - Site matching: fish sites matched to nearest three chemical determinand sites; manual curation based on sampling frequency, timing overlap, and proximity.
  - Data handling: LOQ treatment options (LoQ, LoQ/2, 0) and maximum thresholds for some metals; summary statistics computed for 12 months prior to fish surveys.
  - Exclusions: some determinand sites removed due to licensing or licensing-related restrictions.

- Altitude
  - Elevation data for fish sites derived from the UKCEH Integrated Hydrological Digital Terrain Model (IHDTM).
  - Extraction via ArcGIS Extract multi-values-to-points.

- Climatic covariates
  - Gulf Stream Index (GSI): annual mean values (UK data).
  - North Atlantic Oscillation Index (NAOI): annual values.
  - Data sources: Plymouth Marine Laboratory (GSI) and NCAR Climatedataguide (NAOI); annual values used due to high monthly variability.

## Data structure and documentation

- Core data tables and files (regionally segmented)
  - Fish data and metadata
    - CP_Fish_DataTable (region-specific)
    - CP_Fish_SiteTable (region-specific)
    - CP_Fish_SpeciesTable
  - RHS and habitat
    - RHS scores_V2.xls
  - Land cover
    ENG_Fish_LC2015.csv
  - Hydrology
    CP_Fish_HydrologyStats_Region.csv
  - EDF
    CP_0101_FISH_England_keys_v1_figures.csv
    EDF (ED_SITE_ID linkage)
  - Water quality determinants
    Data access via EA Water Quality Data Archive; determinants stored per region
  - Altitude
    20201110_NFPD_Fish_ENG_Altitude (Altitude_CC and Altitude_BI)
  - Climate covariates
    GSI (Gulf Stream Data.pdf)
    NAOI (NAOI_station_annual.txt)

- Data notes and caveats
  - Occasional coordinate differences between Fish_Easting/Northing in SiteTable vs DataTable.
  - Some RHS/HABSCORE data limited by availability; not all sites have matched RHS/HABSCORE data.
  - LOQ handling methods and threshold rules explicitly documented.
  - Some WQ determinand sites excluded due to licensing restrictions.
  - Exceedance and threshold definitions for hydrology statistics use standardized terminology.

## Data processing and workflow highlights (high-level)

- General approach
  - Download and harmonise multiple data sources; select relevant site subset; spatially align data to river network; temporally align covariates to ecologically meaningful windows; document processing steps and decision rules for reproducibility.
- Processing tools and languages
  - GIS: ArcGIS (versions 10.6–10.8.x) and ArcGIS Pro
  - Scripting: Python 3.x (data extraction, LOQ handling, matching), R (GAMMs, degree-day calculations)
  - Geospatial matching: IRN extension in ArcGIS for RHS–fish site matching; river network snapping for hydrology and EDF
- Documentation and reproducibility
  - Workflow steps are itemized per data component, with explicit step-wise descriptions from data ingestion to final covariate extraction.
  - Clear listing of models (e.g., GAMMs for water temperature) and no models created for other datasets; model details and code are referenced rather than embedded.

## Data governance, quality and disponibilty considerations

- Data provenance and lineage
  - Multiple data sources with explicit attribution and access points; site-level linkage keys (Fish_SiteID, etc.) enable traceability across tables.
- Data quality and cleaning rules
  - Transparent handling of semi-quantitative vs quantitative data; mid-point conversions for log-scale abundances; standardisation of species codes; LOQ handling policies; QA steps for matching WQ and hydrology data.
- Accessibility and licensing
  - Some data components (e.g., HABSCORE) require access from EA regions; licensing restrictions noted for certain water quality determinands.
  - EDF, WQ determinands, and other covariates are provided with explicit output variables and flags for missing data.
- Update and maintenance considerations
  - Dataset spans 1975–2017 for fish data; future updates would require re-running the defined workflows with updated NFPD, EA, and NRFA sources; documentation supports reproducibility for reprocessing.
- Challenges aligned with the Data Steward archetype
  - Harmonising data across many systems/formats and ensuring consistent metadata.
  - Handling incomplete or missing covariate data and aligning temporal windows.
  - Managing large, regionally partitioned datasets with complex matching (fish sites to RHS, flow gauges, determinand sites).

## Quick references and access points

- NFPD data: Environment Agency / UK data portal
  - Freshwater Fish Counts and related NFPD files (regionally linked)
- RHS/HABSCORE data: Environment Agency (EA) and River Habitat Survey documentation
- Land Cover Map 2015: UKCEH data catalog
- Water quality: Environment Agency Water Quality Data Archive
- Hydrology: UKCEH NRFA (National River Flow Archive)
- Temperature and climate covariates: CHESS-MET (UKCEH), GSI and NAOI data sources
- Altitude: IHDTM (UKCEH)
- Modelling and analysis tools: ArcGIS, Python, R with GAMMs

- Data-specific file examples (names appear in the document)
  - CP_Fish_DataTable_region.csv
  - CP_Fish_SiteVariables_Region.csv
  - CP_Fish_SpeciesTable.csv
  - RHS scores_V2.xls
  - ENG_Fish_LC2015.csv
  - 20201110_NFPD_Fish_ENG_Altitude
  - Region_FISHWIMSStats_DET.csv (WIMS)
  - Gulf Stream Index (GSI) and NAOI files
  - NFPD_CumulativeDegreeDays.csv
  - CP_0101_FISH_England_keys_v1_figures.csv
  - EDF (CP_0101_FISH_England_keys_v1_figures.csv)