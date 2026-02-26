# Supporting documentation on the patch-discovery experiment

## Overview
- Location: Wytham woods, Oxfordshire, UK (51°46′N, 1°20′W).
- Subjects: great tits (Parus major), blue tits (Cyanistes caeruleus), marsh tits (Poecile palustris); birds fitted with unique metal leg-rings and passive integrated transponder (PIT) tags.
- Timeframe: January–March 2021.
- Aim: to investigate how changes in local population density influence discovery of a novel resource (a new feeder) by PIT-tagged birds.

## Experimental design
- Two sites with two existing feeders each; a novel feeder placed near each existing feeder (approximately 40 meters apart) in opposite directions.
- In the second patch-discovery experiment, during density manipulation, other locations were selected for novel feeders.
- Novel feeders provided sunflower seeds and allowed access to all PIT-tagged birds.

## Data collection and methods
- Data collectors: Keith McMahon, Sam Croft, Kristina Beck.
- Deployment timing: novel feeders installed the day before the experiment after sunset or on the day of the experiment before sunrise; feeders remained in place for one day.
- Data type: visits to novel feeders by individual birds.

## Data product and data structure
- Single CSV dataset containing:
  - Date and time of each visit.
  - Logger (novel feeder) identifier.
  - Site (experimental site).
  - Bto.ring (bird identity).
  - Bto.species.code (species of the bird).
- Species codes:
  - greti = great tit
  - bluti = blue tit
  - marti = marsh tit

## Data schema and codes
- Columns of interest:
  - Bto.ring (individual identifier)
  - Site (experimental site)
  - Bto.species.code (greti, bluti, marti)
  - Date, Time
  - Logger (novel feeder)

## Spatial considerations for GIS work
- Feeder layout per site: two existing feeders plus two novel feeders, placed in opposite directions; distance between nearby feeders ≈ 40 meters.
- Site-level data enables mapping discovery order and timing across spatial arrangements and under different density conditions.
- Geographic context: data tied to specific sites within Wytham Woods, enabling spatial analyses of discovery patterns.

## Provenance and references
- Primary reference: Savill P, Perrins C, Kirby K, Fisher N. 2011. Wytham Woods: Oxford's ecological laboratory. Oxford University Press.