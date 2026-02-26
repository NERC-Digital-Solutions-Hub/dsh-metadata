# Terrestrial habitat and vegetation data from the marginal uplands of Cumbria, 1978

## Overview
- A historic ecological survey of marginal upland habitats and vegetation across Cumbria, England (1978).
- Surveyed 262 plots of 200 m² each, selected via stratified sampling across Cumbria’s 1 km squares.
- Data collected include plant species, habitat types, major biota, and soil information (soil data noted as not documented or available as of 2017-09-12).
- Geographic coverage is Cumbria; time period corresponds to 1978.
- Soil-related data exist but are not currently accessible in this dataset.

## Data content and categories
- Vegetation Data: presence/occurrence of vascular plants, bryophytes, and macro-lichens.
- Habitat Data: habitat categories inside the 200 m² plot and across the full 1 km square; slope and aspect measured for plots.
- Data collection focuses on enabling environmental classification, monitoring changes, and supporting broader data use.

## Sampling design and survey methods
- Original purpose: to classify Cumbria environmentally (1975 framework) and investigate marginal upland areas (33% of the county) for changes in vegetation, fauna, and soils due to agricultural practices.
- Sampling framework:
  - Stratified land-class approach using 150 attributes per 1 km²; 16 strata identified (Bunce et al., 2015).
  - From strata 9–12 (marginal areas), 52 1 km² squares were selected, each containing 5 plots of 200 m².
- Vegetation sampling:
  - Nested quadrat system: data recorded from 4 m², 25 m², 50 m², 100 m², and 200 m² quadrats.
  - Within each plot, all vascular plants, bryophytes, and macro-lichens were recorded; only new species were listed at progressively larger quadrats.
- Habitat and environmental data:
  - Habitat types recorded within the 200 m² plot and within the whole 1 km square.
  - Slope measured with a clinometer; aspect measured bearing down the slope with a Silva compass.
- Plot selection and randomization: 5 plots per 1 km square site, positioned randomly.

## Data structure and accompanying files
- CMUP_1978_SITE_DESCS.csv: Habitat descriptions for each entire 1 km square site.
- CMUP_1978_SITE_DESCS_RELATED.csv: Related habitat descriptions for 1 km square sites, including information on woody species (breeds, trees) and related taxa.
- CMUP_1978_PLOTS.csv: Plot-level information, including STRATUM, SITE_ID, PLOT_NO, SLOPE, ASPECT, and 10 km grid coordinates (E_10KM, N_10KM).
- CMUP_1978_PLOT_DESCS.csv: Habitat descriptions for each plot within 1 km square sites (HAB_GROUP, codes and descriptions).
- CMUP_1978_GROUND_FLORA.csv: Ground flora presence data for plots, including SURVEY_DATE, NEST (plot sampling level 1–5), BRC_NUMBER, BRC_NAMES, COMMON_NAME, and GROWTH_FORM (e.g., aq, b, f, fe, g, l, ma, m, s, ss, w).
- Appendix 1 (within GROUND_FLORA data): Full species list (example entries shown include a broad range of dicots, ferns, bryophytes, and algae).

Note on data structure: A nested quadrat approach underpins vegetation data collection, with species coded by BRC numbers and growth forms; site-level and plot-level habitat descriptions accompany the species data.

## Provenance, governance, and access notes
- Originators: C.B. Benefield and J.K. Adamson (Institute of Terrestrial Ecology – Merlewood).
- Field surveyors: C.B. Benefield, J.K. Adamson, W. Elfyn Hughes.
- Data management: C. Wood, Centre for Ecology & Hydrology, Lancaster.
- Privacy and accessibility: Specific site locations are not provided to protect landowner privacy; most sites were privately owned.
- Original publications and documentation:
  - Standardized ecological survey methods (Bunce & Shaw, 1973).
  - UK Ecological Survey: Handbook of Field Methods (Bunce, 1978).
  - Ecological survey of Cumbria (Bunce & Smith, 1978).
  - Land Classification of Cumbria 1975 (Bunce et al., 2015).
  - Related dataset entries and DOIs available through NERC Environment Information Data Centre.

## Related datasets and publications
- Related datasets:
  - Terrestrial habitat, vegetation and soil data from Cumbria, England, 1975 (NERC EIDC).
  - Land Classification of Cumbria 1975 (NERC EIDC).
- Key references for methods and context:
  - Bunce & Shaw (1973): A Standardised Procedure for Ecological Survey.
  - Bunce (1978): UK Ecological Survey – Handbook of Field Methods.
  - Bunce & Smith (1978): An ecological survey of Cumbria.
  - Bunce et al. (2015): Land Classification of Cumbria 1975.

## Data use considerations for a Data Support workflow
- Temporal context: Data are from 1978; suitable for historical baselining, long-term change studies, or validation against modern datasets.
- Data integration: Structure supports joining site-level, plot-level, and ground flora data with habitat descriptors and topographic variables (slope, aspect).
- Data quality and limitations:
  - Soil data mentioned as not documented or accessible (as of 2017).
  - Site locations withheld to protect privacy; precise spatial analysis requires handling of generalized site descriptors.
  - Data formats are CSVs with codes (e.g., PCODE, BRC numbers) that require reference lists for interpretation.
- Potential outputs for end users:
  - Dashboards or reports summarizing vegetation diversity by habitat type and slope/aspect, with self-service filtering by stratum or site.
  - Visualizations linking habitat classes to plant groups and growth forms.
  - Data provenance traces linking 1978 methods to vegetation records and site descriptions.
- Suggested integration with other data:
  - Combine with other Cumbria ecological datasets from 1975 or later to analyze landscape changes and land classification outcomes.

## Summary of original purpose and value
- Purpose: to enable predictions and monitoring of changes in marginal upland environments in Cumbria, driven by agricultural practices and land-use changes.
- Value for data support: provides a well-documented, multi-layer dataset combining vegetation inventories, habitat classifications, and topographic context, suitable for historical baselining, environmental classification studies, and cross-dataset ecological analyses.