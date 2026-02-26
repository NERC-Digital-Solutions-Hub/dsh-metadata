# Terrestrial habitat and vegetation data from the marginal uplands of Cumbria, 1978

## Overview
- A comprehensive ecological survey of marginal upland habitats and vegetation in Cumbria, England, conducted in 1978.
- 262 plots of 200 m2 were sampled using stratified design across 1 km squares, within 52 surveyed 1 km2 sites.
- Aimed to support environmental classification, monitoring of land-use change, and predictive monitoring of vegetation, soils, and environmental parameters.

## Scope and content
- Geographic coverage: Cumbria, England.
- Time period: 1978.
- Data categories:
  - Vegetation data: vascular plants, bryophytes, and macro-lichens.
  - Habitat data: within-plot and within-square habitat types, slope, and aspect.
  - Soils: collected but not documented or available in this release (noted as missing as of 2017).
- Privacy note: specific site locations are not provided to protect landowner privacy; most plots are on private land. Location references are managed to preserve confidentiality.

## Sampling design and methods
- Stratified sampling based on a county-wide land classification framework; originally 16 strata with marginal uplands represented by strata 9–12.
- 52 1 km2 squares selected; within each square, 5 plots of 200 m2 were surveyed (262 total plots).
- Vegetation data collection:
  - Nested quadrat system: per plot, species recorded in increasing quadrat sizes: 4 m2, 25 m2, 50 m2, 100 m2, and 200 m2.
  - Five plots per 1 km square were chosen randomly.
- Habitat data collection:
  - Habitat types recorded inside plots and for the whole 1 km square.
  - Slope measured with clinometer; aspect measured with compass.
- Data recorded per plot and per species, with detailed habitat code schemes and growth forms.

## Data files and structure
- CMUP_1978_SITE_DESCS.csv: habitat descriptions for each 1 km square site; fields include STRATUM, SITE_ID, PCODE, PDESCRIPTION, TYPE.
- CMUP_1978_SITE_DESCS_RELATED.csv: related habitat descriptions for 1 km square sites; includes woody species data (SCI_NAME) and descriptive codes.
- CMUP_1978_PLOTS.csv: plot-level metadata; STRATUM, SITE_ID, PLOT_NO, SLOPE, ASPECT, E_10KM, N_10KM.
- CMUP_1978_PLOT_DESCS.csv: habitat descriptions for each plot; STRATUM, SITE_ID, PLOT_NO, CODE_NO, DESCRIPTION, HAB_GROUP.
- CMUP_1978_GROUND_FLORA.csv: presence/absence data for vascular plants, bryophytes and lichens by plot; includes SURVEY_DATE, NEST (1–5), BRC_NUMBER, BRC_NAMES, COMMON_NAME, and GROWTH_FORM.
- Appendix 1: full species list (long taxon list with codes and growth forms).
- Related publications and datasets (e.g., 2015/2017 linked datasets on Cumbria land classification and Cumbria ecological surveys).

## Data provenance and governance
- Originators and field team: C.B. Benefield, J.K. Adamson, and W. Elfyn Hughes.
- Data management: C. Wood (Centre for Ecology & Hydrology, Lancaster).
- Original purpose: to advance an environmental classification of Cumbria and monitor changes in marginal uplands related to agricultural practices.
- Documentation and standards: methods follow Bunce & Shaw (1973) standardized survey procedures and Bunce, Smith & Hill (2015) land classification frameworks; 1978 UK Ecological Survey field methods are cited.
- Documentation status: soil data collected but not documented or publicly available in this release (as of 2017).
- Privacy and access: precise site locations withheld to protect landowners; approximately OSGB coordinates are present in the data files for grid-based referencing, but exact site coordinates are not disclosed.

## Quality, limitations, and stewardship considerations
- Strengths: standardized, stratified design with a detailed nested-plot vegetation sampling approach; explicit habitat coding and growth-form taxonomy; linkage to broader Cumbria ecological datasets.
- Limitations:
  - Soils data not documented or accessible in this dataset.
  - Exact plot/site locations restricted for privacy.
  - Data captured in 1978; temporal updates or changes since then are not included.
- Stewardship notes:
  - Clear data lineage, standardized survey methods, and explicit metadata descriptions support discoverability and re-use.
  - Potential for updates or integration with related Cumbria datasets (e.g., 1975/2015–2017 linked datasets) through the CMUP coding framework.
  - Data management records attributed to CEH with historical field teams; any reuse should acknowledge the original sources and linked publications.