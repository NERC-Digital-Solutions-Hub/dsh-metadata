# Data Collection

- Context and aim: Part of a NERC-funded PhD project examining interactions between avian colonial social structure and tick-borne pathogen dynamics. Field site is the Isle of May, Scotland (56.2° N, 2.6° W). Primary aim is to quantify movements of host-seeking seabird ticks to understand infection risk of Great Island virus for guillemots.

- Specimens and collection: 24 adult female and 24 nymphal Ixodes uriae ticks collected on Isle of May (adults from cracks in rock faces, nymphs from boiler suits worn by field workers). Stored in a moist, dark environment for no longer than four weeks before testing.

- Laboratory conditions: Experiments conducted at 20 °C and 70% relative humidity. Each tick tested individually in an arena.

- Arena setup and procedure:
  - Floor: single A1 piece of paper; walls: 30 cm high white cardboard.
  - At the start and at each subsequent time interval, the tick’s position is marked.
  - Time intervals: nymphs recorded with 2-minute intervals for a total of 10 minutes; adult females with 1-minute intervals for a total of 5 minutes.
  - Kairomone control: the arena paper is changed each time a tick is introduced to avoid chemical cues from previous trials.
  - Process: ticks tested sequentially; returned to moist tubes between tests; acclimatization period of 1 minute before recording begins.

- Data relevance for GIS: Data capture includes spatial positions over time within a controlled arena, enabling time-resolved movement analysis that can inform spatial modelling of tick behavior under standardized conditions.

- Data Structure (fields):
  - Tick_ID: Unique identifier for each tick.
  - Date_norm: Number of days from the first date of data collection.
  - Trial: Order in which ticks were tested (sequential).
  - Dec_time: Decimalised time of day.
  - Total displacement: Straight-line distance from starting to finishing point (cm).
  - Distanced_movedx: Straight-line distance moved in interval x (cm).
  - Life_stage: Stage of tick (nymph or adult female).