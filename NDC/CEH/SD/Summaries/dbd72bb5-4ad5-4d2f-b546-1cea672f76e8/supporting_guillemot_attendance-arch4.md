# Data Collection

- This was part of a NERC-funded PhD project examining interactions between avian colonial social structure and tick-borne pathogen dynamics.
- Site: Isle of May, Firth of Forth, Scotland (56.2° N, 2.6° W), chosen for its large, accessible common guillemot population.
- Model species: common guillemots; aim to quantify movements of immature birds to understand infection risk to the breeding colony, particularly regarding Great Island virus.
- Timeframe: data collected on immature guillemots from 25 April–12 May and 21 May–15 June 2013.
- Data collection goal: record locations of birds to assess time spent in pre-breeding vs. breeding areas and relate movement to infection risk.

- Spatial recording approach:
  - A grid was overlaid on site photographs to categorize grid cells as breeding or pre-breeding based on observed breeding activity (egg/chick presence).
  - Cells with ledges but no observed breeding activity, yet surrounded by breeding activity, were treated as breeding areas.

- Observation protocol:
  - 69 randomly selected, individually marked birds followed with a telescope (×20–60) for 10-minute watches.
  - Locations recorded every 15 seconds; calculations yielded time in pre-breeding vs. breeding areas.
  - Each site observed for 2 hours per day with a stratified sampling design to balance coverage across sites and times of day.
  - If a focal bird remained out of sight, the watch continued; if it flew away, the watch was terminated.
  - Dataset includes some preliminary observations.

- Breeder attendance index:
  - Calculated by counting birds in a clearly delimited breeding area and dividing by the maximum count in that area to produce a proportional breeder attendance metric.

- Data structure: key fields and coding
  - Date_norm: day offset from the first data collection date.
  - Sub_colony: site where the bird was observed.
  - Time_perod: 1 = dawn–10:30, 2 = 10:30–16:00, 3 = 16:00–dusk.
  - Wind_strength: 1 = None, 2 = Light breeze, 3 = Fair breeze, 4 = Strong, 5 = Gale force.
  - Sea condition: 1 = Still, 2 = Calm, 3 = Fairly choppy, 5 = Very choppy, 6 = High waves.
  - Temperature: 1 = Very warm, 2 = Warm, 3 = Comfortable, 4 = Cool, 5 = Very Cool, 6 = Freezing.
  - B_att_prop: number of breeding birds observed in the defined area / maximum count in that area during data collection.
  - Age: age of bird (current year minus year of ringing; birds known to have been ringed as chicks).
  - Ring: unique ID for each bird.
  - Sampling_period: length of time the bird was watched (mostly 10 minutes; some preliminary observations vary).
  - P_recs: number of intervals where the bird was seen in a pre-breeding area.
  - Time_interval: interval at which the bird’s location was recorded (mostly 15 seconds; some preliminary observations vary).
  - B_recs: number of intervals where the bird was seen in a breeding area.
  - Other_unknown_recs: number of intervals where the bird was not seen in any grid cell (e.g., flew off).
  - Other_known_recs: number of intervals where the bird was seen in a grid cell of unknown status.

- Contextual note:
  - The dataset references prior work on avian disease and tick-borne viruses, including Great Island virus (Nunn et al., 2006).