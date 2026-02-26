Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018

## Overview
- A comprehensive, open data product combining macroinvertebrate abundance at 1,519 English river monitoring sites (1965–2018) with 41 water quality determinands, river flow, air temperature, and static environmental site descriptors.
- Datasets assembled from Environment Agency (EA) biosys, EA Water Quality Data Archive, NRFA, UKCEH CHESS-met, LF2000-WQX wastewater effluent model, RHS habitat data, and Land Cover Map 2015 (LCM2015).
- Aimed to enable environmental data analysis and modelling (ChemPop project) by providing harmonised, analysis-ready CSV files with metadata and methodological documentation.
- Noted challenges include non-standardised historic formats, data gaps, licensing restrictions, and scale mismatches.

## Data Components

### Macroinvertebrate abundance
- Time series for 1,519 sampling sites across seven EA regions (1965–2018).
- Taxonomic data include order, family, genus/species names, and abundance counts (semi-quantitative before 2002, numeric counts from 2002 onward).
- Files per region:
  - CP_<REGION>_MInv_taxonAbundance_<startDate-endDate>.csv
- Site descriptors corresponding to macroinvertebrate sites stored separately.

### Water quality determinands
- 41 chemical determinands, with measurements linked to macroinvertebrate sites for the preceding 6 months.
- Data sources: EA Water Quality Archive (from 2000 onward) and pre-2000 EA licensed data.
- Handling of values below LoQ and above upper measurement limit via three treatment configurations (LoQ1/LoQ2/LoQ3 and upper-limit handling).
- Statistics computed per macroinvertebrate sampling date:
  - Min, Max, Median, Mean, Standard Deviation
  - Totals: number of samples, and counts below LoQ / above upper limit
- Files per region:
  - CP_<REGION>_MInv_<determinandLabel>Stats_<startDate-endDate>.csv
- Data quality notes: some sites excluded due to licensing restrictions or missing data.

### River flow
- Daily mean river flow data from NRFA, matched to macroinvertebrate sites by nearest river-network distance.
- Time span aligned with macroinvertebrate dates and the broader period of interest (POI: 20/05/1974–29/03/2019).
- Statistics per site:
  - Mean, Median, SD, Coefficient of Variation (CV)
  - Q5/Mean and Q95/Mean (quantile-based metrics)
  - 6-month pre-sampling period statistics (using Indicators of Hydrologic Alteration methods): thresholds at multiple quantiles, exceedances, patch lengths, and durations.
- Files per region:
  - CP_<REGION>_MInv_riverFlowStats_<startDate-endDate>.csv

### Air temperature
- Daily mean air temperature at macroinvertebrate sites, derived from CHESS-met (1961–2017).
- Time windows aligned to macroinvertebrate sampling dates; statistics computed for the 6 months before each sample.
- Limitations: CHESS-met ends in 2017; no data beyond that for pairing with post-2017 samples.
- Files per region:
  - CP_<REGION>_MInv_airTempStats_<startDate-endDate>.csv

### Habitat quality (RHS)
- River Habitat Survey (RHS) site descriptors linked to macroinvertebrate sites within 5 km along the river.
- Indices used:
  - Habitat Modification Score (HMS) and HMS_Class
  - Resectioned Bank/Bed SubScore (RSB_SubScore)
  - Habitat Quality Assessment Score (HQA) and adjusted (HQA_ADJ)
- RHS provides single measurements per site (with a small subset having multiple RHS surveys).
- Site descriptors stored in:
  - CP_<REGION>_MInv_siteVariables.csv
- Habitat data provide context on physical modification and habitat quality for ecological interpretation.

### Land cover
- Upstream catchment land cover derived from Land Cover Map 2015 (LCM2015), aggregated to four broad categories: Woodlands, Arable, Seminatural, Urban.
- Processing used IHDTM flow direction grids and 50 m cells; catchment upstream area delineation used flow accumulation thresholds.
- All macroinvertebrate sites have matched land cover data; values stored in site descriptor files.

### Environmental site descriptors (EDF and related)
- Wastewater effluent exposure modeled as EDF (percentage wastewater) using LF2000-WQX.
- EDF data linked to macroinvertebrate sites and stored in site descriptor files (CP_<REGION>_MInv_siteVariables.csv) with EDF summary statistics (mean, 90th/95th percentile, standard deviation).
- EDF limitations: calibration is conservative; smaller WWTWs may be omitted; some headwater sites may show NA where truncated network geometry excludes minor contributors.

## Data Integration and Processing

