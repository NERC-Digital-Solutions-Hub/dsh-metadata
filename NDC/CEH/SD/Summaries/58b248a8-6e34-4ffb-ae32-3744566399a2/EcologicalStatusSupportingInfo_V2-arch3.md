# Mapping biodiversity: a spatial indicator based on species occurrence data

- Overview:
  - A spatial indicator of ecological status for biodiversity across the UK, derived from species occurrence records.
  - Aimed at valuation, policy scrutiny, and informing future decisions on environmental health monitoring.

- Data availability and access:
  - UK ecological status map version 2 available from the Environmental Information Data Centre (ENDC) with DOI: 10.5285/58b248a8-6e34-4ffb-ae32-3744566399a2.
  - Emphasizes openness and public sharing of underlying data, while noting potential governance and metadata considerations.

- Data sources and collation:
  - 11 taxonomic groups: bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera, vascular plants.
  - Spatial unit: 10 km x 10 km grid squares (hectads) across Great Britain and Ireland.
  - Time periods: 1970–1990 and 2000–2013.
  - Data origins:
    - Vascular plants: non-natives excluded due to high non-native proportion in GB.
    - Birds: breeding birds of the UK from the British Trust for Ornithology (BTO).
    - Other groups: collated from Biological Records Centre (BRC).
  - Purpose: build a baseline and assess changes in biodiversity status over time.

- Methodology and indicators:
  - Per taxonomic group and time period, compile species lists for each hectad and calculate species richness.
  - Account for recorder effort variation within hectads using the FRESCALO method (Hill 2012).
  - Ecological status (relative richness): assign each hectad to an environmental zone determined by land cover, climate, geology, and topography.
  - Land classification: 2007 ITE land classification (45 classes) used to define environmental zones (dominant land class per hectad).
  - Reference lists: generate zone-specific potential species lists; compare observed richness to potential to derive relative ecological status.
  - Aggregation: compute mean ecological status across all 11 taxonomic groups for the 2000–2013 period, relative to the 1970–1990 maxima.
  - Key output: a map-based ecological status indicator at hectad resolution, plus underlying data and descriptive metadata.

- Land classification and environmental zones:
  - 2007 ITE land classification provides 45 classes used to group hectads into zones with similar abiotic conditions.
  - Includes a structured list of summary names for the 45 land classes, with regional adaptations for England, Scotland, and Wales.

- Data fields and dataset structure:
  - gridSquare: Ordnance Survey National Grid reference (10 km square).
  - Easting/Northing: grid coordinates (metres) corresponding to the southwest corner of the grid square.
  - dominantLandClass: 2007 ITE land class for the hectad.
  - ecologicalStatus: mean ecological status for the hectad (across taxonomic groups).

- Outputs, interpretation, and use:
  - Provides a standardized, cross-taxonomic biodiversity status indicator suitable for large-scale environmental assessment and policy evaluation.
  - Facilitates comparison across time periods and regions, informing decisions on monitoring priorities and conservation actions.

- Data governance, openness, and challenges:
  - Requires careful data management, metadata, and governance to ensure datasets meet standards, are stored, shared appropriately, and kept up to date.
  - Highlights typical monitoring-framing challenges: data gaps, data access, organizational silos, metadata quality, data transformation needs, and communicating complex results clearly.
  - Addresses some barriers by centralizing access via ENDC and applying transparent methodology and references.

- Key references and supporting materials:
  - Dyer, R.; Oliver, T. (2016). UK ecological status map version 2. NERC ENDC.
  - Hill, M. O. (2012). Local frequency as a key to interpreting species occurrence data when recording effort is not known.
  - Bunce, R. G. H. et al. (2007). ITE Land Classification of Great Britain 2007.