# Litterfall in human-modified forests of Eastern Amazonia

## Overview
- Dataset: Litterfall.csv documenting litterfall measurements in 20 Amazonian forest plots (each 250 x 10 m) across a disturbance gradient prior to El Niño.
- Disturbance classes (5 plots each): undisturbed primary forests, logged primary forests, logged-and-burned primary forests, and secondary forests.
- Timeframe: Data collected from February 2015 to October 2018; part of the NERC Human-modified Tropical Forests Programme (HMTF).

## Study design and data collection
- Sampling design: Six litter traps per plot (0.25 m2 each) arranged 50 m apart; traps located 1.20 m above ground.
- Sampling frequency: Contents collected every two weeks.
- Sample processing: Field-collected material separated into six components (leaves, flowers, fruits, seeds, wood, rest), oven-dried at 80°C for 3 days, then weighed to 0.01 g precision.
- Data captured per trap: Site metadata, disturbance class, El Niño fire status, date, team, and component masses.

## Spatial and temporal scope
- Spatial coordinates: 20 plots with explicit coordinates (Latitude and Longitude) provided for each plot identifier (e.g., 112_12, 112_8, 129_10, etc.), covering multiple catchments (microcatchments ~5,000 ha).
- Temporal coverage: Repeated measurements over the 2015–2018 period, enabling temporal analysis of litter flux in relation to El Niño events and disturbance history.

## Data structure and key fields
- Core columns in Litterfall.csv:
  - Catchment, Transect, Plot: Plot and location identifiers.
  - Forest_pre_El_nino: Disturbance class before El Niño (pre-2015-16).
  - El_Nino_fire: Binary indicator if the plot burned during the 2015-16 El Niño (1 = fire, 0 = no fire).
  - Litter: Trap number within each plot (1–6).
  - Day: Data collection date.
  - Team: Field data-collection team.
  - Leaf (g), Wood (g), Flower (g), Seed (g), Fruit (g), Rest (g): Dry weight of each litter component.
  - Total (g): Total dry weight of all components in the trap.
  - Notes: Field notes.
- Data quality: All components weighed to nearest 0.01 g; standardized collection and processing protocol across traps and plots.

## How this data can be used in GIS
- Map-based visualization of litterfall distribution across disturbance types and catchments.
- Spatial integration with canopy disturbance history (1988–2010) and El Niño fire status for multi-layer analyses.
- Temporal analysis of litter flux components (leaf, wood, flower, seed, fruit, rest) across 2015–2018.
- Potential to combine with ancillary spatial datasets (e.g., land-use change, fire scars) to assess drivers of litter production.

## Provenance and access
- Data provenance: Collected as part of the HMTF programme; dataset includes explicit disturbance classifications and El Niño-related fire data.
- Access: Litterfall.csv attached with comprehensive metadata and coordinate information for GIS use.