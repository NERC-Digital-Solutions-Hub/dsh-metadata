# Multi-tier archetypes to characterise British landscapes, farmland and farming practices: Supporting Information

## Purpose and approach
- Uses data-driven machine learning (Self-Organising Maps) to create landscape and agricultural management archetypes at 1 km resolution across Great Britain.
- Defines three tiers of archetypes:
  - Tier 1: broad, long-timescale landscape differences (modifiable mainly over 10–100 years).
  - Tier 2: nuanced variations within farmland-dominated areas (intermediate timeframes, 1–10 years).
  - Tier 3: national-level, farm-management–relevant socio-economic and agro-ecological characteristics (shorter timeframes).
- Tier 3 archetypes could not be generated for Scotland due to input data gaps.
- Outputs include spatial archetype maps and associated codebooks to describe variable loadings.

## Data structure and outputs
- Four multi-band raster files at 1 km resolution:
  - Tier 1 and Tier 2: a single raster for Great Britain.
  - Tier 3: one raster for England and one for Wales.
  - Each raster band contains: archetype ID and Euclidean distance to the archetype centroid.
- Four supporting CSV files containing:
  - Loadings of each input variable for each archetype.
  - Shorthand names for archetypes.

## Input variables and data sources (1 km resolution)
- Land cover and geomorphology
  - Nine land cover classes; Land Cover Map 2015 data.
  - Landscape structure metrics (Aggregation Index) for applicable classes.
  - Watercourses, woody linear features, inter-field hedges.
  - Elevation, slope, and related terrain metrics.
- Climate and soils
  - Mean temperature and precipitation (2005–2015).
  - Soil pH, sand, silt, clay, and organic carbon.
  - Mean soil moisture (2005–2015) and relative soil dryness.
- Hydrology and water management
  - Elevation-related metrics and water-related layers.
- Socio-economic and accessibility
  - Population density (2011 census).
  - Road accessibility distances to major/minor roads; protected area coverings (Tier 2).
  - High-level socio-economic indices derived from the Sustainable Intensification Dynamic Typology Tool (Farm Business Survey-based).
- Farm and field characteristics
  - Farm boundaries and field data from stewardship and farming schemes; interpolated farm size via kriging.
  - Spread Index, field shape index (edge:area ratio).
- Crops and livestock
  - Crop and livestock data from Land Cover plus Crops (LCC) and Agricultural Census; pesticide application rates (2012–2016).
  - Crop diversity metrics (Simpson indices, Edge Contrast Index, Subdivision, Isolation).
  - Functional diversity and patch-based metrics over multiple years (2015–2020 for certain metrics).

## Tier definitions and variable selections
- Tier 1: captures broad landscape differences across Britain; limited by long-term modifiability.
- Tier 2: focuses on farmed landscapes with potential landowner influence over shorter to mid-term timescales.
- Tier 3: emphasizes elements of the landscape farmers can modify or influence in the short term.
- Variables are selected by expert judgment to represent physical, land-management, and socio-economic variation appropriate to each tier.

## Self-Organising Maps (SOM) parameterisation and stability
- SOMs used to cluster 1 km grid cells into archetypes (nodes) based on normalised input data.
- Handling missing data: SOMs accept cells with missing data for all but one variable; missing data do not bias clustering.
- SOM configuration:
  - Parallel batch SOM with 500 presentations.
  - Grid size chosen by assessing the elbow in mean distance to archetype centroids across configurations.
- Stability and certainty:
  - 1000 iterations run with fixed input parameters to assess classification certainty.
  - Hierarchical clustering (Ward’s method) on node codebooks to identify consistent archetypes across iterations.
  - Final cell archetype assignment uses the most frequent archetype across iterations; certainty recorded as a measure of consistency.
- Archetype naming:
  - Names are derived from the strongest positive/negative variable loadings and simplified to human-readable labels.
  - Names are convenience descriptions and do not fully describe all archetype characteristics.

## Outputs and interpretation for data leadership
- The dataset provides a repeatable, scalable way to characterize landscapes and farming practices via archetypes at multiple spatial scales.
- Outputs enable:
  - Easy comparison of landscape types and farming regimes across Great Britain.
  - Assessment of how archetypes align with user needs and policy contexts (through loadings and distance to archetype centroids).
  - Investigation of spatial patterns in soil, climate, land cover, and socio-economic factors as they relate to management opportunities.
- Notable limitations:
  - Tier 3 archetypes unavailable for Scotland due to input data gaps.
  - Archetype names are indicative rather than exhaustive descriptors of complex characteristics.
  - Tiers are analyzed separately rather than as a nested hierarchy to maintain interpretability.

## Practical implications for data strategy
- Demonstrates a robust, data-rich workflow for creating typologies that integrate physical, ecological, and socio-economic variables at multiple scales.
- Provides transparent, shareable data products (raster archetypes and loadings CSVs) suitable for integration with policy analysis, land-management planning, and cross-sector collaboration.
- Emphasizes reproducibility through multiple iterations, stability checks, and explicit documentation of variable loadings and archetype definitions.