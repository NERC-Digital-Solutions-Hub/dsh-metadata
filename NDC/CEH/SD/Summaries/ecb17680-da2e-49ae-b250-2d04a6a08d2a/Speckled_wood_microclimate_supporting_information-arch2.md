# WINTER AND SUMMER SPECKLED WOOD SURVIVAL AND PERFORMANCE

## Overview and aims
- Reared F1 larval offspring from wild-caught Pontia aegeria to assess survival and larval performance across winter and summer habitats in the UK.
- Compare outcomes between woodland and grassland habitats, across multiple sites and seasons, to understand environmental effects on development and growth.
- Data collected to be stored and made available for analysis alongside environmental context (microclimate and host-plant quality).

## Experimental design and methods

### Winter experiment (2008–2009)
- Sites: 1 woodland and 1 grassland site in the UK.
- Procedure: Adults collected in August 2008 near the species’ northern range boundary; eggs laid on potted Poa pratensis in greenhouses; larvae transferred to pots (5–15 larvae per pot) with nets to protect from grazing, predation, and dispersal.
- Setup: 40 pots per site; split brood design (larvae from one female contributed to one pot per site).
- Timeline: Pots deployed in September; overwintered until June with plant replacement as needed.
- Measurements: development time (weeks from field placement to pupation), pupal mass (mg), larval growth rate (mg per week), survival (percentage pupating or surviving to end).
  
### Summer experiment (2009)
- Sites: 3 woodland and 3 grassland sites.
- Procedure: Similar rearing from field-collected adults; larvae placed on fresh potted host plants; desiccation allowed in field.
- Setup: 7 pots per site; 5 larvae per pot with split broods; uneven pot numbers due to disturbances.
- Timeline: Began in August; ended in September.
- Measurements: development time (days to pupation), pupal mass (mg), growth rate (mg per day), survival (alive as larvae, alive as pupae, dead).

## Data and outputs

### Winter survival and performance dataset
- File: Winter_survival_and_performance.csv
- Key columns:
  - Habitat (W = woodland, G = grassland)
  - Female (offspring lineage code)
  - Alive (num. pupated)
  - Dead (num. died)
  - Development time (weeks)
  - Pupal mass (mg)
  - Growth rate (mg/week)
- Notes: NA for variables not applicable (e.g., when no pupation occurred). Uneven pot numbers across sites.

### Summer survival and performance dataset
- File: Summer_survival_and_performance.csv
- Key columns:
  - Habitat
  - Site (woodland: 1 The Grange, 2 Bishop Wood, 3 Skipwith Common; grassland: 1 University of York Campus, 2 Wistow, 3 Skipwith Common)
  - Pot (pot code)
  - Alive as larvae
  - Alive as pupae
  - Dead
  - Development time (days)
  - Pupal mass (mg)
  - Growth rate (mg/day)
- Notes: Uneven number of pots between sites due to disturbances.

## Microclimate data

### Winter microclimate
- File: Winter_microclimate.csv
- Data: Hourly temperature readings (°C) from four loggers placed 30 cm above the ground at each site; loggers wrapped to minimise solar effects.
- Columns: Date and time, plus one column per logger (labeled by habitat and logger code); uneven logger counts due to failure.

### Summer microclimate
- File: Summer_microclimate.csv
- Data: Hourly temperature readings (°C) from four loggers per site/habitat; site codes and logger codes indicated in headers.
- Columns: Date and time, habitat-letter, site-code, logger-code; uneven logger counts due to failure.

## Summer host plant quality

### Potted grass water content
- File structure: Habitat, Site, Pot, Percentage water content
- Purpose: Assess water content of potted Poa pratensis at pots to relate plant quality to larval performance.

### Wild grass water content
- File structure: Habitat, Site, Sample, Percentage water content
- Purpose: Compare water content of nearby wild grass to potted plants for contextual quality differences.

## Speckled Wood cold tolerance (laboratory)

### Cold exposure experiment
- Larvae were kept at 13°C, starved briefly to clear gut content, then exposed to -5°C or -10°C at 1°C per minute.
- Sampling: For each exposure, subsets of larvae were removed after 1–8 days depending on temperature to assess survival post-treatment and performance.
- Post-treatment: Surviving larvae returned to host plants; monitored for pupation and eclosion.

### Control
- A control group kept at 5°C for 8 days, matching the longest exposure duration.

### Measured outcomes
- Immediate survival after treatment
- Successful pupation
- Successful eclosion
- Development time (days) to pupation after treatment
- Pupal mass (mg)
- Growth rate (mg/day) after treatment

### Cold tolerance dataset
- File: Cold_tolerance.csv
- Key columns:
  - Exposure temperature (°C)
  - Duration of exposure (days)
  - Sample
  - Immediate survival (%)
  - Successful pupation (%)
  - Successful eclosion (%)
  - Development time (days)
  - Pupal mass (mg)
  - Growth rate (mg/day)

## Data use and integration opportunities (for Analysts Monitoring the Environment)
- Standardised, multi-habitat temporal data to compare environmental effects on survival, growth, and development across seasons.
- Potential to integrate survival and growth data with microclimate measurements to identify climate- or habitat-driven patterns.
- Host plant quality data enables analysis of resource-driven performance differences between controlled (pots) and natural (wild grass) conditions.
- Cold tolerance data provides mechanistic understanding of physiological limits under extreme conditions, useful for predicting responses to cold events.
- Datasets are structured for reuse and cross-comparison, supporting monitoring and policy assessment of environmental health and species resilience.

## Challenges and considerations
- Uneven sample sizes and pot counts due to disturbances and equipment failure (loggers).
- Some measurements are NA when no survival or pupation occurred, requiring careful handling in analyses.
- Data coverage spans limited sites per season, which should be considered when generalising across broader landscapes.