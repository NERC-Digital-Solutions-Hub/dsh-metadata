# BirdsSheffAllReps2018.csv

- Overview
  - A dataset from the NERC IWUN Project (Improving well-being through urban nature) examining bird diversity and abundance in 10 green spaces in Sheffield City Region.
  - 2775 bird observations collected to explore correlations between biodiversity exposure and people’s emotions/feelings about these places (data also linked to other social science and medical datasets for later correlations).

- Experimental design and sampling regime
  - 10 green spaces (parks) surveyed: Bolehills Park, Botanical Gardens, Crookes Valley Park, Devonshire Green, Endcliffe Park, Graves Park, Peace Gardens, Ponderosa, South Street Park, Weston Park.
  - Each site surveyed on 3 occasions (replications 1, 2, 3) in June–July 2018.
  - Data collected via 6 pre-designated line transects per location (60 m each), with transects non-overlapping and stratified to cover all habitats in the space.
  - Surveys conducted in the early morning (05:30–09:30).
  - Observers recorded birds along transects on either side within distance bands (0–25 m, 26–50 m, 51–100 m).
  - Birds recorded by common name and BTO code; date and time logged for each observation.
  - A single experienced ecologist conducted all surveys for consistency and used binoculars to verify distant sightings.
  - Activity data captured (e.g., calling, in flight, present, singing) with codes: C (calling), F (in flight), P (present), S (singing); plus a descriptive Activity field.
  - The project also collected data via a mobile app to relate bird observations to human emotions, enabling correlations with well-being outcomes.

- Collection/Generation/Transformation methods
  - Site coordinates:
    - Bolehills Park (53.390391, -1.509763)
    - Botanical Gardens (53.371965, -1.497799)
    - Crookes Valley Park (53.383224, -1.492727)
    - Devonshire Green (53.378866, -1.478367)
    - Endcliffe Park (53.368251, -1.507601)
    - Graves Park (53.337137, -1.471532)
    - Peace Gardens (53.379950, -1.469464)
    - Ponderosa (53.385800, -1.489243)
    - South Street Park (53.379135, -1.460122)
    - Weston Park (53.382285, -1.490432)
  - Data collection carried out by Ms Riley; results interpreted by Drs Cameron and Brindley using additional datasets collected by social science and medical colleagues for later correlations.
  - No data excluded from the dataset; all observations included.
  - Data stored in a single CSV file (BirdsSheffAllReps2018.csv) with 11 columns.

- Quality control
  - The data sheet was checked for logical consistency by Ross Cameron.
  - No explicit guarantee that individual birds were never counted twice; process assumed consistent across the dataset due to systematic methodology.

- Details of data structure (BirdsSheffAllReps2018.csv)
  - VisitNo: visit number (1, 2, or 3)
  - BTOCode: British Trust for Ornithology code
  - BirdName: common name of the bird
  - ActivityCode: code for observed activity (C - calling, F - in flight, P - present, S - singing)
  - Activity: described activity during observation
  - Site: site name
  - Transect: transect number (1–6)
  - Date: date of record (DD/MM/YYYY)
  - No.Birds: number of birds observed
  - DistanceBand: observation distance band (0–25 m, 26–50 m, 51–100 m)
  - Time: time band of observation (HH:MM – HH:MM)

- Notes on context and interpretation
  - The primary objective is to assess potential links between urban biodiversity exposure and mental well-being, with bird data serving as the ecological component connected to emotion-related data from the mobile app and other datasets.