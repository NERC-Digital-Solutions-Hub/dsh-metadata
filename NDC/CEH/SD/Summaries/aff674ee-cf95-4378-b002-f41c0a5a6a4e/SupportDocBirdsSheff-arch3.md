# BirdsSheffAllReps2018.csv

## Objective and Context
- Part of the NERC IWUN Project (Improving well-being through urban nature) evaluating whether exposure to nature/biodiversity affects mental well-being.
- Focuses on bird diversity and abundance across 10 green spaces in the Sheffield City Region, linked to emotions/feelings collected via a mobile app.
- 2775 bird observations recorded; data used to interpret relationships between urban biodiversity and well-being.

## Experimental design and sampling regime
- Sites: 10 green spaces (parks) with specified coordinates.
- Sampling: 3 survey repetitions (rep 1, rep 2, rep 3) on pre-designated line transects.
- Transects: 6 transects per site, each 60 m long; transects did not overlap and were selected to represent habitat variety.
- Timing: Surveys conducted in the early morning (05:30–09:30).
- Observation method: Researchers walked along transects noting birds on either side within distance bands (0–25 m, 26–50 m, 51–100 m).
- Data captured: Birds recorded by common name and BTO code; date and time recorded for each observation.
- Team: A single experienced ecologist conducted all surveys to ensure consistency.

## Collection/Generation/Transformation Methods
- Data collected on 10 sites: Bolehills Park, Botanical Gardens, Crookes Valley Park, Devonshire Green, Endcliffe Park, Graves Park, Peace Gardens, Ponderosa, South Street Park, Weston Park.
- Data structure: Each observation includes site, transect, date, time, number of birds, distance band, activity, and species codes.
- Data file: BirdSheffAllReps2018.csv containing 11 columns:
  - VisitNo (1, 2, or 3)
  - BTOCode
  - BirdName
  - ActivityCode
  - Activity
  - Site
  - Transect (1–6)
  - Date (DD/MM/YYYY)
  - No.Birds
  - DistanceBand (0–25 m, 26–50 m, 51–100 m)
  - Time (HH:MM – HH:MM)

## Quality Control
- Data sheet checked by Ross Cameron to ensure logical consistency.
- No explicit guarantee against double-counting; methodology is systematic, allowing an assumption of consistent error potential across the dataset.

## Details of data structure
- CSV file: BirdsSheffAllReps2018.csv
- Columns and meanings (summary):
  - VisitNo: survey replication number
  - BTOCode: standardized bird code
  - BirdName: common name
  - ActivityCode: coded behaviour (e.g., C = calling, F = in flight, P = present, S = singing)
  - Activity: description of activity
  - Site: park name
  - Transect: transect number within site
  - Date: observation date
  - No.Birds: count of individuals observed
  - DistanceBand: observation distance category
  - Time: observation time window

## Relevance for Monitoring Frameworks
- Demonstrates a multi-site, repeated-measure observational design with standardized transects and metadata.
- Emphasizes data quality considerations (consistent observer, post-hoc validation) and the need for clear, defined data structures.
- Highlights potential data governance and sharing considerations (metadata completeness, replication, and transparent methods) relevant to environmental health monitoring initiatives.
- Provides a concrete example of linking biodiversity metrics (bird diversity/abundance) with human well-being outcomes, useful for designing monitoring frameworks that integrate ecological and social data.