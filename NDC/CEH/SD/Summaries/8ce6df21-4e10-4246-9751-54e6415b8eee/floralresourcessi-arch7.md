# Data overview: These are records of flower species and their estimated abundances on farmland

- Purpose and GIS relevance
  - Provides spatially referenced records of flower species and their estimated abundances along transects on farmland, enabling map-based analyses and visualisations for policy, clients, or public audiences.
  - Data designed for integration into GIS workflows via coordinates, transect sections, and standard field attributes.

- Spatial and temporal scope
  - Study area: eight farms across Hampshire and West Sussex, England, UK.
  - Transect: a single 3 km transect marked on each farm (established 2013).
  - Habitat types covered along transects: hedgerows, sown seed mixtures for birds/bees, grass margins, and areas left to regenerate.
  - Time periods: surveys conducted in May–August for 2014 and 2018, aligned rounds.

- Sampling design and locations
  - Farm locations provided as precise latitude/longitude coordinates (eight points labeled A–H).
  - Each farm’s transect is divided into distinguishable sections (labels) walked in both 2014 and 2018.

- Data collection and measurement
  - Floral surveys recorded for each transect section.
  - Estimation basis: number of open flowers within a 2 m width on either side of the observer.
  - Flower definition: fully open, including single flowers, umbels/spikes, or capitula.
  - Survey rounds in 2014: three rounds (dates provided); 2018 rounds aligned to 2014 rounds dates.
  - Quality control: counts calibrated between surveyors using photographs with a scaling factor applied to ensure consistency.

- Data structure and content
  - Source file: FloralResources.csv with 11 columns.
  - Key fields:
    - Year: survey year (2014 or 2018).
    - Round: survey round (1, 2, 3) in date order.
    - Type: countryside stewardship agreement (ELS or HLS).
    - Farm: farm identifier (A–H).
    - Label: transect section identifier.
    - What: management type for transect section.
    - Length (m): transect section length.
    - Width (m): surveyed width (2 m indicated in methodology).
    - Family: plant family surveyed.
    - Species: plant species surveyed.
    - Abundance: estimated open flowers surveyed in the transect section.
  - Data units and scope:
    - Abundance is a count estimate per transect section.
    - Spatially anchored to transect sections along the 3 km transect on each farm.

- How this supports GIS work
  - Enables creation of map layers by farm, transect, section, and species with associated abundance values.
  - Facilitates spatial analyses of habitat types, management practices (ELS/HLS), and flowering resource distributions.
  - Allows cross-referencing with habitat features (hedgerows, margins) and stewardship designations for policy or conservation planning.

- Considerations for integration and use
  - Data resolution is tied to transect section boundaries rather than full-coverage grids; appropriate for linear transect and habitat-feature analyses.
  - Coordinate system and precise geolocations are provided for the farm points; transect section geometry can be derived from the labelled sections if not already stored as polygons.
  - Alignment of 2014 and 2018 data enables temporal comparisons of floral abundance under similar sampling regimes.