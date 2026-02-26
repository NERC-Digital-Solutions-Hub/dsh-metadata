# Data Collection

- This work is part of a NERC-funded PhD project examining interactions between avian colonial social structure and tick-borne pathogen dynamics, conducted on the Isle of May, Scotland, chosen for its large and accessible population of common guillemots.
- Data were collected on the spatial attendance of immature guillemots from 25 April–12 May and 21 May–15 June 2013 at four sites on the Isle of May.
- Aims to quantify movements of immature guillemots (noted for higher infection with Great Island virus) to understand infection risk to the breeding colony.
- A grid was overlaid on site photographs to record bird locations, with grid cells classified as breeding or pre-breeding based on breeding activity (egg/chick presence or surrounding consistent breeding activity).
- If a focal bird was lost from sight, the watch continued; if it flew away, the watch was terminated.
- 69 randomly selected, individually marked birds were followed for 10-minute periods using a telescope (×20–60) with location recorded every 15 seconds. Intervals spent in pre-breeding and breeding areas were computed.
- Each site observed for 2 hours per day, using stratified sampling to balance coverage across all sites and times of day.
- The dataset includes some preliminary data.
- An index of breeder attendance was recorded per site by counting birds in a clearly delimited breeding-area zone and dividing by the maximum count in that area to generate a proportional breeder attendance variable.

## Data Structure

- Date_norm: Day count from the first date of data collection.
- Sub_colony: Site at which the bird was observed.
- Time_perod: 1 = dawn–10:30, 2 = 10:30–16:00, 3 = 16:00–dusk.
- Wind_strength: 1 = None, 2 = Light breeze, 3 = Fair breeze, 4 = Strong, 5 = Gale force.
- Sea condition: 1 = Still, 2 = Calm, 3 = Fairly choppy, 5 = Very choppy, 6 = High waves.
- Temperature: 1 = Very warm, 2 = Warm, 3 = Comfortable, 4 = Cool, 5 = Very Cool, 6 = Freezing.
- B_att_prop: Number of breeding birds observed in a predefined area divided by the maximum count in that area across data collection.
- Age: Age of the bird (current year minus year of ringing; individuals known to be ringed as chicks).
- Ring: Unique ID for each bird.
- Sampling period: Length of time the bird was watched (mostly 10 minutes; some preliminary observations vary).
- P_recs: Number of intervals in which the bird was seen in a pre-breeding area.
- Time interval: Interval at which the bird’s location was recorded (mostly 15 seconds; some preliminary observations vary).
- B_recs: Number of intervals in which the bird was seen in a breeding area.
- Other_unknown_recs: Number of intervals in which the bird was not seen in any grid cell (e.g., flew off).
- Other_known_recs: Number of intervals in which the bird was seen in a grid cell of unknown status.