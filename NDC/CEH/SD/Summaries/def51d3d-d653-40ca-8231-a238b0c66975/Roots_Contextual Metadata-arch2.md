# Root production in human-modified forests of Eastern Amazonia

## Overview
- A dataset (Roots.csv) of fine root production measured in 20 plots (250 x 10 m each) across an environmental disturbance gradient in the Brazilian Amazon.
- Disturbance categories: undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests (5 plots per category).
- Data collection period: October 2014 to May 2018.

## Study design and sampling framework
- Plots distributed across a gradient of disturbance to evaluate how disturbance influences fine root production.
- Disturbance classification based on canopy disturbance analyzed from a satellite chronosequence (1988–2010) plus field assessments of fire scars, charcoal, and logging debris.
- Four in-growth soil cores per plot used to quantify root production.
- Core placement: 50 m apart; each core placed 30 cm deep into the soil (10 cm aboveground).

## Data collection methods and lab processing
- Sampling cadence for each core:
  - First measurement (stock): 24 intervals of 5 minutes each.
  - Second measurement: 3 months after the first (12 intervals of 5 minutes).
  - Third measurement: 3 months after the second (same method as second).
  - Fourth measurement (after one year): new core ~30 cm away; 24 intervals (sampling restarts with the 24-interval protocol).
- At each sampling, soil temperature (inside and outside core) and soil humidity (inside and outside core) were recorded.
- Root processing: samples washed through a 2 mm sieve, oven-dried at 60°C for 72 hours, and weighed.
- Lab and field notes captured per sample.

## Data structure and key fields
- Date: date of data collection.
- Catchment: microcatchment (~5,000 ha) containing the plot.
- Transect: plot number within each catchment (bacia).
- Plot: unique code combining catchment and transect.
- Forest: disturbance class before the 2015–16 El Niño.
- Fire_ElNino: whether the plot burned during the 2015–16 El Niño (1 = fire, 0 = no fire).
- Core number: identifier for each in-growth core.
- Interval: five-minute interval index for root collection.
- Stock: indicator for the first measurement of each core (1 = stock, 0 = not stock).
- Weight (g): sample mass.
- Lab_notes: notes from laboratory processing.
- Temperature (inside/outside): soil temperature before sampling.
- Humidity (inside/outside): soil humidity before sampling.
- Field notes: field processing observations.

## Spatial and temporal coverage
- Plot coordinates provided for 20 plots (codes such as 112_12, 112_8, 129_10, etc.), with corresponding latitudes and longitudes.
- Temporal coverage spans 2014–2018, including pre- and post-disturbance conditions and the El Niño event.

## Implications for environmental monitoring and analysis
- Enables assessment of belowground carbon dynamics and root production responses to different disturbance regimes.
- Facilitates time-series analysis of root production under changing disturbance and climate conditions.
- Data are structured to be combined with other environmental datasets, enhancing cross-study monitoring and policy evaluation.

## Access and interoperability considerations
- Roots.csv is a structured, field- and lab-validated dataset designed for standard data pipelines.
- Metadata supports dataset integration, QA, and reuse in environmental monitoring programs.
- Aligns with general monitoring aims of enabling data access, verification, and broader applicability beyond a single study.