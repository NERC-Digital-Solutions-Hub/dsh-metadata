# Data Collection

- Part of a NERC-funded PhD project examining interactions between avian colonial social structure and tick-borne pathogen dynamics.
- Field site: Isle of May, Firth of Forth, Scotland (56.2° N, 2.6° W) chosen for its large, accessible population of common guillemots (the model host).
- Aim: quantify movements of the host-seeking seabird tick (Ixodes uriae) to understand the risk of infection with Great Island virus for the guillemot host.
- Tick sampling:
  - 24 adult female and 24 nymphal ticks collected on Isle of May (adult females from rock cracks; nymphs from boiler suits worn by field workers).
  - Collection dates: 25–27 March 2014 (adults) and 18 July 2013 (nymphs).
  - Ticks stored in a moist, dark environment for no longer than four weeks before testing.
- Laboratory experiments:
  - Conducted under controlled conditions (20 °C and 70% relative humidity).
  - Each tick tested individually in an arena (30 cm high white cardboard walls with a single A1 paper floor).
  - Position of each tick recorded at start and at subsequent time intervals.
  - Movement recording intervals:
    - Nymphs: 2-minute intervals, total 10 minutes per tick.
    - Adult females: 1-minute intervals, total 5 minutes per tick.
  - Kairomone management: arena floor paper replaced between ticks to avoid carryover effects.
  - Procedure: ticks tested sequentially; returned to moist tubes between tests; 1-minute acclimation period before recording begins.

- Site and host context:
  - Focus on guillemot hosts to assess exposure risk to Great Island virus via tick movements.
  - Tick species: Ixodes uriae.

- Data collection conditions and handling:
  - Each tick tested in a controlled, consistent environment to enable comparability across trials.
  - Ticks stored and handled to maintain moisture and minimize stress prior to testing.

## Data Structure

- Tick_ID: Unique identifier for each tick.
- Date_norm: Number of days from the first date of data collection.
- Trial: Order in which ticks were tested (sequential).
- Dec_time: Decimalized time of day.
- Total displacement: Straight-line distance from starting to finishing point (cm).
- Distanced_movedx: Straight-line distance moved in interval x (cm).
- Life_stage: Life stage of the tick (nymph or adult female).