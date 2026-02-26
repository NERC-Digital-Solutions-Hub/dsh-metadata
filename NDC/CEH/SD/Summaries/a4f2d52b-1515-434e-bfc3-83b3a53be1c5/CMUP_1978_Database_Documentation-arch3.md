# Terrestrial habitat and vegetation data from the marginal uplands of Cumbria, 1978

## Overview
- A survey of terrestrial habitats and vegetation in Cumbria’s marginal uplands conducted in 1978.
- 262 x 200 m2 plots were surveyed across the county using a stratified sampling framework.
- Data focus on vegetation (vascular plants, bryophytes, macro-lichens) and habitat characteristics; soil data were collected but are not documented here and not currently available (as of 12/9/2017).

## Sampling design and methods
- Landscape stratification based on 150 attributes per 1 km2; 16 strata identified (Bunce et al., 2015), with marginal areas represented by strata/Land Class numbers 9–12.
- 52 1 km2 squares were selected, each containing 5 plots of 200 m2.
- Survey methods follow Bunce & Shaw (1973) with Bunce & Smith (1978) and related works as standards.
- Nested quadrat vegetation recording: in each 200 m2 plot, species are recorded in sequential quadrats of 4 m2, 25 m2, 50 m2, 100 m2, and the full 200 m2; only previously unrecorded species are listed as quadrat size increases.
- Habitat data recorded for both within-plot and within-whole-square contexts; slope measured with clinometer; aspect measured bearing down the slope with a Silva compass.
- Soil data were collected but not documented in this dataset; most sites are/private landowners to protect privacy.

## Data content and structure
- Vegetation data: presence of vascular plants, bryophytes, and macro-lichens; growth form coding (e.g., aq, b, f, fe, g, l, ma, m, s, ss, w).
- Habitat data: detailed habitat categorisations within plots and across whole squares, plus slope (degrees) and aspect (magnetic degrees).
- Plot-level data: 262 plots labeled by site (1 km square) and plot number; includes slope, aspect, and 10 km grid references (E_10KM, N_10KM).
- Files (CSV) and purposes:
  - CMUP_1978_SITE_DESCS.csv: habitat descriptions for each 1 km square site; fields include STRATUM, SITE_ID, PCODE, PDESCRIPTION, TYPE.
  - CMUP_1978_SITE_DESCS_RELATED.csv: related habitat descriptions for 1 km squares; includes codes and woody species information.
  - CMUP_1978_PLOTS.csv: plot information; includes STRATUM, SITE_ID, PLOT_NO, SLOPE, ASPECT, E_10KM, N_10KM.
  - CMUP_1978_PLOT_DESCS.csv: habitat descriptions for each plot; includes CODE_NO, DESCRIPTION, HAB_GROUP.
  - CMUP_1978_GROUND_FLORA.csv: presence data for vascular plants, bryophytes, and lichens by plot; includes SURVEY_DATE, NEST, BRC_NUMBER, BRC_NAMES, COMMON_NAME, GROWTH_FORM.
- Appendix and related materials provide a full species list recorded during the survey (Appendix 1) and cross-references to standard methods and related datasets.

## Provenance and documentation
- Originators: C.B. Benefield & J.K. Adamson (Institute of Terrestrial Ecology - Merlewood).
- Field surveyors: C.B. Benefield, J.K. Adamson, W. Elfyn Hughes.
- Data management: C. Wood, Centre for Ecology & Hydrology, Lancaster.
- Original purpose: to classify Cumbria ecologically (1975) and to monitor changes in marginal uplands (33% of Cumbria) influenced by agricultural practice through a detailed survey of soils, vegetation, and environmental parameters.
- Related datasets and publications provide standardized methods (e.g., Bunce & Shaw 1973; Bunce & Smith 1978; Bunce et al. 2015).

## Access, metadata, and governance considerations
- Site locations are not disclosed to protect landowner privacy; coordinates are provided at 10 km scale (OSGB) for reference.
- Data quality is anchored in standardized field procedures and codes; soils data exist but are not documented here.
- Metadata includes structure of data files and growth-form classifications; Appendix 1 contains the full species list, illustrating taxonomic detail and growth forms.
- Public sharing of underlying data may present barriers in some cases due to privacy and sensitivity of site-level information.

## Related datasets and provenance
- Related datasets with DOIs include:
  - 2015 Land Classification of Cumbria (Bunce et al., 2015)
  - 1975 Terrestrial habitat, vegetation, and soil data from Cumbria (Bunce et al., 2017)
- Foundational methods references:
  - A Standardized Procedure for Ecological Survey (Bunce & Shaw, 1973)
  - UK Ecological Survey Handbook of Field Methods (Bunce, 1978)

## Relevance for monitoring frameworks
- Provides a benchmark ecological dataset with standardized survey methods, stratified sampling, and clear data products suitable for baseline comparisons and retrospective monitoring in marginal uplands.
- Demonstrates the importance of:
  - Detailed metadata (e.g., growth-form categories, habitat groupings)
  - Data governance considerations (privacy, data sharing constraints)
  - Clear documentation of sampling design (strata, site and plot structure)
- Potential for trend analysis if integrated with future or repeated surveys, and for cross-site comparisons using the same methodological framework.

## Limitations and considerations for use
- Soil data are collected but not documented here; limits integrated environmental analyses beyond vegetation and habitat.
- 1978 timeframe; may require contextualization for contemporary monitoring (taxonomic updates, land-use changes).
- Site-level privacy constraints limit precise geolocation usage; analyses rely on 1 km square and plot-level descriptors rather than exact coordinates.