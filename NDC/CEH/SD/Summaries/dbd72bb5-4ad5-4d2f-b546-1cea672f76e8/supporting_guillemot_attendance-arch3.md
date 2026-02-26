# Data Collection

## Purpose and Scope
- NERC-funded PhD project examining interactions between avian colonial social structure and tick-borne pathogen dynamics.
- Isle of May, Scotland, chosen for its large, accessible population of common guillemots.
- Aims to quantify movements of immature guillemots to assess infection risk to the breeding colony, particularly regarding Great Island virus.

## Field Site and Study Population
- Location: Isle of May, Firth of Forth, Scotland (56.2° N, 2.6° W).
- Focus species: common guillemots; immature individuals tracked to infer movement patterns and potential pathogen exposure.

## Data Collection Methods
- Timeframe: 25 April–12 May and 21 May–15 June 2013.
- Recording approach: spatial attendance of immature guillemots using grids overlaid on site photographs; grid cells classified as breeding or pre-breeding based on observed breeding activity (egg/chick presence) or surrounding breeding activity.
- Individual tracking: 69 randomly selected, individually-marked birds followed with a telescope (×20–60) for 10-minute watch periods; locations recorded every 15 seconds.
- Observation schedule: each site observed for 2 hours per day with a stratified design to balance coverage across sites and times of day.
- Handling of data collection issues: if a focal bird was lost from sight, the bird was marked as out of sight but the watch continued; if the bird flew away from the site, the watch was terminated.
- Breeder attendance index: calculated by counting birds in a clearly delimited breeding area and dividing by the maximum count observed in that area to yield a proportional breeder attendance variable.
- Additional note: dataset includes some preliminary data.

## Data Structure and Variables
- Date_norm: Day from the first date of data collection.
- Sub_colony: Site at which the bird was observed.
- Time_perod: 1 = dawn–10:30, 2 = 10:30–16:00, 3 = 16:00–dusk.
- Wind_strength: 1 = None, 2 = Light breeze, 3 = Fair breeze, 4 = Strong, 5 = Gale force.
- Sea_condition: 1 = Still, 2 = Calm, 3 = Fairly choppy, 5 = Very choppy, 6 = High waves.
- Temperature: 1 = Very warm, 2 = Warm, 3 = Comfortable, 4 = Cool, 5 = Very Cool, 6 = Freezing.
- B_att_prop: Proportion of breeding birds observed in the defined area relative to the maximum count.
- Age: Age of the bird (current year minus year of ringing).
- Ring: Unique ID for each bird.
- Sampling period: Length of time the bird was watched (mostly 10 minutes; some preliminary observations vary).
- P_recs: Number of intervals in which the bird was seen in a pre-breeding area.
- Time interval: Interval at which location was recorded (mostly 15 seconds; some preliminary observations vary).
- B_recs: Number of intervals in which the bird was seen in a breeding area.
- Other_unknown_recs: Number of intervals when the bird was not seen in any grid cell (e.g., flew off).
- Other_known_recs: Number of intervals when the bird was seen in a grid cell of unknown status.

## Sampling Design and Temporal Coverage
- Two sampling windows within 2013; observations conducted daily across four sites for 2 hours each.
- Focus on 69 individually marked birds; 10-minute focal watches with high-frequency spatial recording (every 15 seconds).

## Data Quality, Gaps, and Preliminary Data
- Acknowledges inclusion of preliminary data in the dataset.
- Data quality depends on grid classification accuracy, consistent sighting, and standardized recording across sites and times.

## Potential Monitoring and Policy Implications
- Provides standardized environmental and behavioral metrics (location, timing, weather, sea state, temperature) linked to disease exposure risk in a colonial seabird context.
- Can inform monitoring frameworks on how animal movement and occupancy relate to pathogen dynamics and colony health.
- Data can support assessments of breeding vs. pre-breeding habitat use and temporal patterns relevant to management decisions for seabird colonies.

## Data Governance and Metadata Considerations
- Emphasizes structured metadata through defined variables (dates, site, time periods, environmental covariates, and occupancy metrics).
- Clear documentation of observational rules (handling of birds out of sight, grid-based breeding classifications) to support reproducibility and data sharing; dataset also notes inclusion of preliminary data.