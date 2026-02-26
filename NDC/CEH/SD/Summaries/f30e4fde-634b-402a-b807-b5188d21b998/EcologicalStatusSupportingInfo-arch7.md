# Mapping biodiversity: a spatial indicator based on species occurrence data

- Purpose: A spatial indicator of ecological status for biodiversity valuation across the UK, derived from species occurrence records and presented as a map-based dataset.
- Target audience: GIS users and biodiversity professionals who need to explore ecological status across the landscape.

## Data sources and scope

- Taxonomic coverage: 11 groups (bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera, vascular plants).
- Spatial resolution: 10 km × 10 km hectads.
- Time periods:
  - 1970–1990 baseline
  - 2000–2013 current period
- Bird data: Breeding birds data for the UK from the British Trust for Ornithology (BTO), corresponding to 1976 and 2001–2011 atlases.
- Source data collated from the Biological Records Centre (BRC).

## Methodology and indicators

- Per-hectad calculations:
  - Compile a species list for each hectad and taxonomic group; compute species richness.
  - Apply the FRESCALO method to account for variation in recording effort across hectads.
- Ecological status calculation:
  - Assign each hectad to an environmental zone based on dominant land cover, climate, geology, and topography.
  - Environmental zones defined using the 2007 ITE land classification (45 classes).
  - For each zone, compile a reference list of potential species.
  - Compare hectad estimated richness to the zone’s potential species list to derive a relative ecological status.
  - Compute the mean ecological status across all taxonomic groups for 2000–2013, relative to the maximum richness observed in 1970–1990.
- Output focus: A relative ecological status per hectad that reflects biodiversity status and inform valuation across the landscape.

## Dataset structure and key fields

- Main file: EcologicalStatusMap.csv
- Columns:
  - gridSquare: Ordnance Survey National Grid reference for the 10 km square.
  - Easting: x-coordinate (metres) of the southwest corner in British National Grid.
  - Northing: y-coordinate (metres) of the southwest corner in British National Grid.
  - dominantLandClass: Dominant 2007 land class for the 10 km square (from Bunce et al. 2007).
  - ecologicalStatus: Mean ecological status (relative metric).

## Land Classification 2007

- Basis for environmental zones: The 2007 ITE land classification (Bunce et al. 2007), comprising 45 land classes used to group hectads by abiotic conditions.
- Classification scope:
  - England: multiple 1e–32e classes with region-specific labels
  - Scotland: 7s–32s classes
  - Wales: 5w–18w classes
- The 45 classes underpin the zone-specific reference species lists used to interpret richness.

## References

- Bunce, R. G. H., Barr, C. J., Clarke, R. T., Howard, D. C., & Scott, W. A. (2007). ITE Land Classification of Great Britain 2007. NERC- Environmental Information Data Centre.
- Hill, M. O. (2012). Local frequency as a key to interpreting species occurrence data when recording effort is not known. Methods in Ecology and Evolution, 3(1), 195–205.

## Notes for GIS practitioners

- The indicator provides a relative ecological status suitable for thematic mapping and comparing biodiversity status across the UK.
- Data integration aspects:
  - Combines multiple taxa and time periods with effort-corrected richness estimates.
  - Requires environmental-zone assignment and reference lists to contextualize observed richness.
- Limitations and future work:
  - Methodology details are described in the associated manuscript (further details forthcoming in an in-preparation publication).