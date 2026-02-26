# Definition of sites and plots in this experiment

- Purpose and scope
  - Describes the data structure, field definitions, and measurement protocol for a forest disturbance experiment in Kielder Forest.
  - Aims to support data governance, discoverability, and reuse by ensuring consistent metadata and data capture.

- Data structure and hierarchy
  - Site: Unique site defined by common stand type and topography.
  - Plot: Each plot within a site measured at 50 m2; associated with a site and described by a disturbance-related metric.
  - Transect: Two 10 m transects per plot, located perpendicular to each other, spanning the plot to collect soil samples.
  - Variables (with examples and units when provided):
    - disturbance_score: Categorical score assessing windthrow disturbance level.
    - nitrogen: Soil nitrogen content (%).
    - carbon: Soil carbon content (%).
    - Soil.Moisture: Gravimetric soil moisture (%).
    - root_mg_per_cm3: Dry root mass per soil core (mg per cm3) from a 10 x 10 x 20 cm core.
    - Latitude: Latitude of sample collection.
    - Longitude: Longitude of sample collection.

- Sampling design and measurement details
  - Plots are defined as 50 m2 units within sites.
  - Transects span approximately 200–400 m along known intact and windthrown forest stands; disturbance is assessed every 20 m along each transect (described by a decision tree in Fig 2).
  - Each plot has two transects oriented perpendicularly to capture spatial variability.
  - Measurements collected along transects include soil chemistry, moisture, root mass, and location data.

- Documentation and figures
  - Fig 1: Definition of sites and plots in this experiment.
  - Fig 2: Decision tree for assessing degree of disturbance every 20 m along transects.

- Data governance considerations for Data Stewards
  - Metadata and standards
    - Ensure clear, consistent field definitions and units for all variables (e.g., nitrogen, carbon, Soil.Moisture, root_mg_per_cm3).
    - Document data provenance: sampling design, transect layout, and measurement timing.
  - Quality assurance and consistency
    - Validate accuracy and consistency across sites, plots, and transects.
    - Maintain metadata quality for the categorical disturbance_score and the quantitative soil metrics.
  - Data sharing and accessibility
    - Prepare data for uploading to relevant portals; maintain catalog entries and versioning.
    - Document any sharing limitations and update mechanisms, particularly if sites or plots are added or re-measured.
  - Interoperability and formats
    - Address potential differences across systems/formats when integrating multiple transects or sites.
  - Operational challenges to anticipate
    - Timely data collection from field teams, adherence to standard metadata, and management of large, possibly heterogeneous datasets from many plots and transects.