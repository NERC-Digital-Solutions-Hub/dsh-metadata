# Litterfall in human-modified forests of Eastern Amazonia

## Overview
- A CSV dataset (Litterfall.csv) documenting litterfall in 20 Amazonian forest plots across a disturbance gradient prior to the El Niño period, categorized as undisturbed primary, logged primary, logged-and-burned primary, and secondary forests.
- Data collected from January 2015 to October 2018 as part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).
- Six litter traps per plot (0.25 m2 each) deployed 1.20 m above ground, with contents collected biweekly and processed in the field lab.

## Data collection methods
- Traps: six per plot, spaced 50 m apart; contents separated into leaves, flowers, fruits, seeds, wood, and rest; dried at 80°C for 3 days and weighed to the nearest 0.01 g.
- Sampling cadence: biweekly collections from February 2015 to October 2018.
- Data processing: field lab separation and weighing, yielding total litter per trap per collection date.
- Disturbance classification: based on canopy disturbance inferred from a satellite-based chronosequence (1988–2010) plus field assessments of fire scars, charcoal, and logging debris.

## Study sites and coordinates
- 20 plots across multiple catchments (5 plots per disturbance class).
- Disturbance classes: undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests prior to the 2015–16 El Niño.
- Plot coordinates are provided (latitude and longitude) for each microcatchment/plot.

## Data structure and key fields
- Catchment: microcatchment (~5,000 ha) where each plot is located.
- Transect: plot number within each catchment.
- Plot: unique plot code (combination of catchment and transect).
- Forest_pre_El_nino: disturbance class before the 2015–16 El Niño.
- El_Nino_fire: whether the plot burned during the El Niño (1 = fire, 0 = no fire).
- Litter: litter trap number (1–6) per plot.
- Day: date of data collection.
- Team: data-collection team.
- Leaf (g), Wood (g), Flower (g), Seed (g), Fruit (g), Rest (g): dry weight of each litter component.
- Total (g): total dry weight of contents in the trap.
- Notes: field notes.

## Temporal scope and provenance
- Timeframe: January 2015 – October 2018.
- Data provenance: field-collected measurements for the HMTF program; dataset attached as CSV with detailed column descriptions.

## Access and usage considerations for data support
- Format: comma-separated values (CSV) with clearly labeled columns suitable for aggregation, filtering by disturbance class, El Niño period, or plot.
- Potential analyses: compare litterfall totals and component contributions across disturbance classes; assess effects of El Niño fire on litter input; temporal trends within and across plots; integration with canopy disturbance data or fire history.
- Data quality notes: consistent measurement protocol (80°C drying, 0.01 g precision); ensure alignment of dates, trap IDs, and plot codes; consider missing collections or field notes in downstream analyses.