# Mapping biodiversity: a spatial indicator based on species occurrence data

- Purpose: Provides a spatial indicator of ecological status for biodiversity valuation across the UK, derived from species occurrence records and suitable for map-based analysis in GIS.

- Temporal and spatial scope:
  - 10 km grid (hectad) scale across the UK.
  - Two time periods: 1970–1990 and 2000–2013.
  - Includes 11 taxonomic groups: bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera, and vascular plants.
  - For vascular plants, non-native species are excluded.

- Data sources:
  - Species occurrence data from Biological Records Centre (BRC) for all groups.
  - Bird data from the British Trust for Ornithology (BTO) (breeding birds; 1976 and 2001–2011 atlases).

- Methodology (GIS-focused overview):
  - For each hectad and time period, compile species lists and calculate species richness per taxonomic group.
  - Apply FRESCALO to adjust for variation in recorder effort across hectads.
  - Assign each hectad to an environmental zone using the dominant 2007 ITE land classification (45 classes).
  - Build a reference species list per environmental zone; compute ecological status as the observed richness proportion relative to the zone’s potential richness.
  - Derive the mean ecological status across all taxonomic groups for 2000–2013, relative to the 1970–1990 maximums.
  - Primary methodological reference: Dyer et al. (2016); additional methodology details in Dyer & Oliver (2016).

- Data fields / dataset structure:
  - gridSquare: 10 km grid reference (Ordnance Survey National Grid).
  - Easting: x coordinate (metres) in British National Grid.
  - Northing: y coordinate (metres) in British National Grid.
  - dominantLandClass: dominant 2007 ITE land class for the 10 km square.
  - ecologicalStatus: mean ecological status for the hectad.

- Land Classification 2007 (ITE 45 classes):
  - Land classes derived from the 2007 ITE land classification used to define environmental zones with similar abiotic conditions.
  - Summary names provided for the 45 classes (examples include flood plains, low calcareous hills, flat plains, coasts, upland valleys, etc.), with regional variants for England, Scotland, and Wales.

- Data availability and provenance:
  - UK ecological status map version 2 is available from the Environmental Information Data Centre (EIDC).
  - DOI: 10.5285/58b248a8-6e34-4ffb-ae32-3744566399a2

- Key references:
  - Bunce et al. (ITE Land Classification of Great Britain 2007)
  - Dyer & Oliver (UK ecological status map version 2; 2016)
  - Hill (2012) on interpreting species occurrence data with uneven recording effort

- Notes for GIS applications:
  - The indicator is a relative measure, enabling comparison of ecological status across hectads and time periods.
  - Data fusion involves handling two temporal snapshots and aligning by 10 km grid with environmental zones.
  - The dataset supports map-based visualization of biodiversity status and can inform site-specific assessments (e.g., impact studies like shale gas discussions as explored in related work).