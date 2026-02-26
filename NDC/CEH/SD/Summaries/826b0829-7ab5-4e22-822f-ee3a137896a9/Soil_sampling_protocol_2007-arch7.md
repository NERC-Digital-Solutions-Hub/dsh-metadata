# Soil Core Sampling Protocol for X-plots

- Purpose: Collect and prepare soil core samples and a composite soil sample from each X-plot square for analysis, with careful labeling, storage, and dispatch to regional laboratories.

## Key data and design points relevant to GIS

- Each X-plot yields five samples: four cores (C, F, N, P) plus one composite sample from 8–10 sub-samples around the 5 m quadrat boundary.
- Core locations are defined relative to the centre quadrat:
  - Core C (Black): 15 cm south of the centre quadrat corner.
  - Core F (Short White): 15 cm east of Core C.
  - Core N (Long White): 15 cm south of Core C (30 cm from the south corner of the centre quadrat).
  - Core P (Long Grey): 15 cm west of Core C; ensure the bevelled end is on the soil surface.
- Composite sample: collected along the boundary of the 5 m quadrat, 8–10 sub-samples at depths of 15 cm, distributed with at least two samples on each side of the quadrat.

## Equipment and packing (highlights)

- Portable field kit includes:
  - Electric Cold Box (powered from vehicle lighter socket) and mains charger for accommodation use
  - Core-specific bags, end caps, and mailbags for 5 X-plots
  - Tools: knives, hammers, pliers, mallet, trowels (regular and long thin), notebook and pen
  - Packaging materials: parcel tape, spare cores, labelled bags
- Core-specific labeling and bagging:
  - Each core has its own labeled bag; cores stored by type and square for cooling and transport

## Sampling procedures (step-by-step highlights)

- General guidelines
  - If problems arise (e.g., large roots, unusual vegetation, rocks), note in the envelope with specifics
  - Move sampling point as needed to obtain a homogeneous, sensible location; record any deviations
  - Clear vegetation and debris from the surface before sampling
  - Take care not to lose soil when extracting cores; use spare pipes if needed
- Core C: Black core
  - 15 cm long, 5 cm diameter; locate 15 cm south of centre quadrat corner
  - Use the bevelled end on the soil surface; place in bag and seal
- Core F: Short White core
  - 8 cm long, 4 cm diameter; locate 15 cm east of Core C
  - Leave litter layer intact; once sampled, cap ends, seal in bag
- Core N: Long White core
  - 15 cm long, 4 cm diameter; located 15 cm south of Core C (30 cm from south corner)
  - Cap ends, seal, and bag
- Core P: Long Grey core
  - 15 cm long, 4 cm diameter; locate 15 cm west of Core C
  - Must be right side up with bevelled end on soil surface; cap ends, seal, and bag
- Composite soil sample (SQID sample)
  - Collect 8–10 sub-samples using long thin trowel around the 5 m quadrat boundary
  - Depth to 15 cm; place into a single bag, filling to the top white panel
  - If insufficient depth, repeat until the bag is full, then seal (bag inside another bag if needed)
  - Return composite sample to its labelled bag

## Post-collection handling and storage

- Immediate handling after field collection
  - Core C: place in its bag; once all black cores for the square are collected, store together in a spare bag
  - Core F: store with other short white cores from the square in the cool box; after five samples, place in CEH Lancaster mailbag
  - Core P: store with other long grey cores from the square in the cool box; after five samples, mail to CEH Lancaster
  - Core N: store with other long white cores from the square in the cool box; after five samples, mail to CEH Bangor
  - Soil Sample Bag (composite): place in the cool box, then mail to CEH Lancaster
- Dispatch
  - Post samples as soon as possible
  - If last post is Thursday and cannot be posted that day, leave in the cool box over the weekend and post Monday
  - Do not post on Fridays
  - If local post boxes cannot accommodate the packages, use a convenient Post Office
  - Check OS map data or Road Atlas for Post Office locations

## Data alignment considerations for GIS

- Sampling positions are explicitly tied to the centre quadrat; geospatial mapping should encode:
  - Absolute or relative coordinates for each core (C, F, N, P) per square
  - The exact orientation and measurement references (south, east, west from the black core)
  - The 5 m quadrat boundary for composite sampling
- Maintain careful metadata on: sampling date/time, core IDs, lot/bag IDs, and any deviations or notes about unusual conditions
- Ensure downstream data products can link each sample to its square identifier and the corresponding GIS polygon for the X-plot