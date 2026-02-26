# Litterfall in human-modified forests of Eastern Amazonia

- The dataset captures litterfall measurements across 20 Amazonian forest plots along a gradient of prior human disturbance, with plots classified into undisturbed primary, logged primary, logged-and-burned primary, and secondary forests.
- Sampling period spans from February 2015 to October 2018 (biweekly collection), as part of the NERC Human-modified Tropical Forests Programme (HMTF; Grant NE/K016431/1).

## Study design and disturbance classification

- Plots are 250 m x 10 m (per plot) and distributed across catchments with a microcatchment (~5,000 ha).
- Disturbance classifications before the 2015-16 El Niño were determined through:
  - Canopy disturbance analysis using a satellite image chronosequence (1988–2010)
  - Field assessments of fire scars, charcoal, and logging debris
- El Niño fire status is captured per plot (El_Nino_fire: 1 = burned, 0 = not burned).

## Data collection methods

- Six litterfall traps per plot (each 50 x 50 cm; 0.25 m2), placed 1.20 m above ground and spaced 50 m apart.
- Traps collected every two weeks from February 2015 to October 2018.
- Field samples were brought to a lab and separated into six components: leaves, flowers, fruits, seeds, wood, and rest (non-identifiable material).
- Samples were oven-dried at 80°C for 3 days and weighed to the nearest 0.01 g.
- Trapped litter totals are recorded as Total (g) per sample.

## Spatial and plot metadata

- Coordinates for plots are provided (lat/long for each plot; listed in the dataset as multiple plot codes such as 112_12, 112_8, etc.).
- Each plot is identified by a combination of Catchment, Transect, and Plot codes for unique tracking.

## Data structure and key fields

The dataset is delivered as a comma-separated file with the following columns:
- Catchment: microcatchment where the plot is located
- Transect: plot number within each catchment
- Plot: unique plot code combining catchment and transect
- Forest_pre_El_nino: disturbance class before El Niño (pre-El Niño)
- El_Nino_fire: whether the plot burned during the 2015-16 El Niño (1 = fire, 0 = no fire)
- Litter: litter trap number within the plot (1–6)
- Day: date of data collection
- Team: data collecting team
- Leaf (g): dry weight of leaves
- Wood (g): dry weight of woody material
- Flower (g): dry weight of flowers
- Seed (g): dry weight of seeds
- Fruit (g): dry weight of fruits
- Rest (g): dry weight of other materials
- Total (g): total dry weight of litter in the trap
- Notes: field notes

## Relevance for environmental monitoring

- The standardized measurement approach (consistent trap size, height, and drying/weight protocol) supports time-series analyses of litterfall across disturbance gradients.
- The dataset enables monitoring of how prior disturbance and El Niño events influence organic input to the forest floor.
- Data are suitable for integration with other environmental datasets, aligning with goals to increase data value and improve access to underlying data for policy-relevant monitoring.

## Data quality and usage considerations

- Data were collected under a structured field protocol and quality-controlled through lab processing (drying and precise weighing).
- Disturbance classifications combine remote sensing and field validation to ensure robust categorization.
- The dataset is intended to be stored and shared through appropriate data portals, supporting broader accessibility and reuse.