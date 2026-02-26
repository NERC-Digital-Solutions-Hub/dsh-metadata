# The provenance trial environment

- Overview
  - The La Petite Charnie provenance trial was established by France’s National Institute for Agricultural Research (INRA).
  - Approximately 200,000 individual trees representing 103 provenances of Quercus petraea and 9 provenances of Quercus robur.
  - Located at mean elevation ~140 m with Atlantic, temperate, wet climate; substrates mainly red sandstone, schist, and clay lenses.
  - Surrounded by mature oak forest and mixed hardwoods; native populations are not represented in the trial (nearest population ~50 km away).

- Trial design and layout
  - Each soil zone contains 2–3 plots per provenance, with 24 trees per plot arranged in four columns of six; spacing 1.75 m within columns and 3 m between columns.
  - 8 different provenances are grouped into blocks; blocks are randomized within soil zones to separate plot, block, soil-zone, and provenance effects.
  - For this subset of provenances, block effects were not considered; plot positions within soil zones treated as random.
  - Each provenance is planted in multiple replicate plots across five soil zones, totaling 200 study plots and 4,800 trees.

- Herbivore survey (cynipid gall wasps)
  - Surveys conducted in 2008 and 2009 across the 20 selected provenances (i.e., subset of plots).
  - Four surveys per year: spring (sexual generation) and autumn (asexual generation) for each year.
  - For each of the 200 plots, galls were surveyed on 12 of the 24 trees (in practice, the two internal rows of six trees per plot).
  - Sampling per tree: 10 twigs selected from the last two years’ growth (identified by ring scars).
  - Galls identified in the field to species and generation using morphology and field experience.

- Nature and units of recorded values
  - Data are counts of galls, separated by gall wasp species and by generation (sexual vs. asexual).

- Quality control and data collection procedures
  - One-to-one training of data collectors.
  - Double-checking for outliers during transcription.

- Data structure and key variables
  - Core identifiers and design metadata:
    - ProvCode (Provenance Code)
    - Soile Zone (1–5) and ParcelleID (plot identifier)
    - YearGen (Generation: S for spring; A for autumn; plus survey year: 08 or 09)
    - TreeNo (Tree ID)
    - ShootNo (Shoot ID for the 10 shoots surveyed per tree)
  - Gall count fields (examples; all are counts):
    - AfecAsex, AglanAsex, AsolAsex, NalbAsex, NantAsex, NqbAsex, NnAsex, CdivAsex, CqfAsex
    - AtestSex, NalbSex, NantSex, NnSex, NqbSex
  - These fields correspond to counts of galls for the asexual and sexual generations of various cynipid species (e.g., Andricus foecundatrix, Andricus glandulae, Neuroterus albipes, Cynips quercusfolii, etc.).

- Context for monitoring and governance relevance
  - Demonstrates a structured, replicated monitoring framework with clearly defined plots, provenance representation, and soil-zone stratification.
  - Integrates longitudinal sampling across two years and two generations of herbivores to assess spatial and temporal patterns.
  - Emphasizes data provenance, metadata completeness, and standardized data collection and quality assurance practices that are central to environmental monitoring and policy evaluation.