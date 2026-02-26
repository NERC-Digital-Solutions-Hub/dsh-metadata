# WildCrickets05A-CaptureRecapture Description of content

- Purpose: Provides basic information on each male adult cricket tagged in the population for capture-recapture analysis.

- Key fields and meanings:
  - Year: the year the cricket was alive.
  - ID: individual identification.
  - Birth: day of birth relative to the first adult cricket emergence that year (0 indicates unknown birth date).
  - Death: date of death relative to the birth date of the first adult cricket emerging that year.
  - Recapture days: values range from 2 to 99; represents recapture days (timing of recapture events).

- Data quality and interpretation:
  - Birth date may be unknown when Birth = 0.
  - Death is relative to the first emergence date; absolute dates require knowledge of that first emergence date.
  - Recapture days provide temporal capture history but require alignment with birth/death for complete life-history context.

- GIS/data preparation implications:
  - If spatial coordinates are available, join by ID to map individuals and analyze spatial patterns of recapture.
  - If only temporal data exists, create time-enabled analyses of birth, death, and recapture events.
  - Transformations to perform:
    - Absolute birth date = first emergence date + Birth days.
    - Absolute death date = absolute birth date + Death offset.
    - Derive lifespan and capture histories from Recapture days.
  - Handle missing/unknown values (e.g., Birth = 0) appropriately in analyses.

- Potential uses and analyses in GIS context:
  - Visualize temporal patterns of emergence and survival.
  - Conduct capture-recapture modeling to estimate population size and dynamics.
  - Integrate with environmental or spatial covariates for spatial-temporal analyses if location data are available.