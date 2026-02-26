# Mapping biodiversity: a spatial indicator based on species occurrence data

- Purpose: Provide a spatial indicator of ecological status for UK biodiversity valuation, based on species occurrence records.

- Data scope and sources:
  - 11 taxonomic groups: bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera, vascular plants.
  - Spatial scale: 10 km2 hectads; two time periods (1970–1990 and 2000–2013).
  - Bird data: breeding birds of the UK from BTO atlases (1976 and 2001–2011).
  - Primary data origin: Biological Records Centre (BRC) with supplementary bird data from BTO.

- Methodology:
  - For each hectad and taxonomic group, compile species lists and calculate species richness.
  - Apply FRESCALO to account for variation in recording effort across hectads.
  - Ecological status: relative measure of estimated species richness, linked to environmental zones defined by land cover, climate, geology, and topography.
  - Land classification: dominant land class per hectad determined using the 2007 ITE land classification (45 classes).
  - Reference lists: develop zone-specific potential species lists; ecological status of a hectad is contextualized against this reference.
  - Temporal comparison: derive the mean ecological status across all taxonomic groups for 2000–2013 relative to the maxima from 1970–1990.

- Dataset structure:
  - File: EcologicalStatusMap.csv
  - Key columns:
    - gridSquare: Ordnance Survey National Grid 10 km reference
    - Easting: x-coordinate (metres)
    - Northing: y-coordinate (metres)
    - dominantLandClass: 2007 dominant land class (45 classes)
    - ecologicalStatus: mean ecological status

- Land Classification 2007:
  - Uses the 45 ITE land classes to define environmental zones with similar abiotic conditions.
  - Includes region-specific examples for England, Scotland, and Wales, illustrating diverse landform types (e.g., flood plains, coastal plains, upland valleys, sea cliffs, estuarine/coastal zones).

- References and methodology sources:
  - Bunce, R.G.H. et al. (2007). ITE Land Classification of Great Britain 2007.
  - Hill, M.O. (2012). Local frequency method for interpreting species occurrence data with uneven recording effort (FRESCALO).

- Practical considerations for data leaders:
  - Demonstrates integrating multi-taxa data across time, ensuring data quality, metadata, and discoverability (grid references, land class, ecological status).
  - Supports data-driven policy and biodiversity valuation, enabling spatial and temporal comparisons.
  - Highlights need for consistent land classification standards and comprehensive coverage to reduce data gaps.

- Version control notes:
  - Documented updates include addition of a Land Classification 2007 section and corrections to datafile naming and descriptions, indicating ongoing data curation.