# Cx pipiens abundance at CEH Wallingford 2015

- Overview
  - Dataset details the seasonal abundance of Culex pipiens across life stages (eggs, larvae, pupae, adults) at the CEH Wallingford field site in 2015.
  - Immature stages sampled three times per week (March–October 2015); adults sampled four times per week (April–October 2015).

- Experimental design, sampling regime, and collection methods
  - Immature sampling
    - Four 450 L circular water butts located close together with varying exposure (sunlight and shelter) to simulate microhabitats.
    - Hay infusion introduced January–March by adding 2 kg hay per butt; bags removed end of March.
    - Egg rafts counted at 10:00 on Mondays, Wednesdays, and Fridays.
    - Larvae and pupae sampled via 500 mL dip from north, south, east, and west edges (not the middle); photos taken for counting when numbers are large.
    - Monthly 4th instar larvae collected for species identification (microscopy after boiling for kill).
  - Adult sampling
    - Four John W. Hock Miniature Downdraft Blacklight (UV) traps baited with dry ice.
    - Traps operated nightly from 14 April to 2 October; five consecutive empty collections halt trapping in yellow locations; generally run four nights per week (Mon–Thu), with some nights missed due to logistics.
    - Traps placed at varying distances (approx. 80–200 m from the butts).
    - Adults preserved and identified to species in the lab; counts recorded for female Cx. pipiens (males not counted).

- Fieldwork and laboratory instrumentation
  - UV traps for adult sampling; dry ice as attractant.
  - Laboratory identification via standard dissection and light microscopy.
  - HOBO weather station for ambient conditions and hourly water temperature loggers for each butt.

- Nature and units of recorded values
  - Eggs: counts of egg rafts per butt per sampling date.
  - Larvae/Pupae: counts per sampling date, per butt, separated by instar categories (L1/2 and L3/4; explicit corner labeling for each butt).
  - Adults: counts of adult female Cx. pipiens per trap per sampling date (other species recorded as Cs. annulata and Ae. geniculatus).
  - Temperature: hourly water temperatures in degrees Celsius per butt.

- Quality control
  - Larval/pupal counts validated by comparing counts from direct tray observations with counts derived from photographed contents; results were consistent.

- Details of data structure (files and key columns)
  - Egg_abundance_2015_Wallingford.csv
    - Columns: Date, Butt (1–4); egg raft counts per date.
  - Larval_and_pupal_abundance_2015_Wallingford.csv
    - Columns organized by butt: N,E,S,W with L1/2 and L3/4 counts; date-stamped.
  - Adult_abundance_2015_Wallingford.csv
    - Columns: Date; Location (trap ID); Cx. pipiens counts; Cs. annulata; Ae. geniculatus; NA entries indicate missing trap data.
  - Larval_identification_2015_Wallingford.csv
    - Columns: Date of 4th instar identification; number identified as Cx. pipiens; Butt origin.
  - Water_temperatures_2015_Wallingford.csv
    - Columns: Date, Time, Butt, Temperature (°C) for hourly surface water temps.
  
- Data gaps and practical notes
  - Some adult trap data recorded as NA due to staff or dry ice delivery issues.
  - Sampling relied on field photos for large counts to facilitate counting accuracy.

- Relevance for monitoring frameworks
  - Provides a multi-stage, time-series, and spatially resolved dataset suitable for:
    - Monitoring population dynamics across life stages.
    - Evaluating environmental drivers (e.g., water temperature) on mosquito abundance.
    - Assessing spatial variation within microhabitats (different butts) and trap locations.
    - Informing policy decisions and future monitoring design with explicit methods, QA steps, and data structure.