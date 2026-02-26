# Per-capita impacts of an invasive grass vary across levels of ecological organization in a tropical savanna

## Overview
- Metadata and data package for a study analyzing how the invasive grass Urochloa decumbens impacts ecological organization in the Cerrado across multiple levels (plot to ecosystem).
- Study assesses invasion gradients (0–100% IAS cover) in two protected Cerrado areas: Estação Ecológica de Itirapina (EcEI) and Parque Nacional de Brasília (PNB).
- Data focus areas include microhabitat conditions, plant community structure, leaf traits, biomass, decomposition, species richness, and soil CO2 efflux.

## Study areas and sampling design
- Locations: Estação Ecológica de Itirapina (EcEI) and Parque Nacional de Brasília (PNB), Brazil.
- Invasion context: landscapes invaded by Urochloa decumbens, with invasion started >30 years ago in EcEI (80s) and >20 years ago in PNB (90s).
- Sampling framework:
  - 12 invasion gradients (6 per area) across 0–100% IAS cover.
  - Each gradient contains 5 plots (5 x 5 m) representing 0, 25, 50, 75, 100% IAS cover.
  - Each plot subdivided into a core zone (3 x 3 m) and a marginal zone; core subdivided into nine 1 m2 subplots for vegetation surveys.
  - 60 plots total (5 plots x 6 gradients x 2 areas).
- Microhabitat measurement: hourly light, temperature, and humidity using HOBO sensors; 20 kits per area (4 gradients per area) to reduce spatial pseudoreplication; sensors deployed for at least 130 days from transition between rainy and dry seasons to mid-dry season (April–August 2019).

## Data collection and quality control
- Data collection and QA/QC follow established methods; data structured into seven tables.
- Data collection period: March–April 2019 (with continual microhabitat monitoring into the dry season).
- Data identifiers and provenance: dataset titled “Per-capita impacts of an invasive grass vary across levels of ecological organization in a tropical savanna” with a specified data identifier.

## Data structure and content (seven tables)
- microhabitat: illuminance (PAR), air temperature, and humidity at ground level; area, plot, block, sensor references, time stamps; includes PAR, humidity, and temperature values.
- cover: ground and vegetation cover data by plot and functional group; block, plot, subplot, functional_group, cover.
- specific_leaf_area: SLA measurements by species, plot, block, individual leaves, leaf area, leaf weight, and SLA (SLA.mm2.mg).
- biomass: aboveground biomass by area, block, plot, subplot, and functional_group (kg/m2 or equivalent per area); includes live/dead, native/invasive categories.
- decomposition: litter bag decomposition data including weight start/end, interval, time, and calculated decomposition rate k; includes area, block, plot, weight measurements.
- richness: species richness data by area, block, plot, and functional_group; includes richness counts per category (forbs, graminoids, palms, shrubs, etc.).
- co2_efflux: soil CO2 efflux measurements per plot/subplot with weight gain/blank gain, incubation time, chamber area, and resulting CO2 efflux values.

## Key variables and data structure details
- Microhabitat
  - area: Brasilia (Brasilia) or Itirapina (Itirapina)
  - plot: coded combination of treatment and IAS cover (Q for burn, C for control; and a numeric code for IAS cover level)
  - block: area + block number (e.g., B2, I1)
  - sen.light and sen.humi: sensor reference IDs
  - time: timestamp (day/month/year hour/minute/second)
  - PAR: light level (lux)
  - humidity: % relative humidity
  - temperature: °C
- SLA
  - area, block, plot, species, and identification of individual leaves (area.mm2, leaf, weight.mg)
  - SLA.mm2.mg: leaf-specific area value
- Ground cover
  - area, block, plot, subplot
  - functional_group: bare_soil, bromelia, dead_native, dead_urochloa, forb, graminoid, live_urochloa, other_invasive, palm, shrub
  - cover: percentage cover
- Biomass
  - area, block, plot, subplot, functional_group
  - biomass: biomass per area (kg/m2)
- Richness
  - area, block, plot, subplot (or equivalent) and functional_group
  - richness: species richness count
- Decomposition
  - area, block, plot, weight.start, weight.end, time (in days), interval
  - k: decomposition rate calculated as -log(weight.end/weight.start)/time
- Soil CO2 efflux
  - area, block, plot, subplot
  - weight_gain_g, blank_gain_g, time_h, chamber_area
  - CO2_efflux: g C m-2 day-1

## Experimental design specifics
- Invasion gradient design at coarse scale with five 5 x 5 m plots per gradient representing 0–100% IAS cover.
- Core vs marginal microhabitat differentiation within plots (core 3 x 3 m subdivided into nine 1 x 1 m subplots).
- Vegetation surveys using modified Braun-Blanquet method to estimate species cover by percentage.
- Dominant species (covering ~80% of ground) identified for SLA sampling; leaves collected from 10 individuals per species; leaves rehydrated, scanned or measured with LI-COR devices, dried at 80°C, and weighed for SLA calculation.
- Ecosystem properties include: aboveground biomass, CO2 soil efflux via soda-lime incubation, and decomposition using Urochloa decumbens standing dead biomass in litterbags (90, 120, 160 days).

## Data provenance and references
- Projects and funding acknowledged (Neotropical Grassland Conservancy; FAPESP grants; NERC Newton Grant).
- Reference methods cited for general trait measurements, decomposition, soil CO2 measurement, and Braun-Blanquet cover estimation.

## How this dataset supports environmental monitoring and analysis
- Provides standardized, multi-scale data to assess how an invasive grass influences community composition, plant traits, biomass production, litter dynamics, soil respiration, and carbon cycling across invasion gradients.
- Facilitates cross-comparison with other monitoring datasets and integration with broader environmental indicators.
- Outputs suitable for time-series and gradient-based analyses, maps, and charts to evaluate policy performance and ecological health over time.

## Opportunities for analysts monitoring the environment
- Visualize how invasion intensity correlates with microhabitat conditions, SLA, biomass distribution, and CO2 efflux.
- Compare native vs invasive functional-group dynamics across gradients and sites.
- Integrate with remote-sensing or other environmental datasets to scale up findings beyond the two study areas.
- Use standardized data structures to build dashboards or reporting formats for policy evaluation and monitoring programs.
- Acknowledge data access and reuse considerations, ensuring data remain accessible through appropriate portals and are linked to underlying data sources.