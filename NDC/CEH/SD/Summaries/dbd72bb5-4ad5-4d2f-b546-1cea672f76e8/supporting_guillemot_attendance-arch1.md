# Data Collection

- Field site and study purpose:
  - Isle of May, Firth of Forth, Scotland (56.2° N, 2.6° W).
  - NERC-funded PhD project on interactions between avian colonial social structure and tick-borne pathogen dynamics.
  - Model species: common guillemots; aim to quantify movements of immature birds to understand infection risk to the breeding colony.

- Data collection timeframe and scope:
  - Dates: 25 April–12 May 2013 and 21 May–15 June 2013.
  - Four sites on the Isle of May used; grid overlaid on site photographs to classify grid cells as breeding or pre-breeding areas.
  - A total of 69 randomly selected, individually-marked birds followed.

- Field procedures:
  - Observation method: telescope (×20–60) for 10-minute periods; location recorded every 15 seconds.
  - If a focal bird was lost to sight, the watch continued; if it flew away, the watch was terminated.
  - Each site observed for 2 hours per day with stratified sampling to balance coverage across all sites and times of day.
  - Breeder attendance index created by counting birds in a defined breeding-area segment and normalizing by the maximum count in that area.

- Data scope and preliminary data:
  - Dataset includes some preliminary observations.
  - Grid-based approach to determine breeding vs pre-breeding status based on observed breeding activity (egg/chick) at any point or consistent surrounding breeding activity.

- Data structure and variables (key fields):
  - Date_norm: Day from the first date of data collection.
  - Sub_colony: Site where the bird was observed.
  - Time_perod: 1 = dawn–10:30, 2 = 10:30–16:00, 3 = 16:00–dusk.
  - Wind_strength: 1 = None, 2 = Light breeze, 3 = Fair breeze, 4 = Strong, 5 = Gale force.
  - Sea condition: 1 = Still, 2 = Calm, 3 = Fairly choppy, 5 = Very choppy, 6 = High waves.
  - Temperature: 1 = Very warm, 2 = Warm, 3 = Comfortable, 4 = Cool, 5 = Very Cool, 6 = Freezing.
  - B_att_prop: proportion of breeding birds observed in a defined area (per area’s maximum count).
  - Age: Age of bird (current year minus year of ringing; birds ringed as chicks).
  - Ring: Unique ID for each bird.
  - Sampling period: Length of time the bird was watched (mostly 10 minutes; some preliminary observations vary).
  - P_recs: Number of intervals where the bird was seen in a pre-breeding area.
  - Time interval: Interval at which bird’s location was recorded (mostly 15 seconds; some preliminary data vary).
  - B_recs: Number of intervals where the bird was seen in a breeding area.
  - Other_unknown_recs: Intervals where the bird was not seen in any grid cell (e.g., flew off).
  - Other_known_recs: Intervals where the bird was seen in a grid cell of unknown status.

- Analytical relevance for researchers:
  - Enables quantification of movements between pre-breeding and breeding areas.
  - Facilitates analysis of how environmental factors (wind, sea state, temperature) relate to attendance and movement.
  - Provides an attendance index (B_att_prop) for site-level activity and potential exposure contexts.
  - Longitudinal aspects possible via Bird Ring IDs and age data to explore individual movement patterns over time.
  - Data can be integrated to model infection risk dynamics for the tick-borne Great Island virus indirectly through spatial-temporal exposure patterns.