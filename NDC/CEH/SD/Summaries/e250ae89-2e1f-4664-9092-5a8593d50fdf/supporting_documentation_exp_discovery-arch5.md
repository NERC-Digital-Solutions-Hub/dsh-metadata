# Supporting documentation on the patch-discovery experiment

## Study context and aims
- Location: Wytham Woods, Oxfordshire, UK (51°46′N, 1°20′W)
- Subjects: great tits (Parus major), blue tits (Cyanistes caeruleus), marsh tits (Poecile palustris)
- Timeframe: January–March 2021
- Objective: investigate how changes in local population density influence discovery of a novel resource (a new food patch)

## Data collected and key variables
- Data format: a single CSV file
- Core variables:
  - Date and time of each visit
  - Logger id (novel feeder)
  - Bto.ring (identity of the individual)
  - Site (experimental site identity)
  - Bto.species.code (species code: greti = great tit, bluti = blue tit, marti = marsh tit)

## Experimental design and data collection methods
- Setup: at each site, a novel feeder placed near two existing feeders (approximately 40 m apart) in opposite directions
- Second patch-discovery phase: conducted during the density manipulation at additional locations
- Novel feeders: sunflower seeds; accessible to all PIT-tagged birds; identical design to existing feeders to avoid neophobia
- Placement timing: inserted the day before the experiment after sunset or on the day of the experiment before sunrise
- Duration per patch: feeders were available for one day
- Data collectors: Keith McMahon, Sam Croft, and Kristina Beck

## Data provenance and metadata
- Dataset origin: observational data collected during the patch-discovery experiment
- Referenced background: Savill et al. 2011, Wytham Woods: Oxford's ecological laboratory
- Metadata considerations for stewardship:
  - Clear field names and coding for species (greti, bluti, marti)
  - Precise timing (date/time) and linkage to specific feeders (logger)
  - Explicit site identifiers and individual IDs (Bto.ring)

## Data quality, limitations, and reuse considerations
- Strengths: concise per-visit record with essential identifiers (individual, species, site, feeder, timestamp)
- Limitations and considerations:
  - Single CSV; scope limited to visits to novel feeders within the experimental window
  - Data limited to PIT-tagged birds; may not capture all individuals in the population
  - Temporal scope confined to January–March 2021 and to the patch-discovery context
  - Potential need for decoding species codes and validating time formats for reuse
- Governance implications for reuse:
  - Ensure complete metadata documentation (date/time format, time zone, feeder IDs)
  - Validate consistency of IDs (Bto.ring) and site codes across records
  - Provide provenance references and context for density manipulation experiments to aid interpretation

## References
- Savill P, Perrins C, Kirby K, Fisher N. 2011. Wytham Woods: Oxford's ecological laboratory. Oxford University Press.