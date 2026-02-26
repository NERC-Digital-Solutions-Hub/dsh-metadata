# Tree, vegetation and soil information from an ecological survey of semi-natural woodlands in the English Lake District, 1969

## Overview
- A historical ecological survey of 48 semi-natural woodlands in the English Lake District conducted in June–August 1969.
- Data collected across six randomly placed 20 m x 20 m plots per site (sometimes 6–8) to capture trees, shrubs, ground flora, and soil attributes.
- Aimed to support site classification and broader woodland surveys with standardized methods and screening for data suitability and gaps.

## Dataset composition and contents
- Core data files and tables:
  - LAKEDISTRICTWOODS_1969_GROUND_FLORA: presence/absence data for vascular plants and bryophytes from 10 nests per plot (25 cm x 25 cm sampling areas).
  - LAKEDISTRICTWOODS_1969_SoilPH: top 10 cm soil pH values from 5 sampling points per plot (uses 1:1 soil:distilled water; 999 indicates no sample).
  - TREE_ID / SHRUB and related fields: species, DBH (cm), height, stem counts, dead indicators, and taxonomic coding; records trees vs shrubs and their measurements.
  - Site and Plot metadata: site name, OS grid references, plot numbers, weather, aspect, slope, and sampling date.
  - LAKEDISTRICTWOODS_1969_SITES: location data for each woodland site (including coordinates for mapping).
  - Additional detailed plot-level and nest-level sampling schemas (e.g., nested vegetation sampling grids, species codes, and bryophyte coverage).
- Data capture schema includes standardized fields for species names (with Latin names aligned to updated taxonomies), soil chemistry, and vegetation structure.
- Sampling framework documented as 6 plots per site (4 x 4 m grid inside each plot for nested sampling) and 10 nests per plot for vegetation presence/absence.

## Spatial and temporal coverage
- Geographic scope: Lake District, England (northwest England sampling sites).
- Time period: June–August 1969.
- Spatial granularity: 48 woodland sites with precise OS grid references; each site sampled via six 20 m x 20 m plots.

## Methodology and provenance
- Originator: Woodland Ecology Section, Nature Conservancy (Merlewood, Grange-over-Sands, Cumbria).
- Context: Built on 1968 Merlewood Programme emphasis on woodland site classification; linked to national woodland surveys and association-analysis approaches.
- Procedures:
  - Six randomly placed 20 m x 20 m plots per site; 25 cm x 25 cm vegetation nests sampled within 10 grid intersections per plot.
  - Tree measurements: DBH and heights for trees within each plot; shrubs measured across DBH categories; presence/absence of ground flora recorded at nest intersections; bryophyte presence recorded for entire plots.
  - Soil sampling: top 10 cm from five points per plot for pH analysis and loss on ignition (LOI) via standard methods.
  - Documentation of weather, aspect, slope, and plot observations per sampling occasion.
- Analytical lineage: Preliminary association-analytic grouping of species data; results used to validate site classification procedures for broader woodland surveys (e.g., 1971 National Woodland Surveys).

## Data management, structure, and metadata
- Data management notes emphasize standardization of data collection and alignment of species names to current taxonomies (BRC codes and updated Latin names).
- Ground flora data structure records species, presence/absence per nest, and nest-level sampling details; includes bryophyte data for full quadrats in most sites.
- Soil data structure records site, plot, nest, and pH values with missing data flagged (999 as no sample).
- Tree and shrub data recorded with detailed columns for species, DBH, height, and status (live/dead) and clade type (TREE vs SHRUB).
- Spatial data include OS grid references and easting/northing coordinates to support GIS interoperability.

## Related datasets and references
- Related to Woodland Survey of Great Britain, 1971 (Wood et al., 2015) and broader National Woodland Surveys (1971–2001).
- Foundational methods and background references:
  - Bunce & Shaw (1973) on standardized ecological survey procedures.
  - Steele (1968) Woodland Cards and national woodlands data.
  - Williams & Lambert (1959) multivariate association analysis in plant communities.
  - Allen (1974) Chemical analysis of ecological materials.
- Cross-referenced data products and updates:
  - Wood et al. 2015; Wood et al. 2016 (Earth System Science Data) on woodland surveys and classifications.

## Access considerations and reuse
- Data are organized as discrete, tabular files compatible with GIS and statistical analysis (site, plot, ground flora, soil, and tree/shrub datasets).
- Coordinates and site details enable spatial analyses and cross-dataset integration with other 1960s-era woodland surveys.
- Taxonomic harmonization (Latin names and BRC codes) facilitates long-term ecological comparisons and reproducibility.

## Practical implications for data leadership and use
- Provides a robust, standardized historical dataset suitable for validating current woodland classifications and for methodological comparisons with later surveys.
- Useful for meta-analyses on vegetation structure, species associations, and soil-vegetation relationships in semi-natural woodlands.
- Highlights the value and challenges of long-term data integration: legacy methods, missing values (e.g., 999 for pH), and need for careful taxonomic updates and provenance tracking.
- Demonstrates a clear lineage from local site classification efforts to national-scale woodland surveys, illustrating the role of standardized data collection in building scalable data ecosystems.