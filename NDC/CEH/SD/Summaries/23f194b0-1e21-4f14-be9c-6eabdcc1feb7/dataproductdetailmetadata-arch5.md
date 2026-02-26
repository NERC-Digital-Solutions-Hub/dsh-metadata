# Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018

## Summary
- Open data product linking macroinvertebrate abundance (1,519 English river sites, 1965–2018) with 41 water quality determinands, river flow, air temperature and static environmental site descriptors.
- Integrates multiple nationally collected datasets (EA Biosys, EA Water Quality Archive, NRFA, CHESS-met, LF2000-WQX, RHS, Land Cover Map 2015) into a harmonised, analysis-ready CSV portfolio.
- Includes site descriptors, time-series statistics (6-month windows before sampling), and spatially coordinated variables to support environmental modelling and ecological research.
- Data product produced under the ChemPop project (NERC funding) and deposited for public use; acknowledges licensing, data governance and provenance requirements.

## Context and Purpose
- Macroinvertebrates as indicators of chemical and environmental stress in rivers; short life cycles provide rapid responses to stress.
- English long-term monitoring data (40+ years) underpin spatial and temporal trend analyses beyond laboratory settings.
- Aims to provide a usable, discoverable data product, balancing comprehensiveness with resource constraints and documenting integration methodology and limitations.

## Data Model and Key Components
- 1519 macroinvertebrate sampling sites with accompanying site descriptors (altitude, slope, upstream catchment land cover, discharge, width, depth, substrate).
- 41 water quality determinands (from Water Quality Archive; pre-2000 licensed EA data included) with 6-month preceding statistics (min, max, mean, median, sd).
- River flow statistics at nearest NRFA gauging stations (mean, median, sd, CV, Q5/mean, Q95/mean) for both the full time series (period of interest) and 6-month antecedent windows.
- Daily air temperature statistics derived from CHESS-met (1961–2017) for 6-month windows preceding sampling.
- Habitat quality indices from River Habitat Survey (RHS): HMS, HMS_Class, RSB_SubScore, HQA, HQA_ADJ; RHS data is largely single-visit but some sites have multiple RHS surveys.
- Land cover upstream of sites from Land Cover Map 2015 (LCW, LCArable, LC Seminatural, LC Urban) aggregated to catchment scale.
- Effluent dilution factor (EDF) for wastewater exposure estimated with LF2000-WQX model, providing mean, standard deviation, and 90th/95th percentiles.
- File structure and naming conventions standardized to region-based CSV files (see below).

## Data Sources and Provenance
- Macroinvertebrate time series: Freshwater river macroinvertebrate surveys (Biosys) via Environment Agency and UKCEH pipelines.
- Water quality: Environment Agency Water Quality Archive (pre-2000 licensed EA data included); 41 determinands selected (determinant codes and labels provided in Appendix tables).
- River flow: National River Flow Archive (NRFA) gauging data; daily flow values linked to macroinvertebrate sites by proximity along the river network.
- Air temperature: CHESS-met meteorology dataset (Great Britain, 1961–2017).
- Habitat quality: River Habitat Survey (RHS) data (1994–present).
- Land cover: Land Cover Map 2015 (21 classes) with upstream catchment aggregation using IHDTM flow direction/grid.
- EDF modelling: LF2000-WQX model for wastewater influence in river flows.
- river network and hydrology infrastructure: UKCEH digital river network, IHDTM grids, and associated GIS tools.

## Data Processing, Cleaning and Quality Assurance
- FRMS macroinvertebrate data cleaned and harmonised (duplicate removal, ID consistency, taxon name standardisation to Davies & Edwards 2011; conversion from semi-quantitative categories to numerical abundances post-2002).
- Taxonomic reconciliation performed to align EA names with standard nomenclature; added family and order metadata.
- Water quality data extraction: regional matching of water quality sites to macroinvertebrate sites, with manual verification to satisfy:
  - same river reach; no upstream wastewater works or major tributaries between sites.
  - proximity and data availability considerations.
  - handling of LoQ values via three schemes (LoQ, 0, LoQ/2) for min/max/median/mean calculations.
