# Root production in human-modified forests of Eastern Amazonia

## What this dataset is
- A dataset of fine root production measurements across 20 plots in the Brazilian Amazon, spanning a gradient of disturbance.
- Disturbance classes: undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests (5 plots per class).
- Data collected from October 2014 to May 2018.
- Each plot has precise geographic coordinates provided.

## How data were collected
- Four in-growth soil cores per plot (12 cm diameter, 40 cm deep) placed 50 m apart; cores set 30 cm deep with 10 cm above ground.
- Pre-sampling measurements included soil temperature inside and outside each core.
- Field processing: cores broken into smaller parts on a sheet, homogenized, and roots extracted for weighing.
- Sampling schedule per core:
  - First measurement (root stock): 24 intervals of five minutes each.
  - After 3 months: second sampling with 12 intervals of five minutes.
  - After an additional 3 months: third sampling with 12 intervals.
  - After one year: a new core ~30 cm from the first, sampled with 24 intervals.
- Laboratory processing: roots washed through a 2 mm sieve, oven-dried at 60°C for 72 hours, and weighed.

## Data structure and variables
- Data file: Roots.csv
- Key columns include:
  - Date: data collection date
  - Catchment: microcatchment (~5,000 ha) containing each plot
  - Transect: plot number within each catchment
  - Plot: unique plot code combining catchment and transect
  - Forest: disturbance class before the 2015-16 El Niño
  - Fire_ElNino: whether the plot burned during the 2015-16 El Niño (1 = fire, 0 = no fire)
  - Core number: identifier for each in-growth core
  - Interval: five-minute sampling interval during each measurement
  - Stock: indicator for the first measurement of each core (1 = stock, 0 = not stock)
  - Weight (g): dry weight of each root sample
  - Lab_notes: notes from laboratory processing
  - Temperature (inside/outside core): soil temperature measurements
  - Humidity (inside/outside core): soil humidity measurements
  - Field notes: field processing notes
- Plot coordinates:
  - 20 plots with IDs (e.g., 112_12, 112_8, 129_10, etc.)
  - Each plot has latitude and longitude coordinates.

## Plot coordinates and spatial layout
- Coordinates provided for all 20 plots, enabling spatial analyses across the disturbance gradient.

## Temporal scope and sampling design
- Timeframe: October 2014 to May 2018.
- Experimental design: 20 plots evenly distributed across four disturbance classes (5 plots per class).
- Repeated measurements within the first year and an additional core sampled after one year to capture longer-term root production dynamics.

## Access, format, and data quality considerations
- Data delivered as a comma-separated values file (Roots.csv), facilitating discoverability and reuse.
- Rich metadata embedded in the dataset (sample timing, core and interval identifiers, lab and field notes, environmental measurements) to support data provenance, quality assessment, and reanalysis.
- Metadata supports assessing data suitability for analyses of how fine root production relates to disturbance, fire events (El Niño), and environmental conditions.

## Potential uses and implications for data management
- Suitable for analyses of how fine root production responds to different levels of forest disturbance and to fire events.
- Enables temporal analyses given multi-timepoint sampling per core and an additional year-lag sampling.
- Supports cross-plot comparisons with explicit metadata on disturbance class, site conditions, and sampling context.
- Data governance considerations:
  - Clear definitions for disturbance classes and sampling intervals aid in reproducibility.
  - Detailed core-level and environmental measurements support data quality checks and normalization.
  - Spatial coordinates enable integration with regional datasets for broader ecological and management insights.