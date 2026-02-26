# The provenance trial environment

- Overview
  - The La Petite Charnie provenance trial established by INRA (French National Institute for Agricultural Research) to study oak (Quercus petraea and Quercus robur) provenance performance.
  - Contains almost 200,000 trees: 103 provenances of Q. petraea and 9 provenances of Q. robur from across their natural range.
  - Location: mean elevation ~140 m; Atlantic temperate, wet climate; red sandstone, schist, and clay substrata.
  - Surrounded by mature oak forest with mixed beech, ash, and hornbeam; native oaks from La Petite Charnie not represented in the trial (closest population from Forêt de Bercé, ~50 km away).

- Experimental design and data structure
  - Within each soil zone, provenances are represented by two or three plots, each a replicate set of 24 trees in four columns of six trees.
  - Plant spacing: 1.75 m within columns; 3 m between columns.
  - Blocks: 8 different provenances per block; blocks randomized within soil zones to separate plot, block, soil zone, and provenance effects.
  - Focus on a subset of provenances; block effect not considered; plot position within soil zones treated as random.
  - Each sampled provenance planted in multiple replicate plots across five soil zones; total design includes 200 study plots and 4,800 trees.
  - Soil zones: five distinct zones used in the design.

- Herbivore survey (cynipid gall wasps)
  - Survey scope: 20 selected provenances; gall abundance sampled in 2008 and 2009 (four surveys per year, covering spring and autumn generations).
  - Per plot sampling: galls counted on 12 of 24 trees (edge effects minimized by using the two internal rows of six trees).
  - Method: for each surveyed twig (10 twigs per tree; each twig from the last two years’ growth), identify galls by species and generation in the field using a morphological key.
  - Coverage: 2 plots per soil zone per provenance; 200 study plots; 2,400 trees surveyed for galls (12 galls per tree across generations).

- Nature and units of recorded values
  - Data type: counts (gall counts by species and generation).
  - Key data fields include:
    - Record identifiers and provenance/building blocks: ID, Record ID, ProvCode, ParcelleID, Soile Zone (note: “Soile Zone” in documents), YearGen (generation and year; S/A and 08/09), TreeNo, ShootNo, Shoot ID.
    - Gall counts by species/generation, e.g., AfecAsex, AglanAsex, AsolAsex, NalbAsex, NantAsex, NqbAsex, NnAsex, CdivAsex, CqfAsex, AtestSex, NalbSex, NantSex, NnSex, NqbSex.

- Quality control
  - One-to-one training of data collectors.
  - Double checking for outliers during transcription.

- Data management and reuse considerations for Data Leaders
  - Demonstrates a multi-factor hierarchical experimental design (provenance, soil zone, plot, tree) with replication and blocking considerations.
  - Provides detailed metadata and structured data dictionary for provenance, soil zones, timing (spring/autumn; 2008/2009), and species/generation-specific counts.
  - Highlights data quality practices (training, transcription checks) and documentation notes (e.g., subset of provenances studied, block treatment, randomization).
  - Useful for cross-site or cross-trial comparative analyses of provenance performance and herbivore pressure, as well as integration with environmental context (soil, climate, surrounding forest) for broader data-system planning.