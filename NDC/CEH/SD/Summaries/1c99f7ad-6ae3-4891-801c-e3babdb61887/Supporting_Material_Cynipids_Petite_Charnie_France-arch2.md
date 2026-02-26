# The provenance trial environment

## Overview
- Describes the La Petite Charnie provenance trial established by INRA to study oak species Quercus petraea and Quercus robur.
- Contains about 200,000 trees representing 103 Q. petraea and 9 Q. robur provenances from across their natural range.
- Location: La Petite Charnie (mean elevation ~140 m) with Atlantic, temperate, wet climate; red sandstone, schist, and clay substrata.
- Surroundings: mature oak forest with mixed species; native populations not represented in the trial (closest native population ~50 km away).

## Study Design and Sampling
- Experimental layout:
  - Within each soil zone, provenances are represented by 2–3 plots (replicates) of 24 trees planted in four columns of six.
  - Plot spacing: 1.75 m within columns; 3 m between columns.
  - 8 different provenances per block aggregated into blocks to enable separation of plot, block, soil-zone, and provenance effects.
  - Across five soil zones, each provenance planted in multiple replicate plots (total: 200 plots, 4,800 trees).
- Block considerations:
  - Due to focusing on a subset of provenances, block effect was not considered; plot positions within soil zones treated as random.

## Herbivore Survey (Galls)
- Target group: Cynipid gallwasps with broad Western Palaearctic distributions.
- Sampling period: 2008 and 2009; four surveys per year (spring and autumn generations).
- Per plot sampling: 12 of 24 trees surveyed (edge effects minimised by selecting two internal rows per plot).
- per-tree sampling: 10 twigs per tree, each twig representing the last two years’ growth.
- Data collection: Galls identified to species and generation in the field using morphological keys and field experience.

## Data Collected and Measures
- Primary units: Counts (gall counts per twig per tree).
- Generations measured: Asexual and sexual generations for multiple Cynipid species (e.g., Andricus, Neuroterus, Cynips).
- Data captured per twig/tree: Counts for each species-generation combination (e.g., AfecAsex, AglanAsex, AsolAsex, NalbAsex, etc.; AtestSex, NantSex, NnSex, NqbSex).

## Quality Control and Data Management
- Quality control:
  - One-to-one training of data collectors.
  - Double checking for outliers during transcription.
- Data management emphasis:
  - Structured, standardized data collection to enable downstream analyses across plots, soil zones, and provenances.

## Data Structure and Variables
- Core identifiers:
  - ID, RecordID, ProvCode, Soile Zone (typo in source; intended as SoilZone), ParcelleID, Part of the trial design, YearGen (generation and survey year), TreeNo, ShootNo, ShootID (for the dataset of 10 shoots per tree).
- Sampling detail fields:
  - AfecAsex, AglanAsex, AsolAsex, NalbAsex, NantAsex, NqbAsex, NnAsex, CdivAsex, CqfAsex (counts of asexual generation for various species)
  - AtestSex, NalbSex, NantSex, NnSex, NqbSex (counts of sexual generation for various species)
- Structure supports analysis by provenance, soil zone, plot, tree, and shoot with year/generation context.