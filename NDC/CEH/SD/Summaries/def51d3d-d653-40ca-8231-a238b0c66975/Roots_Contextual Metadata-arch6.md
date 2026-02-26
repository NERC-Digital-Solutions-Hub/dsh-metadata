# Root production in human-modified forests of Eastern Amazonia

- Overview
  - Dataset Roots.csv contains measurements of fine root production in 20 plots (each 250 x 10 m) across a disturbance gradient in the Brazilian Amazon.
  - Disturbance classes: undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests (n=5 per class).
  - Data collection period: October 2014 to May 2018.
  - Disturbance classification based on canopy disturbance from a satellite image chronosequence (1988–2010) and field assessments (fire scars, charcoal, logging debris).

- Sampling design and field methods
  - Four in-growth soil cores per plot (12 cm diameter, 40 cm deep), placed 50 m apart; cores set 30 cm deep with 10 cm aboveground.
  - Pre-sampling measurements: soil temperature inside and outside the core.
  - Root sampling protocol:
    - First sampling (root stock): 24 intervals of five minutes each (with three-minute breaks); roots cleaned and weighed after lab processing.
    - Second sampling: after 3 months, same method but 12 intervals of five minutes each.
    - Third sampling: after another 3 months (total ~6 months from first), same method as second.
    - One year after the first core, a new core is installed ~30 cm from the first; sampling cycle restarts with 24 intervals.
  - Laboratory processing: roots washed (2 mm sieve), oven-dried at 60°C for 72 hours, and weighed.
  - Core reuse: soil replaced in holes after each sampling.

- Data structure and key variables (Roots.csv)
  - Date: date of data collection
  - Catchment: macro catchment (~5,000 ha) where the plot is located
  - Transect: plot number within each catchment
  - Plot: unique code combining catchment and transect
  - Forest: disturbance class before the 2015–2016 El Niño
  - Fire_ElNino: whether the plot burned during the 2015–2016 El Niño (1 = fire, 0 = no fire)
  - Core number: identifier for the in-growth core
  - Interval: sampling interval number within each core (five-minute blocks)
  - Stock: indicator for the first measurement of a core (1 = stock measurement, 0 = not a stock)
  - Weight (g): weight of each root sample
  - Lab_notes: notes from laboratory processing
  - Temperature (inside the core): soil temperature inside the core before sampling
  - Temperature (outside the core): soil temperature outside the core before sampling
  - Humidity (inside the core): soil humidity inside the core before sampling
  - Humidity (outside the core): soil humidity outside the core before sampling
  - Field notes: notes from field processing

- Coordinates and plots
  - A set of plot-specific coordinates (latitude and longitude) provided for each plot, covering multiple plots within the study area.

- Temporal and spatial scope
  - Spatial coverage: 20 plots across four disturbance classes in Eastern Amazonia.
  - Temporal coverage: measurements from Oct 2014 to May 2018, with sampling at multiple intervals within each core over time.

- Usage and potential analyses
  - Compare fine root production across disturbance classes and over time (stock vs. subsequent intervals).
  - Assess how disturbance history and El Niño-related fire events relate to root production dynamics.
  - Integrate with environmental measurements (temperature and humidity) to explore drivers of root production.
  - Build dashboards or self-service analyses to explore root production patterns by plot, disturbance class, and sampling period.

- Quality and considerations
  - Replication: five plots per disturbance class provide comparative insight, with standardized core sampling and lab procedures.
  - Data notes: includes field and lab notes to aid data interpretation and metadata context.
  - Potential limitations: patchy temporal resolution within cores, reliance on consistent lab processing, and possible missing data in some intervals for certain cores.