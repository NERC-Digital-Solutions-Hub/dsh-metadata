# Mapping biodiversity: a spatial indicator based on species occurrence data

## Overview
- Provides a spatial indicator of ecological status for biodiversity valuation across the UK, derived from species occurrence records.
- Data cover 11 taxonomic groups and use a 10 km grid (hectad) with two time periods: 1970–1990 and 2000–2013.
- Data sources include the Biological Records Centre (BRC) and, for birds, the British Trust for Ornithology (BTO).

## Relevant data files
- EcologicalStatusMap.csv

## Data sources and scope
- UK species occurrence data collated from BRC for 11 taxonomic groups: bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera, and vascular plants.
- Time periods: 1970–1990 and 2000–2013.
- Bird data for breeding birds obtained from BTO (from 1976 and 2001–2011 atlases).
- Data collation supports cross-group ecological status estimation and comparison across zones.

## Methodology (how ecological status is estimated)
- For each hectad and taxonomic group:
  - Compile a species list and calculate species richness.
  - Apply FRESCALO to adjust for variation in recorder effort across hectads.
- Ecological status per hectad:
  - Assign to an environmental zone defined by dominant land class, climate, geology, and topography.
  - Use the 2007 ITE land classification (45 classes) to determine zones.
  - Compile a zone-specific reference list of potential species.
  - Compare observed richness to the potential richness to derive a relative ecological status.
- Aggregation:
  - Compute mean ecological status across all taxonomic groups for the 2000–2013 period, relative to the 1970–1990 period maxima.

## Data structure and metadata
- Dataset column headings:
  - gridSquare: Ordnance Survey National Grid 10 km reference
  - Easting: x-coordinate (metres, British National Grid)
  - Northing: y-coordinate (metres, British National Grid)
  - dominantLandClass: Dominant land class for the 10 km square (2007 version)
  - ecologicalStatus: Mean ecological status
- Additional details: methodology relies on the 2007 land classification to define environmental zones and the relative richness approach.

## Land Classification 2007 (environmental zones)
- Based on the ITE Land Classification of Great Britain 2007 (45 classes) used to assign zones with similar abiotic conditions.
- 45 classes are summarized into named land types (e.g., Flood plains/shallow valleys, Low calcareous hills/variable lowlands, Flat/gently undulating plains, etc.).
- Regional code examples:
  - England: a range of 1e, 2e, 3e, etc.; Scotland: 7s, 13s, 18s, etc.; Wales: 17w1, 17w2, 17w3, 5w, etc.
- Purpose: provide consistent environmental context for comparing ecological status across hectads.

## Practical notes for use and governance
- The document records updates and version history, including datafile naming and column descriptions.
- Methodological details are to be expanded in a manuscript in preparation.
- Data provenance and cross-agency collaboration (BRC and BTO) underpin data quality and reproducibility.

## References
- Bunce, R. G. H., Barr, C. J., Clarke, R. T., Howard, D. C., & Scott, W. A. (2007). ITE Land Classification of Great Britain 2007. NERC-Environmental Information Data Centre.
- Hill, M. O. (2012). Local frequency as a key to interpreting species occurrence data when recording effort is not known. Methods in Ecology and Evolution, 3(1), 195-205.

## Version history
- 14/03/14: Created
- 28/04/14: Corrected datafile name; updated column descriptions
- 02/02/16: Added section on Land Classification 2007