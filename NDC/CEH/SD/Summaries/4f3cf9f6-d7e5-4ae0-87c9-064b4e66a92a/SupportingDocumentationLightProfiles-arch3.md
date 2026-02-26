# Vertical profile data of light transmission in Atlantic forests along a disturbance gradient

- Purpose and context: This dataset supports tropical forest light regime analyses in human-modified landscapes (associated with Fauset et al., Ecosphere). It provides vertical profiles of light transmission across an intact, logged, secondary, and fragmented montane humid Atlantic forest in Brazil.

- Study site and landscape context:
  - Núcleo Santa Virginia, Serra do Mar State Park, São Paulo, Brazil.
  - Montane moist dense forest with steep topography; inland areas are pastoral with pockets of privately owned forest.
  - Disturbance gradient includes continuous forest within the park and two nearby fragments (edge and interior) adjacent to cattle pasture.
  - Plot types: four plots in continuous forest (intact-K, intact-M, logged, secondary) and two fragments (fragment-C, fragment-L).

- Sampling design:
  - 1-hectare permanent forest inventory plots inside the park (established under Biota Functional Gradients) and additional plots within fragments outside the reserve.
  - In continuous forest: 4 plots, sampled as described; in fragments: 2 plots with edge and interior transects (approximately 30 m from edge and 100 m from edge, respectively).
  - For fragments, historical context suggests long-standing forest cover for fragment-C since before 1962; fragment-L has mixed past land use.
  - Within each plot, 10 sampling locations were surveyed across subplots to cover the light environment; at least 20 m between sampling locations to ensure independence.

- Light profile measurements:
  - 19 PAR sensors built with GaAsP photodiodes, calibrated against a LI-COR 190 sensor.
  - One sensor served as open-sky reference; additional sensors connected to multiplexers and data loggers to record simultaneously.
  - Profiles measured by suspending sensors at 1 m intervals along a rope; data collected every 30 seconds and averaged per minute.
  - Top-of-tree height measured where possible; in some cases the topmost sensor lay below the crown, requiring interpolation for higher portions.

- Fieldwork timing and procedures:
  - Field data collection conducted March–October 2016.
  - At each sampling point, a 20 x 20 m subplot (10 x 10 m for fragments) was selected under stratified design; the tallest suitable tree determined sensor placement.
  - At least one hour and up to three days of measurements per point, ensuring periods of diffuse light (overcast, dawn/dusk) to minimize sunfleck effects.
  - Height measurements taken with laser rangefinder, hypsometer, or visual estimation.

- Data and metadata structure:
  - ProfilesMetadata.csv: includes Plot name, plot code (ForestPlots.net), latitude/longitude, plot area, fragment area, ProfileID, dates of data collection (DD/MM, 2015), and estimated top-tree height.
  - Profiles.csv: per-point, per-height % transmission data with fields for height above ground, plot identifier, interpolation/extrapolation flags (i for interpolated, e for extrapolated), standard deviation, and top/depth indicators.
  - MeanHeightProfiles.csv: plot-level mean % transmission by height above ground, with standard deviations.
  - MeanDepthProfiles.csv: plot-level mean % transmission by depth below canopy top, with standard deviations.

- Data processing and transformations:
  - Diffuse-condition filtering to avoid sunflecks; compute mean % transmission relative to open-sky reference for each sensor.
  - Mean profiles produced by averaging across sampling points for each height (1 m intervals). For fragments, edge and interior data are combined.
  - Handling of unsampled sections:
    - If the highest sensor is below the canopy top, interpolate linearly to 100% transmission at the canopy top.
    - If the bottom sensor is above 1 m, assume transmission below the bottom sensor equals the bottom value.
  - Depth-based profiles (0 m at canopy top) include data down to the plot’s mean sample tree height; extrapolate downward if trees are shorter than the plot mean height.
  - Two profile representations provided: height-above-ground and canopy-depth-based, with corresponding mean transmissions and standard deviations.

- Relevance for monitoring frameworks:
  - Demonstrates a rigorous protocol for capturing vertical light regimes across disturbance gradients, enabling assessment of habitat-light environments for forest health and biodiversity monitoring.
  - Highlights data standards and required metadata, sensor calibration, and provenance critical for data reuse, replication, and comparability across monitoring programs.

- Data quality, accessibility, and governance considerations:
  - Requires careful management of metadata, calibration records, and documentation of interpolation/extrapolation decisions to ensure transparency.
  - The need to share underlying data openly (where possible) and to manage data governance (versioning, provenance, and data stewardship) aligns with monitoring framework best practices, while recognizing potential barriers such as data access, fragmentation, or inconsistent metadata.