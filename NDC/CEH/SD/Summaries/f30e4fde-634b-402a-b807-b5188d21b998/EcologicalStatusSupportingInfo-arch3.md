# Mapping biodiversity: a spatial indicator based on species occurrence data

- Purpose and scope
  - Develop a spatial indicator of ecological status to inform biodiversity valuation and policy evaluation across the UK.
  - Supports monitoring and future decision-making by summarising biodiversity status at a 10 km2 grid scale (hectads) across the UK.

- Data sources
  - UK species occurrence data from the Biological Records Centre (BRC) for 11 taxonomic groups: bees, birds, bryophytes, butterflies, carabidae, hoverflies, isopoda, ladybirds, moths, orthoptera, and vascular plants.
  - Bird data drawn from the British Trust for Ornithology (BTO) for breeding birds (1976 and 2001-2011 atlases).
  - Spatial unit: 10 km2 hectads; two time periods analyzed: 1970–1990 and 2000–2013.
  - Column data in the output includes gridSquare (Ordnance Survey National Grid), Easting, Northing, dominantLandClass (2007 ITE land classification), and ecologicalStatus.

- Methodology
  - For each taxonomic group and each hectad, compile a species list and calculate species richness per time period.
  - Apply the FRESCALO method to account for variation in recorder effort across hectads.
  - Assign each hectad to an environmental zone using the dominant 2007 ITE land classification (45 classes) based on abiotic conditions (land cover, climate, geology, topography).
  - Develop a reference species list for each environmental zone; compute ecological status as a relative measure of estimated species richness by comparing hectad richness to the zone’s potential richness.
  - Derive a mean ecological status across all taxonomic groups for 2000–2013, relative to the 1970–1990 maximums.
  - Documentation notes that further methodological details are provided in a manuscript in preparation.

- Land classification and zones
  - Uses the 2007 ITE land classification to define 45 environmental zones (mapping of land classes to ecological zones).
  - Details provided for Great Britain, Scotland, and Wales with example classifications (e.g., flood plains, coastal plains, upland valleys, etc.).

- Output and dataset structure
  - EcologicalStatusMap.csv contains:
    - gridSquare: 10 km grid reference.
    - Easting/Northing: coordinates in British National Grid.
    - dominantLandClass: 2007 ITE land class for the hectad.
    - ecologicalStatus: mean ecological status across taxa for the 2000–2013 period (relative measure).

- Temporal framing and comparison
  - Ecological status for 2000–2013 is evaluated relative to the species richness maxima observed in 1970–1990.
  - Two-time-period analysis enables assessment of change in ecological status over time across taxonomic groups and environmental zones.

- Key references and methodological basis
  - Hill, M.O. (2012). Local frequency as a key to interpreting species occurrence data when recording effort is not known. Methods in Ecology and Evolution.
  - Bunce, R.G.H. et al. (2007). ITE Land Classification of Great Britain 2007.

- Relevance to monitoring framework aims
  - Provides a consistent, spatially explicit biodiversity health indicator aligned with policy evaluation needs.
  - Integrates multiple taxonomic groups and accounts for sampling effort, enabling more robust monitoring and trend analysis.
  - Highlights the importance of linked data quality, metadata, and standardized land classification for reproducible monitoring outputs.