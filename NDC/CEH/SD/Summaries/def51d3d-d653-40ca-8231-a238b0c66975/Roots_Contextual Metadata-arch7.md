# Root production in human-modified forests of Eastern Amazonia

## Overview
- Dataset of fine root production across 20 plots (each 250 x 10 m) in the Brazilian Amazon, spanning a disturbance gradient: undisturbed primary forests (n=5), logged primary forests (n=5), logged-and-burned primary forests (n=5), and secondary forests (n=5).
- Data collected from Oct 2014 to May 2018.
- Disturbance classification derived from canopy disturbance analysis of satellite imagery (1988–2010) and field assessments of fire scars, charcoal, and logging debris.

## Spatial scope and plots
- Microcatchment context (~5,000 ha) with plots distributed across disturbance classes.
- Precise plot coordinates are provided (20 location codes with latitude and longitude) for GIS mapping and spatial analyses.

## Data collection methods (GIS-relevant)
- In-growth soil cores: four per plot (12 cm diameter x 40 cm deep), placed 50 m apart; cores set 30 cm deep with 10 cm aboveground.
- Sampling schedule per core:
  - First measurement (stock): 24 intervals of 5 minutes each (with 3-minute breaks).
  - 3 months later: second measurement with 12 intervals of 5 minutes.
  - One year later: third measurement using the same method as the second.
  - After one year, a new core is installed ~30 cm away due to soil disturbance; sampling restarts with 24 intervals.
- Field measurements: soil temperature and humidity inside and outside cores; soil homogenized between intervals; cores returned to hole after sampling.
- Laboratory processing: roots washed (2 mm sieve), oven-dried at 60°C for 72 h, weighed.

## Dataset structure and variables (Roots.csv)
- Date: date of data collection.
- Catchment: microcatchment where each plot is located.
- Transect: plot number within each catchment.
- Plot: unique code combining catchment and transect.
- Forest: disturbance class prior to the 2015–16 El Niño.
- Fire_ElNino: whether the plot burned during the 2015–16 El Niño (1 = yes, 0 = no).
- Core number: identifier for each in-growth core.
- Interval: sampling interval number (five-minute blocks).
- Stock: indicator for the first measurement of each core (1 = stock measurement).
- Weight (g): root sample weight.
- Lab_notes: notes from laboratory processing.
- Temperature (inside/outside core): soil temperature in and around the core (°C).
- Humidity (inside/outside core): soil humidity inside and outside the core (%).
- Field notes: notes from field processing.

## How to use in GIS and analyses
- Spatial visualization: map plots by coordinates; symbolize by Forest class and Fire_ElNino status.
- Temporal analysis: assemble time-series of root production by plot, core, and interval across 2014–2018; compare stock vs subsequent intervals.
- Data integration: link Roots.csv with disturbance maps, soil properties, and climate data to explore relationships between disturbance, microclimate, and fine root production.
- Data QA and cleaning: leverage Lab_notes and Field notes for data quality checks; reconcile multiple intervals and cores per plot.

## Data quality, limitations, and notes
- Multi-temporal design across four disturbance categories; potential variability in sampling intervals and core locations over time.
- Spatial resolution limited to plot-level coordinates; finer-scale heterogeneity within plots not directly captured.
- Requires careful handling of mixed units and interpretation of “Stock” vs subsequent interval measurements.
- Metadata provided via the column descriptions aids reproducibility and proper data handling in GIS workflows.