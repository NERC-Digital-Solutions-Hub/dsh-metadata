# Litterfall in human-modified forests of Eastern Amazonia

- Overview
  - A dataset named Litterfall.csv containing litterfall measurements from 20 Amazonian forest plots (each 250 x 10 m) across a disturbance gradient: undisturbed primary, logged primary, logged-and-burned primary, and secondary forests.
  - Disturbance classification derived from satellite-based canopy disturbance (1988–2010) and field assessments (fire scars, charcoal, logging debris).
  - Data collected from January 2015 to October 2018 as part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).

- Data collection methods
  - Six litter traps per plot (50 x 50 cm; total area 0.25 m2), placed 1.20 m above ground, arranged 50 m apart.
  - Traps harvested every two weeks from February 2015 to October 2018.
  - Samples labeled and processed in the field lab; separated into leaves, flowers, fruits, seeds, wood, and rest (non-identifiable material).
  - Samples oven-dried at 80°C for 3 days and weighed to the nearest 0.01 g.

- Dataset structure and metadata
  - A comma-separated value file (Litterfall.csv) with the following columns:
    - Catchment: microcatchment (~5,000 ha) where each plot is located
    - Transect: plot number within each catchment
    - Plot: unique code combining catchment and transect
    - Forest_pre_El_nino: disturbance class before the 2015–16 El Niño
    - El_Nino_fire: whether the plot burned during El Niño (1 = fire, 0 = no fire)
    - Litter: trap number within each plot (1–6)
    - Day: date of data collection
    - Team: data-collecting team
    - Leaf (g), Wood (g), Flower (g), Seed (g), Fruit (g), Rest (g): dry weight per category
    - Total (g): total dry weight per trap
    - Notes: field notes
  - Units for all mass measurements are grams; timing spans January 2015 to October 2018.

- Geographic information
  - A list of coordinates for plots (Latitude and Longitude) is provided for each plot (e.g., codes like 112_12, 112_8, 129_10, etc.), detailing precise locations across the study area.

- Data provenance and stewardship context
  - Data originate from field collection in tropical forests and laboratory processing described above.
  - Collected under the HMTF program; associated grant information included in the overview.
  - Clear documentation of data collection timing, plot differentiation, and disturbance history to support reproducibility and reuse.

- Access, format, and reuse considerations
  - Data are provided as a CSV file with explicit column definitions and units.
  - Metadata captures disturbance classification, El Niño event context, and sampling methodology to aid data discoverability and interoperability.

- Quality, limitations, and stewardship implications
  - Weight measurements are precise to 0.01 g; consistent drying and weighing protocol supports comparability across traps and plots.
  - Documentation links disturbance history, fire events, and sampling cadence, enabling robust provenance tracking.
  - For data stewards: ensure ongoing metadata alignment with standard ecological datasets, maintain links to related datasets (e.g., satellite disturbance records), and consider future updates or extensions to capture additional years or plots.