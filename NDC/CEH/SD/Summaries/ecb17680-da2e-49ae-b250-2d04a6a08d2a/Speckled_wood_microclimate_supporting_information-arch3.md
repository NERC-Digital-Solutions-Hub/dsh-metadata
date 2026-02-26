# WINTER AND SUMMER SPECKLED WOOD SURVIVAL AND PERFORMANCE

## Overview
- Aimed to assess survival rates and larval performance of F1 offspring of wild-caught P. aegeria in different habitats (woodland vs grassland) during winter and summer.
- Adults were captured near the northern range boundary in England and reared to produce offspring on Poa pratensis hosts in controlled greenhouse conditions.
- Field experiments involved placing replicated larval pots at nearby woodland and grassland sites to evaluate development, mass, growth, and survival under real-world habitat conditions.
- Data were collected through a combination of field experiments, laboratory cold-tolerance tests, and plant quality assessments to understand habitat and climate impacts on performance.

## Experimental design and sites
- Adults collected in August 2008 and July 2009 at a woodland site (Bishop Wood) and reared to lay eggs on potted host plants.
- Larvae transferred to fresh host plants and deployed at field sites near the capture location, with nets to prevent grazing, predation, and larval dispersal.
- Winter experiment: 40 pots per site (woodland: Bishop Wood; grassland: Wistow) set up in September and overwintered to June; 5–15 larvae per pot from one female per site (split brood design).
- Summer experiment: 7 pots per site (3 woodland sites: The Grange, Bishop Wood, Skipwith Common; 3 grassland sites: University of York Campus, Wistow, Skipwith Common) placed in early August and left to desiccate until late September; larvae from each female split across treatments.
- Measurements included development time, pupal mass, growth rate, and survival (pupated or alive at end of period).

## Winter_survival_and_performance.csv
- Habitat: W = woodland, G = grassland.
- Female: code identifying the contributing adult female.
- Alive: number that pupated during the period.
- Dead: number that died during the period.
- Development time: average weeks (winter) to pupation; NA if no pupation.
- Pupal mass: average mg at pupation; NA if no pupation.
- Growth rate: average mg/week; NA if no pupation.

## Summer_survival_and_performance.csv
- Habitat: W = woodland, G = grassland.
- Site: woodland sites (1 The Grange, 2 Bishop Wood, 3 Skipwith Common); grassland sites (1 University of York Campus, 2 Wistow, 3 Skipwith Common).
- Pot: pot code (uneven due to losses).
- Alive as larvae: number alive as larvae at end.
- Alive as pupae: number that pupated.
- Dead: number that died during the period.
- Development time: average days to pupation; NA if no pupation.
- Pupal mass: average mg at pupation; NA if no pupation.
- Growth rate: average mg/day; NA if no pupation.

## Winter_microclimate.csv
- Data loggers: 4 loggers per site at 30 cm above ground, within netting, hourly readings.
- Logger data: temperature (°C) from each logger, foil-wrapped to reduce solar insolation effects.
- Instrument: iButton DS1922L, accuracy ~0.4 °C.
- Structure: Date/time column and habitat-site/logger-specific columns; uneven numbers due to logger failures.

## Summer_microclimate.csv
- Similar to winter microclimate data, with hourly temperature readings from loggers at each site and habitat.
- Structure: Date/time column and habitat/site/logger-specific columns; uneven logger counts due to failures.

## Summer host plant quality
- Potted grass water content
  - Habitat: W or G.
  - Site: woodland sites (The Grange, Bishop Wood, Skipwith Common) or grassland sites (University of York Campus, Wistow, Skipwith Common).
  - Pot: pot code.
  - Percentage water content: water content of pot grass sample.
  - NA where pot was lost.
- Wild grass water content
  - Habitat, Site, Sample: sample identifier within site.
  - Percentage water content: water content of nearby wild grass.
  - NA where no grass was available.

## SPECKLED WOOD COLD TOLERANCE
- Assessed lethal and sublethal effects of cold exposure on larvae under controlled conditions.
- Larvae exposed to -5 °C or -10 °C after a 3-day pre-feeding halt, then recovered at 5 °C for two days.
- Sampling: groups of 10 larvae per treatment; multiple time-point removals to assess responses.
- Post-treatment performance: survival to pupation and eclosion, development time to pupation, pupal mass, and growth rate.
- Control group: maintained at 5 °C for 8 days to compare extreme cold effects.
- Measurements recorded as percentages and means (immediate survival, pupation, eclosion, development time, pupal mass, growth rate).

## Data quality and governance considerations for monitoring frameworks
- The study illustrates the integration of multi-source data (field experiments, lab assays, microclimate sensors, and plant quality measures) to evaluate environmental effects on a species.
- Key monitoring considerations aligned with monitoring-framework priorities:
  - Data availability and accessibility: multiple datasets with structured columns enable cross-analysis across habitat, site, and time.
  - Metadata and data quality: explicit variable definitions and units; presence of NA values and uneven replication highlights metadata completeness needs.
  - Data integrity and provenance: trials occurred across numerous sites with brood-level replication; some pots and loggers were lost or failed, introducing gaps.
  - Data governance: sharing underlying data and ensuring clear documentation for reproducibility and transparency.
  - Communication of complex results: a combination of survival, development, and growth metrics across habitats requires clear, policy-relevant summaries for decision-makers.
- Implications for monitoring frameworks:
  - Demonstrates designing multi-layer monitoring programs combining organisms, microclimate context, and habitat quality.
  - Emphasizes the need for robust metadata, standardised data formats, and strategies to minimize data loss and handle missing data.
  - Supports creation of dashboards or reports that integrate lab and field findings to inform habitat management and climate resilience policies.