# WINTER AND SUMMER SPECKLED WOOD SURVIVAL AND PERFORMANCE

## Overview
- Examines survival and larval performance of F1 offspring of wild-caught P. aegeria reared in winter and summer across UK woodland and grassland habitats.
- Data assets span survival, development, growth, and mass metrics, plus microclimate data and host-plant quality, plus controlled cold-tolerance experiments.
- Data are organized into multiple CSV files with explicit column definitions and site/habitat coding.

## Experimental Design and Sampling
- Source population: wild-caught adult P. aegeria from a woodland near the species’ northern range boundary; eggs laid on Poa pratensis in greenhouse conditions.
- Field deployment: larvae transferred to fresh host-plant pots near where adults were caught; pots dug in and netted to reduce grazing, predation, and movement.
- Winter experiment:
  - Sites: 1 woodland and 1 grassland in the UK.
  - Setup: 40 pots per site (5–15 larvae per pot) in a split-brood design (offspring from one female in each pot per site).
  - Duration: September to June; plants replenished as eaten.
- Summer experiment:
  - Sites: 3 woodlands and 3 grasslands.
  - Setup: 7 pots per site with ~5 larvae per pot; larvae from each female split evenly and randomly assigned.
  - Duration: early August to late September; pots left to desiccate in the field.
- Measurements:
  - Development time (weeks in winter, days in summer) from field placement to pupation.
  - Pupae mass at pupation; larval/ pupation outcomes; growth rate (mass/time).
  - Affected by uneven pot numbers due to disturbances.

## Data Files and Key Variables
- Winter_survival_and_performance.csv
  - Columns: Habitat (W or G), Female (offspring contributor code), Alive, Dead, Development time (weeks), Pupal mass (mg), Growth rate (mg/week). NA where no pupation occurred.
- Summer_survival_and_performance.csv
  - Columns: Habitat (W or G), Site ( woodland: 1 The Grange, 2 Bishop Wood, 3 Skipwith Common; grassland: 1 York Campus, 2 Wistow, 3 Skipwith Common), Pot, Alive as larvae, Alive as pupae, Dead, Development time (days), Pupal mass (mg), Growth rate (mg/day). NA where no pupation occurred.
- Winter_microclimate.csv
  - Columns: Date/time plus hourly temperature readings for each data logger; Habitat code (W/G) and logger code; note: uneven number of loggers due to failures.
- Summer_microclimate.csv
  - Columns: Date/time plus hourly readings; Habitat code (W/G), Site code, Logger code; note: uneven loggers due to failures.
- Summer Host Plant Quality
  - Potted grass water content: Habitat, Site, Pot, Percentage water content.
  - Wild grass water content: Habitat, Site, Sample, Percentage water content.
- Speckled Wood Cold Tolerance (lab exposure)
  - Columns: Exposure temperature (-5°C or -10°C), Duration (days), Sample, Immediate survival (%), Successful pupation (%), Successful eclosion (%), Development time (days), Pupal mass (mg), Growth rate (mg/day). NA where no pupation occurred.

## Measurements, Methods, and Equipment
- Field: pots with Poa pratensis, netted to prevent predation; plant replacement as needed.
- Development and growth: measured as pupal mass at pupation and growth rate calculated from mass/time.
- Microclimate: iButton data loggers at 30 cm, hourly readings, foil-wrapped to minimize insolation error; accuracy ~0.4°C.
- Host-plant quality: grass samples from pots and nearby wild grass; samples dried at 60°C for 24 h to determine water content.
- Cold tolerance: larvae exposed to -5°C or -10°C in a controlled cabinet, then returned to 5°C; outcomes tracked through pupation and eclosion.

## Data Quality, Gaps, and Considerations
- Missingness and NA values reflect non-pocessed cases (no pupation or survival) and logger/site failures.
- Uneven data across sites (e.g., varying numbers of pots and loggers) due to disturbances or equipment issues.
- Clear site/habitat coding to enable cross-site comparisons and meta-analyses.
- Units explicitly stated (mg, mg/day, mg/week, days/weeks) to support consistency and reproducibility.

## Uses, Implications, and Data Governance Considerations for Data Leaders
- Enables cross-habitat comparisons of larval survival, development, and growth under natural and near-natural conditions.
- Supports analysis of microclimate effects on survival and performance, including comparative winter vs. summer dynamics.
- Provides a dataset to study maximum tolerance to cold exposure and subsequent performance.
- Data governance needs:
  - A unified data dictionary and metadata standard across all files (codes, sites, habitats, units).
  - Documentation of site coordinates, habitat classifications, and pot/larva identifiers to ensure reproducibility.
  - Clear handling of NA values and exceptions (e.g., failed loggers, disrupted pots) for robust analyses.
  - Consideration of cross-dataset linkage (e.g., linking microclimate data to performance outcomes and plant quality).
  - Facilitation of data discoverability and re-use beyond the original study, potentially by sharing with the wider data community.