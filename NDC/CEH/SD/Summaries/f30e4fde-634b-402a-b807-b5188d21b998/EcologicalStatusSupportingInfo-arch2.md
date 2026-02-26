# Mapping biodiversity: a spatial indicator based on species occurrence data

## Purpose and application
- Provides a spatial indicator of ecological status for biodiversity valuation across the UK.
- Enables assessment of environmental health and policy performance over time using a consistent, map-based output.
- Targets organisations with established biodiversity monitoring responsibilities and emphasizes standardized, repeatable approaches.

## Data sources and scope
- Data collated from the Biological Records Centre (BRC) for 11 taxonomic groups: bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera, and vascular plants.
- Spatial resolution: 10 km x 10 km squares (hectads) across the UK.
- Time periods: 1970–1990 and 2000–2013.
- Bird data for breeding birds sourced from the British Trust for Ornithology (BTO) using atlas data from 1976 and 2001–2011.

## Methods and analyses
- For each hectad and taxonomic group:
  - Compile a species list and calculate species richness.
  - Apply the FRESCALO method to account for variation in recording effort across hectads.
- Ecological status estimation:
  - Assign each hectad to an environmental zone defined by land cover type, climate, geology, and topography.
  - Use the 2007 ITE land classification (45 classes) to determine the dominant environmental zone for each hectad.
  - Create a reference list of potential species for each environmental zone; compare hectad richness to the zone’s potential richness to derive a relative ecological status.
- Aggregation:
  - Calculate mean ecological status across all 11 taxonomic groups for the 2000–2013 period.
  - Relative to the maximum estimated species richness observed in the 1970–1990 period.
- Note: Further methodological details are to be provided in a manuscript in preparation.

## Data columns and structure
- gridSquare: Ordnance Survey National Grid reference for the 10 km square.
- Easting: x-coordinate of the southwest corner of the grid square (British National Grid, metres).
- Northing: y-coordinate of the southwest corner of the grid square (British National Grid, metres).
- dominantLandClass: Dominant land class for the 10 km square (2007 version) from the ITE classification.
- ecologicalStatus: Mean ecological status for the hectad.

## Land classification 2007 (environmental zones)
- Based on the 2007 ITE land classification (Bunce et al. 2007), comprising 45 land classes used to define environmental zones indicative of similar abiotic conditions.
- Includes regional groupings for England, Scotland, and Wales with code examples (e.g., 1e to 32e in England/Scotland/Wales listings) to reflect varied landscapes such as flood plains, hills, coastal plains, upland valleys, and mountain areas.
- These environmental zones underpin the reference species lists and ecological status calculations.

## Outputs and usage
- Spatial map and dataset of ecological status across the UK for 2000–2013, relative to 1970–1990 benchmarks.
- Datasets intended for storage and upload to appropriate portals as part of standard monitoring outputs.
- Used to support biodiversity valuation and monitoring of environmental health and policy performance over time.

## References
- Bunce, R. G. H., Barr, C. J., Clarke, R. T., Howard, D. C., & Scott, W. A. (2007). ITE Land Classification of Great Britain 2007. NERC-Environmental Information Data Centre. doi:10.5285/5f0605e4aa2a-48ab-b47c-bf5510823e8f
- Hill, M. O. (2012). Local frequency as a key to interpreting species occurrence data when recording effort is not known. Methods in Ecology and Evolution, 3(1), 195-205. doi:10.1111/j.2041-210X.2011.00146.x