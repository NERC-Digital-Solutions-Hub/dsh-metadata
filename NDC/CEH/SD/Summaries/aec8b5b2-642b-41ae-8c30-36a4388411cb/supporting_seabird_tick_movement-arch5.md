# Data Collection

## Overview and Aim
- Part of a NERC-funded PhD project studying interactions between avian colonial social structure and tick-borne pathogen dynamics.
- Field site: Isle of May, Scotland (56.2° N, 2.6° W), chosen for its large, accessible population of common guillemots (model species).
- Aim: quantify movements of host-seeking seabird ticks to understand infection risk from Great Island virus in guillemots.
- Lab experiments conducted in 2013 and 2014 under controlled conditions (20 °C, 70% relative humidity).

## Field Sampling and Specimens
- Ticks collected: 24 adult female and 24 nymphal Ixodes uriae.
  - Nymphs collected on 18 July 2013; adult females collected on 25–27 March 2014.
- Collection sites:
  - Nymphs from boiler suits worn by field workers.
  - Adult females from cracks in rock faces.
- Post-collection handling: ticks stored in a moist, dark environment for no longer than four weeks before testing.

## Experimental Setup and Procedure
- Arena: single sheet of A1 paper on the floor with 30 cm high white cardboard walls.
- Position tracking: tick position marked at start and at each subsequent time interval.
- Recording intervals:
  - Nymphs: 2-minute intervals over a total of 10 minutes.
  - Adult females: 1-minute intervals over a total of 5 minutes.
- Controls to reduce bias: arena floor replaced between ticks to avoid kairomone buildup; each tick tested sequentially but returned to moist tubes between tests; 1-minute acclimatization in the arena before recording begins.

## Data Collected (Data Structure)
- Tick_ID: Unique identifier for each tick.
- Date_norm: Number of days from the first date of data collection.
- Trial: Ticks were tested sequentially.
- Dec_time: Decimalized time of day.
- Total displacement: Straight-line distance between starting and finishing point (cm).
- Distanced_movedx: Straight-line distance moved in interval x (cm).
- Life_stage: Tick life stage (nymph or adult female).

## Data Governance and Stewardship Considerations
- Metadata and provenance: clear identifiers and timing fields (Tick_ID, Date_norm, Dec_time) facilitate traceability and reproducibility.
- Data quality cues: standardized measurement intervals, explicit arena setup, and handling procedures to minimize experimental bias (e.g., kairomone control, acclimatization period).
- Storage and handling notes: explicit condition (moist, dark environment) and maximum storage period before testing, which should be captured in metadata.
- Usability for reuse: structured, labeled data with explicit units (cm, days, time of day) and clearly defined variables support discovery, integration with related studies, and secondary analyses of tick movement and pathogen risk.