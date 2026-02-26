# Metadata for Marsh Tit ( Poecile palustris ) territory surveys in English woods during 2002-2020

## What is in the dataset
- Annual surveys of the number of occupied Marsh Tit territories in individual woods and woodland patches.
- Surveys occurred in early spring (February–April), just before nesting, representing the number of breeding territories in each wood.

## Context and significance
- Marsh Tits are small, non-migratory songbirds that prefer mature deciduous and mixed woodlands; territories average 5–6 ha.
- The species has declined by about 80% from 1967 to 2018, making monitoring important.
- Monitoring uses a playback method (recorded song/calls) to locate territories; some woods also used colour-ringing in population projects.

## Study design and geography
- Survey framework: playback method (primary), with some woods also surveyed via colour-ringing.
- Coverage: 74 woods in 14 English counties, 2002–2020, predominantly Cambridgeshire and Oxfordshire.
- Temporal resolution: some woods surveyed in a single spring; others annually for up to 17 consecutive springs.
- Spatial scope: surveyed area derived from the Forestry Commission’s National Forest Inventory England 2015.
- Woodland typing: classified by the Ancient Woodland Inventory (AWI) into ASNW (ancient semi-natural woodland), PAWS (planted ancient woodland site), or NEW WOODLAND (post-1600).

## Data quality and limitations
- Territory counts are considered highly reliable.
- Playback method locates about 96% of birds present.
- Underestimation of around 10% for larger woods (>70 ha).
- Some woods were completely or partially surveyed, affecting comparability over time or area.

## Data structure
- Georeferenced dataset stored as a CSV with columns:
  - Wood_id; Wood
  - County
  - OSGB X; OSGB Y (British National Grid coordinates)
  - Survey year
  - Time Series Analysis (1 = used; 0 = not used)
  - Wood area (ha)
  - Complete or partial survey
  - Woodland type (ASNW, PAWS, NEW WOODLAND)
  - Marsh Tit territories
  - Method (Playback or CR)

## Usage and metadata considerations
- Data are designed for time-series analysis and spatial analyses of territory occupancy.
- Enables calculation of mean territory values per wood and assessment of trends across woodland types and regions.
- Metadata and references provide contextual methods and provenance for replication and quality checks.

## Acknowledgements and references
- Acknowledgements to data collectors and landowners.
- Key references include Broughton et al. (2010, 2012, 2014, 2018) on dispersal, habitat occupancy, nest placement, and survey methods; Forestry Commission (National Forest Inventory England 2015); Natural England (Ancient Woodland England); BirdTrends 2018.