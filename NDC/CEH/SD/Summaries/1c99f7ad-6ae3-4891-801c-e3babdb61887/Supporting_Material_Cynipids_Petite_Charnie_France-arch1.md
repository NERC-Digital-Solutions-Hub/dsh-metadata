# The provenance trial environment

## Overview
- The La Petite Charnie provenance trial was established by France's INRA.
- Contains ~200,000 trees representing 103 provenances of Quercus petraea and 9 provenances of Quercus robur.
- Location features: mean elevation ~140 m; Atlantic, temperate, wet climate; substrates include red sandstone, schist, and clay lenses.
- Surrounded by mature oak forest mixed with Fagus sylvatica, Fraxinus excelsior, and Carpinus betulus.
- Nearby native populations (e.g., Forêt de Bercé) are not directly represented in the trial.

## Experimental design
- Within each soil zone, provenances are represented by 2–3 plots (parcelles), each containing a replicate set of 24 trees planted in four columns of six.
- Spacing: 1.75 m between trees within a column; 3 m between columns.
- Blocks: 8 different randomly selected provenances per block, with block positions randomized within soil zones to separate plot, block, soil-zone, and provenance effects.
- For this subset of provenances, block effects were not considered; plot positions within soil zones treated as random.
- Each sampled provenance appears in multiple replicate plots across five soil zones; 2 plots per soil zone per provenance.
- Total: 200 study plots containing 4,800 trees.

## Sampling and measurements (Herbivore survey)
- Target group: Cynipid gall wasps with broad Western Palaearctic distributions.
- Survey years: 2008 and 2009; four surveys per year (spring and autumn generations, two generations each year).
- Within each of 200 plots, galls sampled from 12 of 24 trees (total 2,400 trees).
- Edge effects minimized by surveying the two internal rows of six trees per plot.
- For each surveyed tree: 10 twigs chosen using a pole pruner (~4 m reach), each twig containing the last two years’ growth.
- Galls identified to species and generation in the field using morphological keys and field experience.

## Nature and units of recorded values
- Primary unit: Counts (galls).

## Data structure and variables
- Key identifiers: ID, Record ID, ProvCode, ParcelleID, SoilZone, Soile Zone (1–5), YearGen, TreeNo, ShootNo, Shoot ID.
- Sampling details: Part of the trial design; YearGen indicates generation (S = spring; A = autumn) and survey year (08 = 2008; 09 = 2009); ShootID for the 10 shoots surveyed per tree.
- Gall count variables (Asexual generation): AfecAsex, AglanAsex, AsolAsex, NalbAsex, NantAsex, NqbAsex, NnAsex, CdivAsex, CqfAsex.
- Gall count variables (Sexual generation): AtestSex, NalbSex, NantSex, NnSex, NqbSex.

## Quality control
- One-to-one training of data collectors.
- Double checking for outliers during transcription.

## Additional notes
- The design enables analysis of plot, block, soil-zone, and provenance effects.
- The meticulous recording structure supports cross-plot comparisons of gall abundance by species and generation across provenances and soil conditions.