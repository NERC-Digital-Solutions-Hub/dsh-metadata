# Data Collection

- This work is part of a NERC-funded PhD project examining interactions between avian colonial social structure and tick-borne pathogen dynamics.
- Field site: Isle of May, Firth of Forth, Scotland, chosen for its large, accessible population of common guillemots; aim to quantify movements of host-seeking seabird tick to understand Great Island virus risk for the guillemot host.
- Laboratory experiments conducted in two periods:
  - Nymphs: 19 July–8 August 2013
  - Adult females: 4–11 April 2014
  - Conditions: constant 20 °C and 70% relative humidity
- Tick samples:
  - 24 adult female ticks and 24 nymphs collected on Isle of May (adult females: 25–27 March 2014; nymphs: 18 July 2013)
  - Nymphs collected from field-worker boiler suits; adult females from rock cracks
  - Stored in a moist, dark environment for ≤ four weeks before testing
- Testing setup:
  - Each tick tested individually in an arena (floor: single A1 paper; walls: 30 cm high white cardboard)
  - Tick positions marked at start and at defined intervals
  - Nymphs: recording interval 2 minutes, total duration 10 minutes
  - Adult females: recording interval 1 minute, total duration 5 minutes
  - To avoid kairomone effects, the arena floor was replaced between ticks
  - Ticks tested sequentially; between tests returned to moist tubes
  - Acclimatization: 1 minute in arena before recording begins

## Data Structure

- Tick_ID: Unique ID for each tick
- Date_norm: Number of days from the first data collection date
- Trial: Order in which ticks were tested
- Dec_time: Decimalized time of day
- Total displacement: Straight-line distance from starting to finishing point (cm)
- Distanced_movedx: Straight-line distance moved in interval x (cm)
- Life_stage: Tick life stage (nymph or adult female)

## Implications for Data Leadership

- Demonstrates the importance of clear data schemas with unique identifiers and temporal metadata to enable traceability and reproducibility.
- Highlights rigorous experimental controls and provenance (source of samples, storage conditions, arena design, and procedures to minimize confounding factors).
- Points to data governance considerations: metadata completeness (collection dates, locations, life stage), standardized measurement units, and documentation of testing protocols for future integration with broader data systems.
- Underlines the need for careful attention to data quality and potential batch effects when combining data from distinct experiments (nymph vs. adult female).