### Workflow and approach
- Ecology and GIS expertise combined with spatial data analysis to harmonise national-scale monitoring data with geospatial covariates.
- Three-step integration:
  1) Spatial matching: nearest matching along the river network between macroinvertebrate sites and environmental sampling sites (WQ, RF, RHS).
  2) Spatial integration: extraction of model- and analysis-generated variables (EDF, land cover, air temperature) at macroinvertebrate site locations.
  3) Temporal matching: alignment of environmental observations with macroinvertebrate sampling dates; use 6-month window preceding sample dates for time-series covariates.

### Data sources (key aspects)
- Macroinvertebrates: EA Biosys FRMS data (1965–2018).
- Water quality: EA Water Quality Archive; pre-2000 data from EA licensed EA data store.
- River flow: NRFA gauging data; GAUGE network with quality checks (≤50% missing data).
- Temperature: CHESS-met daily meteorology (1961–2017).
- Habitat: RHS data (1994–present); static RHS metrics linked to macroinvertebrate sites.
- Land cover: LCM2015; catchment extraction and validation performed in GIS and Python pipelines.
- Data processing tools: ArcGIS IRN extension, ArcGIS, GRASS GIS, Python (Pandas, NumPy, Xarray), NetworkX, and Linux scripting for data extraction.

### Quality checks and caveats
- Harmonisation required balancing thoroughness with resource limits; some data remain with gaps or non-standard formats.
- Land cover mapped as static due to resource intensity of time-varying versions.
- EDF matching can yield NA values when the truncated network omits upstream areas; 0% EDF does not guarantee absence of wastewater influence.
- Water quality data pre-2000 licensed data may have lower completeness and QA compared with Water Quality Archive data post-2000.
- CHESS-met end date (2017) limits post-2017 temperature covariate availability.
- RHS provides predominantly single-point data per site; some sites have multiple RHS surveys.

## Outputs and File Structure

- Site descriptors (regionally split):
  - CP_<REGION>_MInv_siteVariables.csv
  - Columns include BIO_SITE_ID, altitude, slope, distance from source, channel width/depth, substrate proportions, EDF, land cover percentages, and other descriptors.
- Taxon abundance (regionally split):
  - CP_<REGION>_MInv_taxonAbundance_<startDate-endDate>.csv
  - Columns include BIO_SITE_ID, BIO_SAMPLE_ID, BIO_SAMPLE_DATE, BIO_FAM_NAME, BIO_SPGRP_NAME, BIO_ABUNDANCE, etc.
- Water quality statistics (per determinand, regionally split):
  - CP_<REGION>_MInv_<determinandLabel>Stats_<startDate-endDate>.csv
  - Stats include WQ_MIN_LOQ#, WQ_MAX_LOQ#, WQ_MEAN_LOQ#, WQMed, WQ_STD, WQ_COUNT, WQ_COUNT_LOQ, WQ_COUNT_GLOQ, etc., with LoQ handling variants.
- River flow statistics:
  - CP_<REGION>_MInv_riverFlowStats_<startDate-endDate>.csv
  - Includes RF_MEAN_POI, RF_Q50_POI, RF_STD_POI, CV, and IHA-derived metrics for 6-month periods prior to samples and over the POI.
- Air temperature statistics:
  - CP_<REGION>_MInv_airTempStats_<startDate-endDate>.csv
  - Contains TAS_MIN, TAS_MAX, TAS_MEAN, TAS_STD, TAS_MEDIAN for the 6-month windows.
- Location mappings:
  - CP_<REGION>_MInv_siteMatchedLocation.csv
  - Provides coordinates and metadata for macroinvertebrate sites and their matched WQ/RF/RHS sites.
- Heatmaps (Appendix 4): heatmaps illustrating temporal coverage and data completeness for each covariate and region.
- Supporting files (Appendix-related): additional RHS sites with multiple surveys, and water quality discrepancy tables (A.3.1, A.3.2).

## Data Accessibility and Usage

- Intended for open data use within environmental science, ecological modelling, and policy-oriented analyses.
- Datasets documented with extensive methodology and provenance; users should consult the accompanying documentation for suitability, data limitations, and methodological choices.
- Data sources and licensing acknowledged; primary data owners include EA, UKCEH, NRFA, and CHESS-met collaborators.

## Author Contributions and Acknowledgements

- Development of data analysis protocols, data management, cleaning, extraction, and documentation performed by a multidisciplinary team.
- Acknowledges EA, UKCEH, NRFA data, and contributors who assisted with technical support and data deposit processes.
- Funding and project context: ChemPop (ERCITE), supported by NERC NE/S000100/1.