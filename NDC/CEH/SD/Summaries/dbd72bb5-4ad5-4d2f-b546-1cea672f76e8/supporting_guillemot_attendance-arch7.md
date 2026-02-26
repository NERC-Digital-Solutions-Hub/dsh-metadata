# Data Collection

## Context and Aim
- NERC-funded PhD project examining interactions between avian colonial social structure and tick-borne pathogen dynamics.
- Study site: Isle of May, Firth of Forth, Scotland (56.2° N, 2.6° W).
- Objective: quantify movements of immature guillemots to understand infection risk to the breeding colony.

## Study Site and Observation Protocol
- Four sites on the Isle of May; grid overlay on site photographs to record locations (grid cells classified as breeding or pre-breeding based on activity during data collection).
- Breeding area assumptions: cells with ledges and surrounding breeding activity may be considered breeding.
- Monitoring rules: if a focal bird is lost from sight, record as out of sight but continue watching; if it flies away from the site, watching is terminated.

## Data Collection Details
- Subjects: 69 randomly selected, individually-marked birds followed.
- Observation method: telescope (×20-60) for 10-minute periods; location recorded in grids every 15 seconds.
- Schedule: each site observed for 2 hours per day; stratified sampling to cover all sites and times of day.
- Dataset notes: includes some preliminary data.
- Breeder attendance index: computed as the number of birds in a clearly delimited breeding area divided by the maximum count in that area.

## Data Collected and Variables (Data Structure)
- Date_norm: Day count from the first data collection date.
- Sub_colony: Site where the bird was observed.
- Time_period: 1 = dawn–10:30, 2 = 10:30–16:00, 3 = 16:00–dusk.
- Wind_strength: 1=None, 2=Light breeze, 3=Fair breeze, 4=Strong, 5=Gale.
- Sea condition: 1=Still, 2=Calm, 3=Fairly choppy, 5=Very choppy, 6=High waves.
- Temperature: 1=Very warm, 2=Warm, 3=Comfortable, 4=Cool, 5=Very Cool, 6=Freezing.
- B_att_prop: Proportion of breeding birds in a predefined area (observed/maximum).
- Age: Age of bird (current year minus year of ringing).
- Ring: Unique ID for each bird.
- Sampling period: Length of time that each bird was watched (mostly 10 minutes; some preliminary observations vary).
- P_recs: Number of intervals in which the bird was seen in a pre-breeding area.
- Time interval: Interval at which location was recorded (mostly 15 seconds; some preliminary data vary).
- B_recs: Number of intervals in which the bird was seen in a breeding area.
- Other_unknown_recs: Intervals where the bird was not seen in any grid cell (e.g., flew off).
- Other_known_recs: Intervals where the bird was seen in a grid cell of unknown status.

## GIS and Data Use Implications
- Grid-based spatial data suitable for mapping movement patterns and occupancy across breeding and pre-breeding areas.
- Enables analysis of time-allocated space use in relation to environmental conditions (Wind_strength, Sea_condition, Temperature) and site-specific factors (Sub_colony, B_att_prop).
- Data can support spatial models of infection risk by linking bird presence in breeding vs. pre-breeding areas with exposure variables.
- Requires careful handling of preliminary data and varying observation lengths when integrating into maps or analyses.