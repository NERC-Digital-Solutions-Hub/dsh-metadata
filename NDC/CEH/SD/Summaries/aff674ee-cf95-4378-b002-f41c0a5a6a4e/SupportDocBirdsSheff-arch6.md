# Experimental design/sampling regime

- The dataset records bird species and counts across 10 green spaces in the Sheffield City Region, with observations of bird activity.
- Each site was surveyed on 3 occasions using 6 pre-designated line transects per location, totaling 10 sites × 6 transects × 3 reps.
- Transect length is 60 meters; surveys occurred in the early morning (05:30–09:30) to capture optimal bird activity.
- Birds were counted along transects within defined distance bands (0–25 m, 26–50 m, 51–100 m) and recorded by common name and BTO code.
- A single experienced ecologist conducted all surveys for consistency, using binoculars to confirm distant sightings.
- The data collection was part of the NERC IWUN Project (Improving well-being through urban nature) and linked to other social science and medical datasets to explore relationships between nature exposure and mental well-being. The study aimed to determine if exposure to biodiversity improved mood/well-being.
- 2775 observations were recorded in total; no data were excluded.

## Study design and data collection

- Data Collection Method:
  - Recording of bird species, counts, activity, and location for each observation.
  - Activity codes include: C (calling), F (in flight), P (present), S (singing); with a corresponding Activity description.
  - Observations are tagged by Site, Transect, Date, Time, VisitNo, and DistanceBand.
- Roles:
  - Ms Riley collected bird data.
  - Drs Cameron and Brindley interpreted results, integrating other datasets for later correlations.
- Data handling:
  - Data were cleaned and quality-checked, with an emphasis on maintaining a consistent methodology across all transects and visits.

## Study sites and timing

- Survey locations (with approximate coordinates):
  - Bolehills Park
  - Botanical Gardens
  - Crookes Valley Park
  - Devonshire Green
  - Endcliffe Park
  - Graves Park
  - Peace Gardens
  - Ponderosa
  - South Street Park
  - Weston Park
- Timing:
  - Surveys conducted in June–July 2018, across three reps with early morning sessions to maximize detection.
  - Each transect line was non-overlapping to ensure spatial independence within each site.

## Data quality and limitations

- Quality control:
  - The data sheet was checked by Ross Cameron for logical consistency.
  - No formal guarantee that individual birds were never counted twice; however, the systematic transect-based approach implies any counting errors would be consistent across the dataset.
- Limitations:
  - Potential for duplicate counts cannot be fully ruled out due to methodology.
  - Data are limited to the 10 selected green spaces and the 3 survey reps within the specified time frame.

## Dataset structure and file details

- File: BirdsSheffAllReps2018.csv
- Columns (11 total):
  - VisitNo: visit number (1, 2, or 3)
  - BTOCode: British Trust for Ornithology code
  - BirdName: common name of bird
  - ActivityCode: code for observed activity (C, F, P, S)
  - Activity: described activity
  - Site: site name
  - Transect: transect number (1–6)
  - Date: date of observation (DD/MM/YYYY)
  - No.Birds: number of birds observed
  - DistanceBand: distance band of observation (0–25 m, 26–50 m, 51–100 m)
  - Time: time band of observation (HH:MM – HH:MM)

## Provenance and project context

- Project context:
  - Part of the NERC IWUN Project aimed at improving well-being through urban nature.
  - Data linked with other social science and medical datasets for broader correlations regarding mental well-being and exposure to urban biodiversity.
- Overall dataset size:
  - 2775 observations across 10 sites, 3 reps, and multiple transects, enabling analyses of bird diversity and abundance by site, time, distance band, and activity.