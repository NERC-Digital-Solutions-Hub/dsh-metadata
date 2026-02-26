# Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018

## Overview
- Open data product compiling long-term environmental monitoring data for England (1965–2018).
- Integrates macroinvertebrate taxonomic abundance at 1,519 sites with 41 water-quality determinands, river flow, air temperature, and static environmental site descriptors.
- Created to investigate chemical exposure effects on wildlife (ChemPop) and to enable broad environmental analyses and modelling.
- Data organized as CSV files with region-specific splits; designed for reuse and reproducibility.

## Data scope and purpose
- Macroinvertebrate time series spanning 1965–2018 across 1,519 sites.
- Associated covariates:
  - Water quality: 41 determinands (minimum, maximum, mean, median, standard deviation, counts; handling of values below LoQ and above measurement range).
  - River flow: daily mean flows with regional gauging-station matching; hydrology metrics for period of interest and 6 months prior to sampling.
  - Air temperature: daily mean values (CHESS-met) matched to sites; statistics over 6 months preceding each sample (CHESS-met ends 2017).
  - Habitat quality indices (RHS): HMS, HMS_Class, RSB_SubScore, HQA, HQA_ADJ; RHS data are a single-visit snapshot for most sites.
  - Land cover upstream: percentages and areas for woodland, arable, seminatural, and urban land cover (LCM2015) upstream of each site.
  - Effluent dilution factor (EDF): modelled percentage of wastewater in river flow using LF2000-WQX, with mean, 90th/95th percentiles, and standard deviation.
- Site descriptors: altitude, slope, distance from source, discharge category, width, depth, substrate, and catchment context.

## Data sources
- Macroinvertebrate time series: Freshwater river macroinvertebrate surveys (Biosys), Environment Agency (EA).
- Water quality data: EA Water Quality Data Archive (and pre-2000 EA licensed data).
- River flow data: National River Flow Archive (NRFA) gauging stations; EA network.
- Air temperature: CHESS-met meteorology dataset (Great Britain, 1961–2017).
- Habitat quality: River Habitat Survey (RHS) dataset.
- Land cover: Land Cover Map 2015 (LCM2015).
- River network and hydrological terrain: UKCEH digital river networks; Integrated Hydrological Digital Terrain Model (IHDTM).
- EDF modelling: LF2000-WQX model (lowFlows2000 WQX).

## Data integration approach
- Three-step integration process:
  - Spatial matching: pair macroinvertebrate sites with nearby water-quality, river-flow, and RHS data along the river network (nearest in river distance). Table-based regional counts provided.
  - Spatial integration: extract model/derived variables (EDF, land cover, air temperature) at macroinvertebrate sites.
  - Temporal matching: align time-series observations to the macroinvertebrate sampling date; aggregate covariates over the 6 months preceding sampling.
- FRMS macroinvertebrate data cleaning:
  - Relational CSVs per region (Site, Index, Taxa); taxonomic name harmonization against Davies & Edwards (2011) standard; update family/order columns.
  - Resolve duplicate sites, inconsistent IDs, and taxonomic name changes; replace implausible abundances with presence indicators; remove zero-abundance taxa.
- Water quality data processing:
  - Matched to macroinvertebrate sites via ArcGIS IRN extension; manual validation to ensure same river reach, no upstream wastewater inputs, and minimal tributaries between sites.
  - 41 determinands extracted for 2000–present; pre-2000 data sourced from EA licensed database with region-specific processing.
  - Below-LoQ handling: multiple configurations (LoQ, 0, LoQ/2) to compute min, max, median, mean, and s.d. across 6-month windows.
- River flow:
  - Nearest NRFA gauging station along the river network; 50% data completeness threshold for POI (1974–2019) included.
  - Hydrological statistics computed for POI and 6-month windows prior to sampling (e.g., mean, median, Q5/mean, Q95/mean, coefficient of variation, etc., plus Richter-based exceedance metrics).
- Air temperature:
  - CHESS-met daily means matched to macroinvertebrate sites; statistics computed for 6 months prior to sampling.
- Habitat quality (RHS):
  - HMS, HMS_Class, RSB_SubScore, HQA, HQA_ADJ extracted for RHS sites within 5 km of macroinvertebrate sites; RHS typically a single observation per site, with a separate file for multi-survey RHS sites.
