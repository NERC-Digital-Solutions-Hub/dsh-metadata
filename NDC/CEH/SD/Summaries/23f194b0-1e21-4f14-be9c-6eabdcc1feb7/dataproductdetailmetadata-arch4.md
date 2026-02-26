# Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018

- A comprehensive open data product combining macroinvertebrate taxonomic abundance from 1,519 English river monitoring sites (1965–2018) with 41 water quality determinands, river flow, air temperature, and static site descriptors.
- Created to support environmental data analysis and modelling, originating from the ChemPop project (NERC-funded, 2018–2022) and intended for broad community use.
- Data assembled from multiple sources with varying formats and purposes, requiring harmonisation and quality checks; final outputs include gaps (noData) due to incomplete records.

## Context and purpose

- Macroinvertebrates serve as effective indicators of chemical and environmental stress due to short lifespans and rapid responses.
- English river monitoring has a long history, producing publicly available datasets (biota, chemistry, hydrology, habitat).
- The data product integrates diverse datasets to enable large-scale analyses of chemical exposure and wildlife responses, while acknowledging inherent non-standardisation and incomplete records.
- Users are encouraged to assess data suitability via provided methodology descriptions and quality checks.

## Scope and coverage

- 1519 macroinvertebrate monitoring sites across England; sampling dates span 1965–2018.
- Variables include:
  - Macroinvertebrate taxonomic abundance (time series, taxon-level data)
  - Water quality determinands (41 chemicals)
  - River flow (daily mean)
  - Air temperature (CHESS-met, daily means)
  - Habitat descriptors (RHS indices)
  - Land cover upstream of each site (LCM2015)
  - Site physical descriptors (altitude, slope, distance from source, channel width/depth, substrate)
  - Wastewater effluent exposure estimates (EDF) derived from LF2000-WQX
- Data delivered as CSV files (regionally partitioned by Environment Agency regions) with extensive metadata and documentation.

## Data integration and processing workflow

- Three core steps to align datasets with macroinvertebrate sites:
  - Spatial matching: link environmental sampling points (water chemistry, flow, habitat) to the nearest macroinvertebrate site along the river network.
  - Spatial integration: extract modelled/derived variables (EDF, land cover, air temperature) at macroinvertebrate locations.
  - Temporal matching: pair water quality and temperature time series with macroinvertebrate sampling dates, using six months prior to each sample.
- Data sourced from multiple repositories:
  - Macroinvertebrate time series and site variables from Freshwater river macroinvertebrate surveys (FRMS, Biosys) via Environment Agency
  - Water quality data from the EA Water Quality Data Archive and pre-2000 EA licensed database
  - River flow from the National River Flow Archive (NRFA)
  - Air temperature from CHESS-met (1961–2017)
  - EDF via LF2000-WQX model
  - Habitat quality from River Habitat Survey (RHS)
  - Land cover from Land Cover Map 2015 (LCM2015)
  - IHDTM-based catchment delineation and river network for spatial processing
- Data processing utilised GIS tools (ArcGIS, IHDTM), Python (Pandas, NumPy, Geopandas), and Linux scripting to generate region-specific descriptor files.

## Data sources and provenance

- Macroinvertebrate time series and site descriptors: FRMS (Biosys), Environment Agency
- Water quality chemistry: EA Water Quality Archive; pre-2000 EA licensed data
- River flow: NRFA (Gauged Daily Flow data)
- Air temperature: CHESS-met (Great Britain)
- EDF (wastewater exposure): LF2000-WQX model
- Habitat quality: River Habitat Survey (RHS)
- Land cover: Land Cover Map 2015 (GB)
- River topology: UKCEH digital river network; IHDTM flow direction/accumulation
- Ground truthing, methodological notes, and reproducibility guidance provided to aid assessment and reuse

## Data files and structure

- Site descriptors (7 regional files): CP_<REGION>_MInv_siteVariables.csv
  - Columns include BIO_SITE_ID, altitude, slope, distance from source, discharge, width, depth, substrate covers, EDF-related fields, etc.
- Macroinvertebrate taxa abundance ( regional split): CP_<REGION>_MInv_taxonAbundance_<startDate-endDate>.csv
- Water quality statistics (41 determinands, regional files): CP_<REGION>_MInv_<determinandLabel>Stats_<startDate-endDate>.csv
- River flow statistics (regional files): CP_<REGION>_MInv_riverFlowStats_<startDate-endDate>.csv
- Air temperature statistics (regional files): CP_<REGION>_MInv_airTempStats_<startDate-endDate>.csv
- Water quality and site matching/location data:
  - CP_<REGION>_MInv_siteMatchedLocation.csv
  - SiteswithmultipleRHSsurveys.csv (subset for RHS repeats)
- Data completeness: Appendix heatmaps show temporal completeness per variable; some macroinvertebrate sites lack water quality matches due to licensing or extraction issues.
- Data notes: NA used for missing values; LoQ handling options described for water chemistry statistics (LoQ1, LoQ2, LoQ3).

## Data quality, gaps, and limitations

- Incomplete data across variables due to historical licensing, data collection changes, and temporal coverage gaps.
- Water quality data pre-2000 required licensing data (not always complete or QA-checked to the same standard as post-2000 data).
- CHESS-met temperature data cease after 2017, limiting post-2017 temperature pairing.
- Land cover is treated as a static variable due to resource constraints in harmonising successive Land Cover Map products.
- Some macroinvertebrate sites lack matched water quality data; a small number have matched water quality data but lack chemistry measurements due to extraction issues.
- EDF modelling relies on a truncated river network and modelling assumptions; discrepancies may occur for headwater branches with small WWTWs.

## Access, usage, and governance

- Data is provided as an open data product intended for broad reuse; citations and acknowledgments included in documentation.
- Primary access routes include EA Ecology& Fish Data Explorer, UKCEH data platforms, NRFA API, and associated data repositories; licensing considerations documented.
- Clear guidance on how to parse and read CSV files (NA coding, data types) to preserve data integrity across languages (Python, R, etc.).
- The product is designed for cross-domain data integration and large-scale ecological modelling, with explicit documentation of methodology and data provenance to support governance and reproducibility.

## Appendices and supplementary notes (highlights)

- Appendix 1: List of 41 water quality determinands with codes, units, and file-labels.
- Appendix 3: Data discrepancies and exclusions (lists of macroinvertebrate sites without water quality matches and with failed extraction).
- Appendix 4: Heatmaps illustrating temporal distribution and data completeness for all covariates.
- Appendix 5–9: Author contributions, acknowledgments, and references to data sources and methodologies.

## Key takeaways for data leaders

- This data product exemplifies large-scale data integration across ecological, chemical, hydrological, and habitat domains to support data-driven decision making.
- Highlights the importance of transparent provenance, interoperability, and metadata when combining heterogeneous time-series data from multiple agencies.
- Demonstrates practical challenges in data standardisation, licensing, temporal alignment, and up-to-date coverage, informing strategy for data governance, licensing, and future harmonisation efforts.
- Provides a structured, reuse-friendly framework with region-specific outputs and detailed documentation to facilitate discoverability, replication, and cross-site analyses.