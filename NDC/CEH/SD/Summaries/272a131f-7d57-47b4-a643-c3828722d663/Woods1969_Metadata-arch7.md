# Tree, vegetation and soil information from an ecological survey of semi- natural woodlands in the English Lake District, 1969

## Overview
- Survey of 48 semi-natural woodlands in the English Lake District conducted in June–August 1969.
- Data collected from nearly 300 plots across the Lake District (and sites in the NW of England) using standardized methods.
- Datasets cover vegetation (vascular plants, bryophytes), trees, shrubs, ground flora, and soils (pH, loss on ignition).

## Spatial scope and data structure
- Geographic coverage: Lake District, England.
- Location data available at multiple levels:
  - LAKEDISTRICTWOODS_1969_SITES: site-level data with SITE_ID, site name, OS grid coordinates (POINT_X, POINT_Y), and OS grid references.
  - LAKEDISTRICTWOODS_1969_PLOTS: plot-level data within each site (plot number, site association, OS coordinates).
  - LAKEDISTRICTWOODS_1969_GROUND_FLORA: nest-level ground flora presence/absence within each plot.
  - LAKEDISTRICTWOODS_1969_SoilPH: soil pH values by nest/sample within plots.
  - TREE data: tree/shrub information linked by SITE_ID and PLOT, with species, DBH, height, and other descriptors.
- Data tables use a consistent schema across plots, nests, and sites, enabling GIS joins across spatial and attribute data.

## Sampling design and collection methods
- 48 woodland sites selected; 6 (occasionally 8) plots sampled per site, each plot measuring 20 m x 20 m.
- Within each plot:
  - Trees: species and DBH measured; heights of tallest specimens recorded.
  - Shrubs: species and DBH categories recorded; heights of tallest shrubs measured.
  - Ground flora: presence/absence recorded at 10 random nest intersections (25 cm x 25 cm each).
  - Bryophytes recorded for the whole plot.
  - Soil: top 10 cm sampled at 5 points (aligned with vegetation nests 2, 4, 6, 8, 10) for pH (using a glass electrode) and LOI (loss on ignition) analysis.
- Plot sampling grid and nest-based recording provide fine-grained spatial data suitable for map-based visualization.

## Datasets and content details
- LAKEDISTRICTWOODS_1969_PLOTS: locations, plot numbers, site associations, observer, date, weather, aspect, slope angle, and approximate coordinates.
- LAKEDISTRICTWOODS_1969_SITES: site-level locations with wood IDs, names, and grid coordinates.
- LAKEDISTRICTWOODS_1969_GROUND_FLORA: species-level presence/absence data across nests (NEST1–NEST10), including taxonomic name mappings (BRC_NAME) and bryophyte flags (BRYO).
- LAKEDISTRICTWOODS_1969_SoilPH: soil pH values by nest, within each plot and site (with quality notes).
- TREE data: per-tree/per-shrub records including SITE_ID, PLOT, SPECIES, DESCRIPTION, DBH_CM, HT_M, and status (D for dead stems, etc.).
- Taxonomic references and data standards referenced (e.g., BRC Name mapping, Latin names) with notes on standardization and links to broader species libraries.
- Templates: Tree Recording Sheet and Shrub Recording Sheet templates provided.

## Data provenance and related sources
- Originator: Woodland Ecology Section, Nature Conservancy - Merlewood.
- Background and context: linked to the Merlewood and national woodland surveys; methodology aligned with standardized ecological survey procedures from the era (e.g., Bunce & Shaw 1973; Williams & Lambert 1959).
- Related datasets: Woodland Survey of Great Britain, 1971; subsequent Earth System Data publications (2015–2016) documenting related survey data.

## Usage and GIS considerations
- Suitable for map-based visualization of species distributions, canopy structure, ground flora presence, and soil properties across Lake District woodlands.
- Spatial integration:
  - Site-level coordinates enable broad mapping of woodland distribution.
  - Plot-level coordinates allow precise mapping of sampling locations within each site.
  - Ground flora and soil data are nest-level and plot-level, requiring joins to plot/site for GIS analyses.
- Temporal context: data reflect ecological conditions in 1969; suited for historical comparisons or baseline assessments.
- Data quality considerations:
  - Older dataset; ensure alignment with modern coordinate systems (OSGB36 is used in the source).
  - Nested data (nests within plots) requires careful relational joins to avoid duplications.
  - Taxonomic names may require reconciliation with current nomenclature.

## Access and references
- Core dataset components are organized into plots, sites, ground flora, soil pH, and tree/shrub data with detailed field descriptors and measurement methods.
- References for further context and standardized methods are provided within the background information and publications list.