- Land cover:
  - LCM2015 processed to compute upstream woodland, arable, seminatural, and urban cover and corresponding areas (km2) via IHDTM flow accumulation.
  - Catchment-level upstream statistics snapped to macroinvertebrate sites; 21 LCM classes aggregated into four broad categories.
- Data quality checks:
  - Distance thresholds, completeness checks, and aggregation validation (land-cover sums near 100%).

## Site descriptors and outputs
- Site descriptor files: CP_REGION_MInv_siteVariables.csv for each EA region; include:
  - BIO_SITE_ID, BIO_ALTITUDE, BIO_SLOPE, BIO_DIST_FROM_SOURCE, BIO_DISCHARGE, BIO_WIDTH, BIO_DEPTH, substrate covers (BOULDERS_COBBLES, PEBBLES_GRAVEL, SAND, SILT_CLAY), BIO_BASE_DATA_DATE, EDF-related fields, and land cover descriptors.
- Taxon abundance files: CP_REGION_MInv_taxonAbundance_startDate-endDate.csv per region.
- Water quality statistics: CP_REGION_MInv_<determinandLabel>Stats_startDate-endDate.csv (41 determinands across 7 regions; includes WQ_MIN_LOQ*, WQ_MAX_LOQ*, WQ_MEDIAN_LOQ*, WQ_MEAN_LOQ*, WQ_STD_LOQ*, WQ_COUNT and LOQ handling).
- River flow statistics: CP_REGION_MInv_riverFlowStats_startDate-endDate.csv (mean, medians, POI statistics, and exceedance metrics).
- Air temperature statistics: CP_REGION_MInv_airTempStats_startDate-endDate.csv (min, max, median, mean, std).
- RHS-derived variables: included as site descriptors; some RHS data provided in a dedicated extra file for sites with multiple RHS surveys (SiteswithmultipleRHSsurveys.csv).
- Location mappings: CP_REGION_MInv_siteMatchedLocation.csv containing matched coordinates and catchment/waterbody identifiers.

## Data quality and limitations
- Completeness varies by region and determinant; some water-quality sites are missing due to licensing restrictions or extraction failures.
- CHESS-met data ends in 2017; no temperature data beyond that date for matching sites.
- Land cover is treated as static due to resource constraints in harmonising successive LC maps.
- EDF data may be NA in headwaters where the truncated river network omits upstream WWTWs; smaller WWTWs may be omitted in the model.
- Some pre-2000 water-quality data had lower QA rigor than later archive data.
- All CSV files use NA for missing values; users should specify data types and missing-value handling when loading.

## Data accessibility and structure
- Data product and supporting information provide extensive metadata, file naming conventions, and appendix details (Appendix 1–4).
- File naming conventions clearly separate region codes and data types (site variables, taxon abundance, water quality stats, river flow stats, air temperature stats, and matched locations).
- Data sources and acknowledgments link to EA, UKCEH, NRFA, CHESS-met, and IHDTM resources; usage guided by contributing authors and institutions.

## Relevance for monitoring frameworks
- Demonstrates end-to-end assembly of a multi-variable, long-term environmental monitoring data product with:
  - Clear data provenance and governance (data sources, licensing considerations).
  - Spatial and temporal alignment strategies to combine heterogeneous datasets.
  - Derivation of covariates (EDF, upstream land cover, RHS indices) that are directly useful for policy evaluation and modelling.
  - Rigorous data cleaning and standardization of taxonomic nomenclature for comparability over time.
  - Transparent handling of data quality issues, gaps, and limitations.
- Provides a practical template for creating open, analysis-ready monitoring data products to inform policy decisions and future monitoring strategies.
- Highlights ongoing challenges for monitoring framers: data silos, metadata completeness, timely data access, and governance around data sharing and updates.

## Author contributions and acknowledgements (highlights)
- Development of data analysis protocols, data management, data acquisition, validation, and documentation performed by a multidisciplinary team.
- Acknowledges EA, UKCEH, NRFA data sources and their custodians; notes funding support from NERC and the ERCITE ChemPop program.