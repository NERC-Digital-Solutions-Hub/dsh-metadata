# WildCrickets05A-CaptureRecapture Description of content

## Overview
- A dataset containing basic information on each male adult cricket tagged in the population.
- Records focus on five traits: Year, ID, Birth, Death, and 2-99 (Recapture days).

## Data fields

- Year: The year when the cricket was alive.
- ID: The unique individual identification for the cricket.
- Birth: Day of birth relative to the day of birth of the first adult cricket emerging that year; zeroes indicate individuals with unknown birth dates.
- Death: Date of death relative to the date of birth of the first adult cricket emerging that year.
- 2-99: Recapture days (recapture events), with values spanning 2 to 99.

## How this data can be used

- Conduct capture–recapture analyses to estimate survival, lifespan, and capture probabilities of tagged male crickets.
- Build individual life histories across years and relate recapture histories to demographic parameters.
- Compare patterns across cohorts or emergence years.

## Data quality and considerations

- Birth dates may be unknown (indicated by 0), which can limit precise age estimates.
- Both Birth and Death are relative to the first emergent adult cricket of that year, requiring anchoring to this reference for absolute dating.
- The field name 2-99 indicates recapture days and implies specific interval timings; ensure correct interpretation in analyses.
- Dataset includes only male adults, which may affect population-level generalizations.

## Practical tips for analysts

- Where possible, anchor Birth and Death to the first emergence date to derive calendar dates.
- Verify the consistency and uniqueness of IDs across years.
- Treat Birth = 0 as missing data for age-related analyses; document handling choices.
- Maintain clear data provenance and metadata to enable reproducible analyses.