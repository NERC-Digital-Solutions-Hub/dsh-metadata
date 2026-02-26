# Experimental design/sampling regime

- Purpose and context
  - Data record bird species and numbers across 10 green spaces (parks) in Sheffield City Region, with activity of individual birds noted.
  - Part of the NERC IWUN Project (Improving well-being through urban nature); aims to correlate bird diversity/abundance with people’s emotions about these places to assess whether exposure to nature improves mental well-being.
  - 2775 observations collected overall; no data excluded.

- Study design
  - 10 green spaces surveyed (parks) with 3 survey repetitions (rep 1 in 6–22 June 2018; rep 2 in 27 June–10 July 2018; rep 3 in 11–18 July 2018).
  - Surveys conducted in the early morning (05:30–09:30).
  - 6 pre-designated line transects per location; transects are 60 m long and non-overlapping.
  - A single experienced ecologist conducted all surveys for consistency.

- Data collection methods
  - Observer recorded birds on either side of transects within distance bands: 0–25 m, 26–50 m, 51–100 m.
  - Birds recorded by common name and BTO code; date and time of observation captured.
  - Activity codes used: C (calling), F (in flight), P (present), S (singing); explicit Activity field included.
  - Binoculars used to verify distant sightings.
  - All observations logged in a single dataset; no data excluded.

- Site locations (with coordinates)
  - Bolehills Park (53.390391, −1.509763)
  - Botanical Gardens (53.371965, −1.497799)
  - Crookes Valley Park (53.383224, −1.492727)
  - Devonshire Green (53.378866, −1.478367)
  - Endcliffe Park (53.368251, −1.507601)
  - Graves Park (53.337137, −1.471532)
  - Peace Gardens (53.379950, −1.469464)
  - Ponderosa (53.385800, −1.489243)
  - South Street Park (53.379135, −1.460122)
  - Weston Park (53.382285, −1.490432)

- Data integration and interpretation
  - Bird data collected by Ms. Riley; results interpreted by Drs. Cameron and Brindley using additional datasets from social science and medical colleagues for later correlations.
  - Objective includes linking wildlife data to human well-being outcomes.

- Quality control and limitations
  - Data sheet checked by Ross Cameron for logical consistency.
  - Potential for double counting is acknowledged, but the systematic methodology implies consistent error across the dataset.
  - No data excluded; all 2775 observations retained.

- Dataset structure
  - File: BirdsSheffAllReps2018.csv
  - Columns: VisitNo, BTOCode, BirdName, ActivityCode, Activity, Site, Transect, Date, No.Birds, DistanceBand, Time
  - Each row represents a single observation episode with the corresponding metadata (location, transect, timing, count, and observed behavior).