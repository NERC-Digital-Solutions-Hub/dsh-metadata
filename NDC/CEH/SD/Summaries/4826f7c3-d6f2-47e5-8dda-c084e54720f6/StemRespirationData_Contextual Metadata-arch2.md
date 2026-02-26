# Stem respiration in human-modified forests of Eastern Amazonia

- Purpose and scope
  - A dataset describing stem respiration in 20 Amazonian forest plots (each 250 x 10 m), spanning a gradient of prior human disturbance (undisturbed primary, logged primary, logged-and-burned primary, and secondary forests).
  - Data collected to understand how stem CO2 efflux varies with forest disturbance and over time, as part of the NERC Human-modified Tropical Forests Programme (HMTF).

- Data collection methods
  - Stem collars installed in at least 13 trees per plot, 20 cm above dendrometers.
  - Trees stratified into five DBH classes (10–19.99 cm, 20–29.99 cm, 30–39.99 cm, 40–49.99 cm, ≥50 cm).
  - PVC collars (~5 cm tall, 10 cm diameter) connected to an infrared gas analyser (EGM5) to measure stem CO2 efflux.
  - Measurements taken every 3 months; if a tree died, the collar was removed and a new collar installed in the same size class, preferably with a dendrometer in place.
  - N/A entries indicate missing data; field notes provide additional context.

- Temporal and spatial coverage
  - Timeframe: June 2015 to July 2018.
  - Spatial context: plots distributed across catchments with recorded latitude/longitude coordinates for each plot (examples include coordinates for plots such as 112_12, 112_8, 129_10, etc.).

- Data structure and contents
  - Data file: StemRespirationData.csv (comma-separated values).
  - Key columns:
    - Date: Date of data collection
    - Catchment: Microcatchment (~5,000 ha) containing the plot
    - Transect: Plot number within each catchment
    - Plot code: Unique code combining catchment and transect
    - Forest: Forest disturbance class before the 2015–16 El Niño
    - Fire: Whether the plot burned during the El Niño (1 = fire, 0 = no fire)
    - Tree TAG: Identifier for the individual with the collar
    - Time: Exact sampling time
    - Collar height: Height of the collar at sampling
    - CO2 initial: CO2 concentration at the start of measurement
    - CO final: CO2 concentration at the end of measurement
    - Flux: Measured stem CO2 efflux
    - Field notes: Field processing notes
  - Dataset includes both disturbance class and fire history, enabling analyses of how disturbance and fire influence stem respiration over time.

- Provenance and accessibility
  - Data collected as part of the NERC HMTF program (Grant NE/K016431/1).
  - The dataset is provided as StemRespirationData.csv, with detailed metadata and notes clarifying measurement conditions and data gaps.

- Potential uses for environmental monitoring and policy analysis
  - Standardized, time-resolved measurements of stem respiration across disturbance gradients support assessment of forest carbon dynamics and responses to human modification.
  - Enables data quality assurance, cross-plot comparisons, and integration with other environmental datasets.
  - Useful for monitoring environmental health and informing policy regarding forest disturbance, fire impact, and carbon cycling in tropical forests.

- Notes on data qualifiers
  - “N/A” denotes missing data; field notes may contain additional context for specific measurements or exclusions.