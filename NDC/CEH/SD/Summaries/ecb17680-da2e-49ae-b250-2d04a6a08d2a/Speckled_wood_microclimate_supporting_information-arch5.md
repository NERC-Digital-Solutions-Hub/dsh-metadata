# WINTER AND SUMMER SPECKLED WOOD SURVIVAL AND PERFORMANCE

## Overview
- A multi-component study on the survival and performance of F1 larvae from wild-caught adult Pararge aegeria (speckled wood) reared in winter 2008-2009 and summer 2009 across UK woodland and grassland sites.
- Aims to quantify larval survival, development time, mass, and growth under different habitat conditions, microclimates, and host-plant quality; includes a controlled cold-tolerance component.
- Data are organized into species-specific datasets, with clear variable definitions and site/habitat coding to support cross-site comparisons and replication.

## Experimental design and data collection

- Source and rearing
  - Adults captured in a woodland site near the northern range boundary (Bishop Wood, North Yorkshire, England, Aug 2008; Jul 2009).
  - Adults kept separately to lay eggs on potted Poa pratensis in York greenhouses.
  - Grass seed sourced commercially and grown under controlled potting conditions; larvae transferred to fresh host plants at second instar and placed at experimental sites.
  - Netting used to protect plants and larvae; pots anchored flush with soil surface.

- Winter experiment
  - Sites: 1 woodland (Bishop Wood) and 1 grassland (Wistow) in Sep; overwintered until Jun.
  - Setup: 40 pots per site; 5–15 larvae per pot; split brood design (larvae from one female contributed to one pot per site).
  - Measurements: development time (weeks to pupation), pupal mass, larval survival (pupated or still alive), growth rate (mass/time).

- Summer experiment
  - Sites: three woodland sites (Bishop Wood, The Grange, Skipwith Common) and three grassland sites (University of York Campus, Wistow, Skipwith Common) in Aug; observed until end of Sep.
  - Setup: 7 pots per site; 5 larvae per pot; larvae from each female split evenly across treatments; random pot assignment within treatments.
  - Measurements: development time (days to pupation), pupal mass, growth rate; larval/pupal survival tracked.

- Microclimate monitoring
  - Winter and Summer: 4 temperature loggers per site at 30 cm above ground; hourly readings; loggers wrapped to minimize solar effects; iButton DS1922L, 0.4 °C accuracy within experimental ranges.
  - Purpose: relate microclimate conditions to survival and performance outcomes.

- Summer host-plant quality
  - Assessment of grass water content
  - Potted plant samples: 3 cm diameter grass sections taken flush with soil from each pot; samples weighed, oven-dried (60 °C, 24 h), re-weighed to compute water content.
  - Wild grass samples collected near pots (2 m and 4 m transects) for comparative water-content analysis.

- Speckled wood cold tolerance (controlled laboratory experiments)
  - Larvae held at 13 °C on potted host plants; 3-day pre-treatment fasting to reduce gut content.
  - Cold exposure: -5 °C or -10 °C, ramped at 1 °C per minute; post-exposure recovery and subsequent development tracked.
  - Timepoints: samples removed after specified durations (2, 4, 6, 8 days for -5 °C; 1–4 days for -10 °C); a 5 °C control group used for comparison.
  - Measurements: immediate survival, pupation success, eclosion success, development time to pupation, pupal mass, growth rate post-treatment.

## Datasets and key variables

- Winter_survival_and_performance.csv
  - Habitat (W = woodland, G = grassland)
  - Female (code identifying contributing adult)
  - Alive (number pupated)
  - Dead (number died)
  - Development time (weeks; NA if no pupation)
  - Pupal mass (mg; NA if no pupation)
  - Growth rate (mg/week; NA if no pupation)

- Summer_survival_and_performance.csv
  - Habitat (W/G)
  - Site (woodland: 1 The Grange, 2 Bishop Wood, 3 Skipwith Common; grassland: 1 University of York Campus, 2 Wistow, 3 Skipwith Common)
  - Pot (pot code)
  - Alive as larvae
  - Alive as pupae
  - Dead
  - Development time (days; NA if no pupation)
  - Pupal mass (mg; NA if no pupation)
  - Growth rate (mg/day; NA if no pupation)

- Winter_microclimate.csv
  - Date and time (hourly)
  - Temperature readings (°C) for each data logger
  - Column naming indicates habitat (W or G) and logger code
  - Note: uneven number of loggers due to failures

- Summer_microclimate.csv
  - Date and time (hourly)
  - Temperature readings (°C) for each data logger
  - Structure similar to Winter_microclimate.csv with site codes and logger identifiers
  - Note: uneven number of loggers due to failures

- SUMMER HOST PLANT QUALITY (Potted grass)
  - Habitat (W/G)
  - Site (The Grange, Bishop Wood, Skipwith for woodland; University of York Campus, Wistow, Skipwith Common for grassland)
  - Pot (pot code)
  - Percentage water content (pot samples)

- Wild grass water content
  - Habitat (W/G)
  - Site
  - Sample (sample number within site)
  - Percentage water content (wild grass samples)

- SPECKLED WOOD COLD TOLERANCE.csv
  - Exposure temperature (°C): -5 or -10
  - Duration of exposure (days)
  - Sample (replicate grouping of 10 larvae)
  - Immediate survival (%)
  - Successful pupation (%)
  - Successful eclosion (%)
  - Development time (days to pupation; NA if no pupation)
  - Pupal mass (mg; NA if no pupation)
  - Growth rate (mg/day; NA if no pupation)

## Data quality, limitations, and governance notes

- Data quality considerations
  - Some pots were lost or disturbed (uneven pot counts by site).
  - Loggers failed at certain sites, leading to uneven microclimate data coverage.
  - Some measurements are NA when there is no successful pupation or eclosion, affecting certain analyses.
  - Experimental conditions (e.g., enclosure netting, field desiccation) introduce potential variability across sites and treatments.

- Provenance and metadata
  - Datasets include explicit column definitions and site/habitat codings to facilitate cross-dataset linkage.
  - Replication structure is described (split brood design in winter; split larvae across treatments in summer).
  - Host-plant and microclimate measurements accompany performance data to enable habitat-quality analyses.
  - Geographical references for sites are provided (OS grid references in the narrative, site names included in dataset codes).

- Potential data stewardship considerations
  - Ensure consistent use of site codes and habitat labels across all datasets for cross-referencing.
  - Maintain notes on logger failures and pot losses to support transparent data quality assessments.
  - Preserve NA handling conventions and document any imputation decisions if used in analyses.
  - Link individual larvae to parental female codes where appropriate to enable lineage-level analyses.
  - Ensure datasets are stored with clear metadata, units, and data dictionaries consistent across files.