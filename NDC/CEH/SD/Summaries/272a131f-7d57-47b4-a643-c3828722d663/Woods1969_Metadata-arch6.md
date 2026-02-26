# Tree, vegetation and soil information from an ecological survey of semi-natural woodlands in the English Lake District, 1969

## Overview
- A dataset from a 1969 ecological survey of 48 semi-natural woodlands in the Lake District, collecting trees, shrubs, ground flora, and soil data using standardized methods.
- Aimed at enabling analysis of vegetation patterns, site attributes, and soil chemistry across a wide range of woodland types.

## Geographic and temporal coverage
- Geographic focus: Lake District, England
- Time period: June–August 1969
- Sites: 48 woodland sites (including 2 outliers) with precise OS grid references

## Data content and structure
- Data categories
  - Trees: species, diameters at breast height (DBH), heights
  - Shrubs: species, heights, DBH categories, stem counts
  - Ground flora: presence/absence of vascular plants and bryophytes recorded across 10 nests per 20x20 m plot
  - Soil: pH (top 10 cm, multiple nests per plot) and loss on ignition
- Data collection units
  - 48 woodlands, with 6 plots per site (occasionally up to 8), each 20x20 m
  - Each plot includes weather, aspect, slope angle and site observations
  - Nested sampling: 10 nests per plot for vegetation; 2 nests selected for detailed nutrient sampling
- Data tables and fields
  - LAKEDISTRICTWOODS_1969_SITES: site_id, site name, coordinates
  - LAKEDISTRICTWOODS_1969_PLOTS: plot-level context (plot number, date, weather, aspect, slope, coordinates)
  - LAKEDISTRICTWOODS_1969_GROUND_FLORA: species, bryophyte presence, nest-level presence/absence (NEST1–NEST10), QUAD_COUNT
  - LAKEDISTRICTWOODS_1969_SoilPH: soil pH values by nest (nest2, nest4, nest6, nest8, nest10) per plot
  - TREE and SHRUB data: species, DBH_CM, HT_M/HT_FT, D_CODE, TYPE (TREE or SHRUB), with SITE_ID, PLOT, TREE_ID
  - BRC_NAME and BRC_NUMBER: standardized taxonomic naming references
- Data management details
  - Data captured from six randomly placed plots per site; plots divided on a 4x4 m grid
  - Leaves, twigs, and soils collected for chemical analysis; pH measured promptly with a glass electrode; LOI analysis described
  - Original data integration references: association-analysis-based grouping; links to the Woodland Cards and broader woodland surveys
- Data provenance
  - Origin: Woodland Ecology Section, Nature Conservancy – Merlewood, Grange over Sands, Cumbria
  - Primary surveyors listed; data management by Wood, C.
  - Ground flora and soil methodologies align with standard ecological survey procedures of the period

## Methodology and design
- Survey design: 48 woodlands sampled; 6 plots per site (occasionally 8); each plot 20x20 m
- Plot sampling: random placement; recording of date, weather, aspect, and slope angle
- Measurements
  - Trees: DBH for all trees in the plot; heights of tallest trees
  - Shrubs: DBH categories and heights
  - Ground flora: presence/absence in 25 cm x 25 cm nests at 10 intersections per plot
  - Soil: top 10 cm samples for pH and LOI (bulk sample per plot)
- Related work and standard procedures
  - Grounded in the Woodland Cards data and association analysis techniques (presence/absence data used to identify site groups)
  - Findings used to validate site-selection procedures and practical classification with limited detail
  - Influenced subsequent National Woodland Surveys (1971) and related datasets

## Related datasets and publications
- Related datasets and sources
  - Woodland Cards (species presence/absence data)
  - Woodland Survey of Great Britain, 1971
  - Publications: Bunce & Shaw (1973), Williams & Lambert (1959), Allen (1974), and later ESSD papers (Wood et al., 2015; Wood et al., 2016)
- Descriptions and references support data interpretation, classification methods, and lineage to later woodland surveys

## Sites list and spatial context
- 48 site entries with precise OS Grid References (e.g., Addyfield, Arnside Knott, Barton Park, Bigland, etc.)
- Site coordinates enable integration with GIS and spatial analyses

## Data quality, usability, and caveats
- Temporal context: data from 1969; suitable for historical vegetation and site classification studies, not real-time monitoring
- Data granularity: rich, multi-table structure enabling per-site and per-plot analyses; nested vegetation data (10 nests) provide detailed presence/absence patterns
- Measurement details: standardized methods described (DBH, height, pH, LOI); units specified (DBH in cm, height in m/ft)
- Potential use cases
  - Vegetation classification across Lake District woodlands
  - Cross-site comparisons of trees, shrubs, ground flora, and soil chemistry
  - Integration with related national woodland datasets for historical trend analyses

## Access and data dictionary highlights
- Core tables and their purposes
  - LAKEDISTRICTWOODS_1969_SITES: site metadata and locations
  - LAKEDISTRICTWOODS_1969_PLOTS: per-plot context and sampling details
  - LAKEDISTRICTWOODS_1969_GROUND_FLORA: presence/absence of species by nest and plot-level summaries
  - LAKEDISTRICTWOODS_1969_SoilPH: soil pH measurements by nest
  - TREE/SHRUB datasets: species, DBH, height, and structural data
- Taxonomic references linked via BRC_NAME/BRC_NUMBER for standardized naming
- Templates and data entry formats included (Tree Recording Sheet, Shrub Recording Sheet)