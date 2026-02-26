# Terrestrial habitat and vegetation data from the marginal uplands of Cumbria, 1978

## Overview
- A survey of terrestrial habitats and vegetation in Cumbria’s marginal uplands (1978).
- 262 plots of 200 m2 surveyed across 52 x 1 km2 squares using stratified sampling.
- Data collected: vascular plants, bryophytes, macro-lichens; habitat categories (within plot and within the full 1 km square); slope and aspect.
- Soils data were collected but are not documented here and currently unavailable (as of 12/9/2017).
- Geographic coverage: Cumbria, England; Time period: 1978.

## Data collected and structure
- Vegetation data: presence/absence of species recorded in nested quadrats (4 m2, 25 m2, 50 m2, 100 m2, 200 m2); growth forms (e.g., aquatic, bryophyte, forbs, ferns, grasses, lichens, woody plants).
- Habitat data: habitat types recorded both within each 200 m2 plot and across the entire 1 km square; height-related attributes (slope and aspect) measured for each plot.
- Plot-level descriptors: slope (degrees), aspect (degrees magnetic), and 10 km grid references (E_10KM, N_10KM).
- Species data: full species list with codes, scientific names, common names where available, and growth forms; includes nested sampling details (NEST 1-5 per plot).

## Survey design and methods
- Based on a county-wide environmental classification (1975) and Bunce & Shaw (1973) standardized survey methods.
- Stratified land classification: 16 strata identified; marginal areas correspond to strata 9–12.
- Site selection: 52 one-kilometre squares; within each square, five 200 m2 vegetation plots were surveyed (total of 262 plots).
- Data collection procedures mirror established ecological survey methods, with a nested quadrat approach for vegetation data.

## Spatial data and data files
- CMUP_1978_SITE_DESCS.csv: habitat descriptions for entire 1 km square sites (stratum, site ID, primary code, description, type).
- CMUP_1978_SITE_DESCS_RELATED.csv: related habitat descriptions for 1 km squares (woody features, beasts, tree species, etc.).
- CMUP_1978_PLOTS.csv: plot-level information (stratum, site ID, plot number, slope, aspect, 10 km coordinates).
- CMUP_1978_PLOT_DESCS.csv: habitat descriptions for each plot within 1 km square sites (code, descriptions, habitat group).
- CMUP_1978_GROUND_FLORA.csv: presence of vascular plants, bryophytes, and lichens by plot (including survey date, nest, species code, scientific name, common name, growth form).
- Spatial coordinates: data include OSGB-based 10 km grid references (E_10KM, N_10KM) for plot placement; specific site locations are not disclosed to protect landowner privacy.

## Provenance and related datasets
- Originators: C.B. Benefield & J.K. Adamson; Data management by C. Wood (CEH Lancaster).
- Related datasets and key publications:
  - Bunce, R.G.H.; Smith, R.S.; Booy, M.; Wood, C.M. (2017). Cumbria 1975 data (NERC EIDC).
  - Bunce, R.G.H.; Smith, R.S.; Hill, M.O. (2015). Land Classification of Cumbria 1975 (NERC EIDC).
  - Bunce & Shaw (1973). A Standardized Procedure for Ecological Survey.
  - Bunce & Smith (1978). Handbook of Field Methods (UK Ecological Survey).
- Related datasets provide broader context for Cumbria ecological surveys and land classification.

## Privacy, access, and data management
- To protect landowner privacy, precise site locations are not disclosed.
- Soil data are mentioned as collected but not documented or available in this dataset version.
- Data management and survey coordination conducted by CEH (Centre for Ecology & Hydrology) and field surveyors named in the dataset.

## Practical GIS implications
- Ideal for map-based visualization of habitat types and plant communities at 1 km and plot scales.
- Use 1 km square site IDs to link to habitat descriptions and to aggregate plot-level data across larger areas.
- Integrate slope and aspect with habitat classifications to analyze microhabitat variation.
- Nested quadrat vegetation data enable richness and growth-form analyses by plot and by 1 km square.
- Coordinate framework based on OSGB 1936 with 10 km grid references supports GIS layering and spatial joins.
- Limitations to consider: absence of precise site coordinates; absence of soil data; historical (1978) timeframe may affect comparability with contemporary datasets.