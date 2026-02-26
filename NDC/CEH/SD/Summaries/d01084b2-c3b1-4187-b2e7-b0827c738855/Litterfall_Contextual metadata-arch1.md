# Litterfall in human-modified forests of Eastern Amazonia

## Overview
- Dataset of litterfall measurements from 20 Amazonian forest plots (each 250 x 10 m) across a disturbance gradient prior to the 2015-16 El Niño.
- Disturbance classes: undisturbed primary forests (n=5), logged primary forests (n=5), logged-and-burned primary forests (n=5), and secondary forests (n=5).
- Data collected from January 2015 to October 2018 as part of the NERC Human-modified Tropical Forests Programme (HMTF).

## Data collection methods
- Six litterfall traps per plot (50 x 50 cm; total area 0.25 m2), placed 1.20 m above ground and spaced 50 m apart.
- Traps installed in each plot; contents collected every two weeks from February 2015 to October 2018.
- Field lab processing: samples separated into six components—leaves, flowers, fruits, seeds, wood, and rest (non-identifiable parts).
- Samples oven-dried at 80°C for 3 days and weighed to the nearest 0.01 g.
- Data collection teams and day records maintained.

## Spatial and temporal coverage
- Microcatchment scale: ~5,000 ha per catchment.
- Plot-level coordinates provided for each plot (latitude and longitude listed for all plots).
- Timeframe: January 2015 through October 2018, with El Niño-related sampling occurring during 2015-2016.

## Data structure and key variables
- File: Litterfall.csv
- Columns include:
  - Catchment, Transect, Plot: identifiers for location and plot within catchments
  - Forest_pre_El_nino: disturbance class before the 2015-16 El Niño
  - El_Nino_fire: presence of fire during the 2015-16 El Niño (1 = yes, 0 = no)
  - Litter: litter trap number within each plot (1–6)
  - Day: date of data collection
  - Team: data collection team
  - Leaf (g), Wood (g), Flower (g), Seed (g), Fruit (g), Rest (g): dry weights of each litter component
  - Total (g): total dry weight of litter per trap
  - Notes: field notes
- Data file is accompanied by comprehensive coordinates and site descriptions for replication and cross-referencing.

## Data processing and classification
- Disturbance classification derived from satellite imagery (1988–2010 chronosequence) and field assessments of fire scars, charcoal, and logging debris.
- El Niño context used to identify plots that burned during the 2015-16 event.
- Data formatted for aggregation and analysis by plot, limb of disturbance category, and across time.

## Potential analyses and uses
- Assess impact of past disturbance (undisturbed, logged, logged-and-burned, secondary) on total litterfall and its components.
- Examine temporal dynamics of litter production across 2015–2018, including during El Niño-related events.
- Partition analyses by litter component (leaves, wood, flowers, seeds, fruits, rest) to understand how disturbance and climate interact to affect different litter pools.
- Use El_Nino_fire and Forest_pre_El_nino variables to model how fire exposure moderates litter production.
- Cross-plot comparisons within and between catchments to evaluate spatial variability in litter dynamics.

## Access and provenance
- Data originate from the NERC Human-modified Tropical Forests Programme (HMTF), Grant No. NE/K016431/1.
- The dataset is provided as Litterfall.csv with detailed field and processing metadata to support reproducibility and further analysis.