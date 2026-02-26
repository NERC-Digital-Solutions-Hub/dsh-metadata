# FloralResources.csv: Flower species and abundance on farmland (Hampshire and West Sussex, England, 2014 and 2018)

- Aim and purpose
  - Provides standardized floral resource data to monitor environmental health and policy performance over time.
  - Enables comparison of flower species presence and abundance across years, farm management types, and habitat contexts.

- Study design and scope
  - Location: eight farms across Hampshire and West Sussex, England.
  - Transects: one 3 km transect per farm, established in 2013; transects cover diverse habitats (hedgerows, sown seed mixtures targeting birds/bees, grass margins, natural regeneration).
  - Temporal coverage: surveys conducted in 2014 and 2018, with three rounds per year aligned to similar calendar windows (May–Aug).

- Data collection and measurement
  - Floral surveys along each transect section; three rounds per year.
  - Recording: for each transect section, identify flower species and estimate the number of open flowers within 2 m on either side of the observer.
  - Flower definition: a fully open flower, including flowers on umbels/spikes or capitula.
  - Spatial units: sections along transects are consistently retained across years.

- Quality control
  - Estimated counts calibrated between surveyors using photograph-based counts to derive a scaling factor for standardisation.

- Data structure and fields
  - Data file: FloralResources.csv with 11 columns.
  - Columns and meaning:
    - Year: collection year (2014 or 2018)
    - Round: survey round (1, 2, 3)
    - Type: countryside stewardship agreement (ELS or HLS)
    - Farm: farm identifier
    - Label: transect section identifier
    - What: management type for the section
    - Length (m): transect section length
    - Width (m): transect section surveyed width
    - Family: plant family
    - Species: plant species
    - Abundance: estimated abundance of open flowers in the section

- Spatial and temporal metadata
  - Precise farm locations and transect details are documented (eight farms; coordinates provided for labeling).
  - Survey rounds are aligned between 2014 and 2018 to ensure comparability.

- Data use and accessibility
  - Data are structured for extraction into analyses, maps, and charts to illustrate environmental health trends over time.
  - Datasets are intended to be stored and uploaded to appropriate data portals; standardized QA supports reuse and integration with other environmental datasets.

- Potential analyses for environmental monitoring
  - Temporal comparisons of species richness and flowering abundance by farm, habitat type, and management (ELS vs HLS).
  - Linking floral resource availability to habitat management practices and landscape context.
  - Aggregation by transect sections to assess spatial patterns of floral resources across the study area.