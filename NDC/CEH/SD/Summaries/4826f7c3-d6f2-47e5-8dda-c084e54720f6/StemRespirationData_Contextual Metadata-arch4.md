# Stem respiration in human-modified forests of Eastern Amazonia

- Dataset summary
  - StemRespirationData.csv contains stem respiration measurements from trees across 20 Amazonian forest plots (250 m x 10 m each).
  - Plots span a gradient of prior human disturbance (before the El Niño event) and are categorized as: undisturbed primary forests (n=5), logged primary forests (n=5), logged-and-burned primary forests (n=5), and secondary forests (n=5).
  - Disturbance classifications are based on canopy disturbance analysis from satellite imagery (1988–2010) and field assessments of fire scars, charcoal, and logging debris.
  - Data collection period: June 2015 to July 2018.
  - Part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).

- Data collection methods
  - At least 13 trees per plot fitted with stem collars, positioned ~20 cm above dendrometers, across five DBH classes (10–19.99 cm, 20–29.99 cm, 30–39.99 cm, 40–49.99 cm, ≥50 cm).
  - PVC collars (~5 cm high, 10 cm diameter) connected to an infrared gas analyser (EGM5) to measure stem CO2 efflux (stem respiration).
  - Measurements taken every 3 months; if a tree died, its collar was removed and replaced on a tree in the same size class (preferably with a dendrometer installed).
  - N/A entries in the dataset indicate missing measurements, with reasons recorded in the notes column.

- Spatial and temporal details
  - Plot locations with precise coordinates are provided (latitude/longitude) for each plot.
  - Data capture time is listed per sample in the “Time” column.
  - Catchment and plot codes uniquely identify each plot; each plot combines catchment and transect identifiers.

- Data structure and fields (csv)
  - Date: Date of data collection
  - Catchment: Microcatchment (~5,000 ha) housing the plot
  - Transect: Plot number within the catchment
  - Plot code: Unique code combining catchment and transect
  - Forest: Disturbance class prior to the 2015–16 El Niño
  - Fire: Whether the plot burned during the 2015–16 El Niño (binary: 1 = yes, 0 = no)
  - Tree TAG: Identifier for the individual with the collar
  - Time: Exact sampling time
  - Collar height: Height of the collar at sampling
  - CO2 initial: CO2 concentration at the start of measurement
  - CO2 final: CO2 concentration at the end of measurement
  - Flux: Measured stem respiration flux
  - Field notes: Field processing notes for the sample

- Data quality, limitations, and provenance
  - Data are derived from a standardized protocol across plots, aiding comparability across disturbance classes.
  - Some measurements are marked as N/A with reasons documented in the field notes, indicating data gaps.
  - Disturbance classification combines historical satellite analysis and on-the-ground assessments, with the 2015–16 El Niño used to flag fire events.

- Relevance for data governance and leadership
  - Clear metadata and structured fields support discoverability, provenance tracking, and reproducibility.
  - Demonstrates integration of ecological measurements with disturbance history to enable cross-plot analyses.
  - The dataset exemplifies robust data collection practices: stratified sampling, standardized instrumentation, quarterly temporal cadence, and explicit handling of missing data.
  - Potential for cross-domain collaboration by linking with other environmental and disturbance data within the HMTF framework.

- Potential uses
  - Analyze how stem respiration flux varies with disturbance type, fire history, and tree size (DBH classes).
  - Compare respiration dynamics across undisturbed, logged, burned, and secondary forests.
  - Integrate with broader ecological datasets to study ecosystem respiration responses to human modification in tropical forests.