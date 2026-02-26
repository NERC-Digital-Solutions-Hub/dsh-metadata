# Root production in human-modified forests of Eastern Amazonia

- The study provides fine root production measurements across 20 plots in the Brazilian Amazon, spanning a disturbance gradient.

- Disturbance classes (5 plots each): undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests.

- Data collection period: October 2014 to May 2018.

Overview of data
- Dataset focuses on belowground production (fine roots) as a key environmental health measure across different forest states.

- Each plot is labeled with a unique code and includes micro-site information to support comparability and transparency.

- The dataset enables assessment of how disturbance history impacts root production over time.

Data collection methods
- In-growth cores: four per plot, each 12 cm diameter x 40 cm deep, with a plastic mesh (mesh size 1.5 cm).

- Core placement: cores placed 50 m apart and positioned 30 cm deep with 10 cm aboveground.

- Sampling protocol:
  - First measurement (stock): 24 intervals of five minutes each (with three-minute breaks) per core; soil homogenized between intervals.
  - Subsequent measurements: repeated at 3-month intervals, with 12 intervals per sampling event.
  - After one year, a new core is installed about 30 cm away from the original one due to soil disturbance; sampling restarts with 24 intervals for the new core.
  - Roots collected, washed, and oven-dried at 60°C for 72 hours, then weighed to obtain root production data.

- Microclimate data: temperature and humidity measured inside and outside each core before sampling.

- Laboratory processing: standardized washing, drying, and weighing procedures to ensure comparability.

Study sites and coordinates
- 20 plots distributed across the disturbance gradient, with plot identifiers (e.g., 112_12, 112_8, 129_10, etc.).

- Each plot has specific latitude and longitude coordinates recorded to enable precise geolocation and reproducibility.

- Plot-level data are linked to forest disturbance class and site metadata (e.g., whether the plot burned during the 2015-16 El Niño).

Data file format and structure
- Primary data file: Roots.csv

- Columns and meanings:
  - Date: date of data collection
  - Catchment: microcatchment (~5,000 ha) containing the plot
  - Transect: plot number within the catchment
  - Plot: unique code combining catchment and transect
  - Forest: disturbance class prior to 2015-16 El Niño
  - Fire_ElNino: binary indicator of whether the plot burned during the El Niño event (1 = fire, 0 = no fire)
  - Core number: identifier for each in-growth core
  - Interval: number of the five-minute interval within a sampling event
  - Stock: indicator for the first measurement of each in-growth core (1 = stock measurement, 0 = not a stock measurement)
  - Weight (g): dry weight of each root sample
  - Lab_notes: laboratory processing notes
  - Temperature (inside the core): internal core temperature (°C)
  - Temperature (outside the core): external temperature (°C)
  - Humidity (inside the core): soil humidity inside the core (%)
  - Humidity (outside the core): soil humidity outside the core (%)
  - Field notes: field processing notes

- The dataset structure supports traceability from field collection through laboratory processing to final measurements, with explicit core and interval identifiers.

Disturbance classification and provenance
- Disturbance categories defined from:
  - Canopy disturbance assessed via a chronosequence of satellite imagery (1988–2010)
  - Field assessments of fire scars, charcoal, and logging debris

- This combination supports cross-site comparisons of root production under different disturbance histories.

Potential uses for monitoring and policy
- Enables evaluation of belowground production responses to different disturbance regimes over multiple time scales.

- The inclusion of metadata fields (Lab_notes, Field notes, core-specific data, and microclimate measurements) supports data governance, quality checks, and transparent reporting.

- Data can inform environmental health monitoring frameworks by providing a replicable protocol and a dataset suitable for inter-site comparisons and trend analyses.