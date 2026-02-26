# Mapping biodiversity: a spatial indicator based on species occurrence data

## Purpose and scope
- Provides a spatial indicator of ecological status for biodiversity valuation across the UK using species occurrence records.

## Data sources
- UK species occurrence data collated from the Biological Records Centre (BRC).
- Tenor: data for 11 taxonomic groups (bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera, vascular plants).
- Bird data sourced from the British Trust for Ornithology (BTO) breeding birds atlases.

## Temporal and spatial resolution
- Time periods: 1970–1990 and 2000–2013.
- Spatial scale: 10 km x 10 km hectads (gridSquares) across the UK.

## Methodology
- Analyses are conducted separately for each time period and each taxonomic group.
- For every hectad: compile a species list and calculate species richness; apply FRESCALO to adjust for uneven recording effort (Hill 2012).
- Ecological status is a relative measure of estimated species richness.
- Environmental zones are defined by land cover, climate, geology, and topography, using the 2007 ITE land classification (45 classes) to assign dominant land class per hectad.
- For each environmental zone, assemble a reference list of potential species; ecological status for a hectad is the observed richness as a proportion of the potential richness for that zone.
- The final ecological status is the mean across all taxonomic groups for 2000–2013, relative to the 1970–1990 maximum richness.

## Data products and dataset structure
- Dataset column headings:
  - gridSquare: Ordnance Survey National Grid 10 km grid reference.
  - Easting: x coordinate of the southwest corner (British National Grid, metres).
  - Northing: y coordinate of the southwest corner (British National Grid, metres).
  - dominantLandClass: Dominant land class for the 10 km square (2007 version).
  - ecologicalStatus: Mean ecological status.
- Outputs designed to enable spatial interpretation of biodiversity status and facilitate further analysis.

## Land Classification 2007
- Uses the 45 ITE land classes from Bunce et al. (2007) to define environmental zones with similar abiotic conditions.
- Classes are summarized with region-specific codes and names for England, Scotland, and Wales (e.g., various floodplain, valley, coastal, upland and plain categories).

## Data provenance and references
- Primary sources: Biological Records Centre (BRC) data, BTO bird atlases (1976 and 2001–2011), ITE Land Classification (Bunce et al. 2007), and the FRESCALO methodology (Hill 2012).
- Note: Further methodological details are to be provided in a manuscript in preparation.