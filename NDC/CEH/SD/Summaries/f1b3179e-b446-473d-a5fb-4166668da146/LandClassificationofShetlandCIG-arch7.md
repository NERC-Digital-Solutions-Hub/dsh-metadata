# Land Classification of Shetland (1974)

## Overview
- A 1974 terrestrial habitat and vegetation survey of the Shetland Isles.
- Stratified environmental land classification used to guide sampling; 16 environmental strata defined.
- Aimed to provide a sound basis for subsequent ecological studies; integrated with map data and, when available, aerial photographs.

## Geography, scope, and data format
- Geographic coverage: Shetland, Scotland; time period: 1974.
- Data format: ESRI Shapefile; projection: OSGB 1936.
- Resolution: 1 km grid squares; total of 2046 land-containing 1 km squares.
- Dataset structure includes a simple attribute column for strata.

## Stratification and sampling methodology
- Stratification based on physical geography using maps and aerial photographs (aerials unavailable at the outset but later used for refinement).
- Sampling unit: fixed 1 km grid squares; stratified random sampling within strata.
- Ground truthing and supplementary surveys for groups with limited prior data:
  - Bryophytes and lichens
  - Key vegetation/habitat types (e.g., cliffs, salt-marshes, shingle banks)
- Nearly 1000 vegetation plots (each ~200 m²) collected using standardized methods.

## Data attributes and structure
- 150 attributes used to produce the stratification (Table 1 in the source).
- Attribute types:
  - Continuous attributes (e.g., altitude, slope)
  - Presence/absence attributes (e.g., cliff, hill-top)
- 18 geological attributes derived from the quarter-inch Geological map (full cover).
- Data columns in the dataset:
  - OBJECTID: unique row identifier
  - STRATA: final stratification class (1–16)
  - Shape: geometry type (polygon)
- Indicator species analysis methods used to drive the stratification and classification.

## Strata and their geographic implications
- Four groups (each with strata 1–4, 5–8, 9–12, 13–16) describing environmental variation:
  - Strata 1–4: Coastal, few rivers, more gentle terrain
  - Strata 5–8: Coastal with more sea influence and steeper slopes; more headlands and sea cliffs; more rivers to sea
  - Strata 9–12: Inland, high altitude; 600–900 ft hills; little water bodies; major rock type often gneiss
  - Strata 13–16: Lower, undulating; extensive peat and freshwater lochs; hills around ~300 ft; Old Red Sandstone common
- The final product maps the distribution of these 16 strata across Shetland.

## Outputs and GIS relevance
- Primary output: map-based strata classification (16 classes) suitable for GIS analysis and visualization.
- Provides a framework for landform classification and interpretation of geographic features in relation to geology and hydrology.
- Facilitates planning of targeted ecological surveys and data integration with other spatial datasets (e.g., coastline, soils, vegetation layers).

## Key references and background
- Foundational methodology and classification concepts:
  - Bunce, R.G.H. & Shaw, M.W. (1973) Standardized Procedure for Ecological Survey
  - Bunce, R.G.H. (1974) Shetland Vegetation Survey: Field Methods
  - Milner (1975) Shetland project monitoring reports
- Stratification and analysis methods:
  - Hill, M.O. (1973) Reciprocal averaging
  - Hill, M.O., Bunce, R.G.H. & Shaw, M.W. (1975) Indicator species analysis
- Broader classification framework:
  - Bunce et al. (1996) Land classification for strategic ecological survey
  - Bunce et al. (2007) ITE Land Classification of Great Britain
  - Metzger et al. (2005) Climatic stratification of Europe
- Milestone context: 1974 survey led by R.G.H. Bunce, Institute of Terrestrial Ecology

## Originator
- R.G.H. Bunce, Woodlands Research Section, Institute of Terrestrial Ecology, Merlewood Research Station.