- River flow: distance-along-network matching of macroinvertebrate sites to nearest gauging station; manual verification to ensure catchment consistency.
- Hydrological statistics computed per 6-month antecedent window and for full POI (period of interest 1974–2019); standardised calculations per Richter et al. (1996) method for flow thresholds and exceedances.
- CHESS-met processing to produce 6-month atmospheric temperature statistics per site.
- Habitat quality indices tied to macroinvertebrate sites via RHS matching within 5 km; notes that RHS is largely a single-visit dataset, with some sites having multiple RHS surveys.
- Land cover extraction and catchment upscaling performed in Data Labs with IHDTM flow-accumulation grids; catchments defined by cells with values >200; categories aggregated to broad groups (Woodlands, Arable, Seminatural, Urban); quality checks confirm <1% variance in aggregation and 100% cumulative coverage.

## Data Access and Structure
- Data delivered as region-wise CSV files, with explicit file naming conventions:
  - Macroinvertebrate taxon abundances: CP_<REGION>_MInv_taxonAbundance_<startDate-endDate>.csv
  - Water quality statistics: CP_<REGION>_MInv_<determinandLabel>Stats_<startDate-endDate>.csv
  - River flow statistics: CP_<REGION>_MInv_riverFlowStats_<startDate-endDate>.csv
  - Air temperature statistics: CP_<REGION>_MInv_airTempStats_<startDate-endDate>.csv
  - Site descriptors: CP_<REGION>_MInv_siteVariables.csv
  - Site matching locations: CP_<REGION>_MInv_siteMatchedLocation.csv
- Core descriptor columns include macrosite IDs, geographic coordinates (E/N), altitude, slope, catchment descriptors, discharge, substrate indicators, and EDF statistics (mean, quartiles, std).
- Data quality notes acknowledge some missing data due to licensing (Tables A.3.1 and A.3.2) and mention that certain EA-licensed water quality data are not publicly accessible.
- Heatmaps (Appendix 4) illustrate the temporal coverage and data completeness for the 41 determinands, river flow, and air temperature, highlighting data gaps (NA) across regions.

## Limitations, Gaps and cautions
- Standardisation gaps: legacy data from disparate purposes resulted in incomplete harmonisation and some variables (e.g., land cover over time) treated as static; final output contains gaps (noData) for many variables at some sites.
- Temporal coverage: CHESS-met ends in 2017; missing air temperature values beyond that date for some macroinvertebrate sites.
- Water quality data licensing: some macroinvertebrate sites lack matched water quality data due to licensing restrictions; a small number of matches fail due to extraction gaps.
- EDF interpretation: 0% EDF does not guarantee absence of wastewater influence in headwaters; small WWTWs may be omitted in the truncated network, but their effects could be non-negligible in headwaters.
- Taxonomic changes: historic taxonomic names updated to current standards, but some older or region-specific synonyms may persist; users should validate taxon scope for longitudinal analyses.
- Habitat indices: RHS provides qualitative scores; cross-site comparability may be constrained by river type and survey timing.

## Governance, Provenance and Licensing
- Data are prepared as an open data product with explicit provenance (EA, UKCEH, NRFA, CHESS-met, RHS, LCM2015) and citations within the supporting information and appendices.
- Data sources and access details (Table 14) include rights acknowledgments and data owners; licensing restrictions noted for certain water quality data.
- Versioned data product: Supporting information document for Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018, version 2; dataset deposits facilitated by NERC EIDC.
- Documentation emphasizes reproducibility: step-by-step methodology, data integration workflow, and scripts (Python-based) used for matching and statistics, with explicit software and libraries (Pandas, NumPy, NetCDF4, Xarray, Shapely, Geopandas, NetworkX).

## Practical Implications for Data Stewards
- Ensure consistent metadata ingestion for all seven regional files, including linking to source datasets and their licenses.
- Maintain version control and changelogs as updates occur (e.g., improvements in taxon nomenclature, changes in source data availability, updates to EDF modelling).
- Provide clear guidance on handling missing values, LoQ treatments, and interpretation of 0-EDF values in downstream analyses.
- Facilitate data discovery by documenting regional coverage, data completeness (Appendix heatmaps) and any site-specific exclusions due to licensing or extraction issues.
- Support interoperability by aligning variable naming with existing ontologies (where possible) and preserving linkage keys (BIO_SITE_ID, region codes, sample dates) across files.