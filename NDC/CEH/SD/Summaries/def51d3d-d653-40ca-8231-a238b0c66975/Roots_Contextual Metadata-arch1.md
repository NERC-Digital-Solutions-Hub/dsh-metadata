# Root production in human-modified forests of Eastern Amazonia

## Overview of the dataset
- A dataset of fine root production from 20 plots (250 x 10 m each) across a disturbance gradient in the Brazilian Amazon.
- Disturbance classes: undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests (5 plots per class).
- Data collection period: October 2014 to May 2018.
- Purpose: quantify how fine root production varies with forest disturbance and over time.

## Data collection methods
- In-growth cores: four per plot (12 cm diameter, 40 cm deep; mesh 1.5 cm), placed 50 m apart; cores set 30 cm deep with 10 cm aboveground.
- Sampling schedule per core:
  - First measurement (root stock): 24 intervals of five minutes each (with 3-minute breaks); soil homogenized between intervals.
  - After 3 months: second stock using the same method but with 12 intervals.
  - After another 3 months: third stock using the same 12-interval protocol.
  - After one year: the soil core is moved ~30 cm away and sampling restarts with 24 intervals.
- Laboratory processing: roots washed (2 mm sieve), oven-dried at 60°C for 72 hours, weighed.
- Environment measurements: soil temperature and humidity recorded inside and outside each core before sampling.
- Documentation: field and lab notes recorded; burn status during the 2015-16 El Niño tracked for each plot.

## Data structure and fields (Roots.csv)
- Date: date of data collection
- Catchment: microcatchment (~5,000 ha) encompassing the plot
- Transect: plot number within each catchment
- Plot: unique code combining catchment and transect
- Forest: disturbance class before the 2015-16 El Niño
- Fire_ElNino: whether the plot burned during the El Niño (1 = fire, 0 = no fire)
- Core number: identifier for the in-growth core
- Interval: five-minute interval number when roots were collected
- Stock: indicator for the first measurement (1 = stock, 0 = not stock)
- Weight (g): weight of each root sample
- Lab_notes: notes from laboratory processing
- Temperature (inside the core): soil temperature inside the core
- Temperature (outside the core): soil temperature outside the core
- Humidity (inside the core): soil humidity inside the core
- Humidity outside the core: soil humidity outside the core
- Field notes: notes from field processing

## Spatial and temporal coverage
- Geographic coordinates are provided for each plot (e.g., multiple plots identified by codes like 112_12, 112_8, 129_10, etc., with corresponding latitude and longitude).
- Temporal span includes multiple sampling points from 2014–2018, capturing initial stocks and follow-up measurements up to one year after initial installation.

## Potential analyses and uses
- Compare fine root production across disturbance classes to assess impact of logging, burning, and secondary succession.
- Examine temporal dynamics of root production within plots (stock, 3-month, 6-month, 12-month intervals).
- Model root production against environmental variables (temperature, humidity) and El Niño fire status.
- Assess within-plot and between-plot variability by core, interval, and forest category.
- Integrate with metadata (date, catchment, transect) to create standardized production rates per core or per unit area.

## Considerations and limitations
- Replication: 5 plots per disturbance class; limited replication may affect generalizability.
- Measurement complexity: multiple intervals and repeated measures require careful handling of nested and temporal structures.
- Data provenance: comprehensive metadata is provided to enable discoverability and reuse, including lab and field notes.