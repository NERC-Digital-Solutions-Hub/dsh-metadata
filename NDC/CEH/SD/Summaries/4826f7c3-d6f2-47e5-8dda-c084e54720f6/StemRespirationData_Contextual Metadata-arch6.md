# Stem respiration in human-modified forests of Eastern Amazonia

## Overview of data
- Dataset: StemRespirationData.csv containing stem respiration measurements for trees in 20 Amazonian forest plots.
- Disturbance gradient: plots classified as undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests (5 plots per class).
- Timeframe: data collected from June 2015 to July 2018.
- Context: part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).

## Data collection methods
- Stem collars installed on at least 13 trees per plot, positioned 20 cm above dendrometers.
- DBH classes: 10–19.99 cm, 20–29.99 cm, 30–39.99 cm, 40–49.99 cm, and ≥50 cm.
- Collars: PVC, about 5 cm tall by 10 cm diameter; connected to an infrared gas analyser (EGM5) to measure stem CO2 efflux.
- Sampling frequency: every 3 months.
- Replacement: if a tree died, its collar was removed and replaced on a new tree in the same size class, preferably near an existing dendrometer.
- Data gaps: marked as N/A with reasons provided in the notes column.

## Plot coordinates
- Coordinates are provided for plots across the study area (20 plots total), identified by codes such as 112_12, 112_8, 129_10, 129_11, 129_5, 260_1, 260_4, 260_5, 261_10, 261_9, 357_2, 357_3, 357_4, 357_6, 357_9, 363_3, 363_6, 363_7, 69_11, and 69_8, with specific latitude and longitude values listed in the dataset.

## Data structure and fields
- Date: Date of data collection
- Catchment: Microcatchment (~5,000 ha) where each plot is located
- Transect: Plot number within each catchment
- Plot code: Unique code combining catchment and transect
- Forest: Forest disturbance class before the 2015–16 El Niño
- Fire: Whether the plot burned during the 2015–16 El Niño (1 = yes, 0 = no)
- Tree TAG: Identifier for the individual with the collar
- Time: Exact time of data sampling
- Collar height: Height of the collar at sampling
- CO2 initial: CO2 concentration at the start of the measurement
- CO final: CO2 concentration at the end of the measurement
- Flux: Measured stem CO2 efflux (flux)
- Field notes: Additional notes from field processing

## Notes and provenance
- N/A entries indicate measurements not taken; reasons are documented in the notes column.
- Data are provided as a single CSV file (StemRespirationData.csv) and are intended for exploration, analysis of stem CO2 efflux across disturbance gradients, and potential self-serve data products (e.g., dashboards or reports).