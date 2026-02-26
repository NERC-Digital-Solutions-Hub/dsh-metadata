# Data on flight-induced maternal effects and offspring performance on drought stressed plants in the Speckled Wood butterfly, Pararge aegeria

## Overview
- A laboratory dataset examining whether repeated flight during female oviposition affects egg provisioning and offspring performance when larvae are reared on drought-stressed host plants.
- Also tests whether flight-induced maternal effects persist to influence adult offspring dispersal abilities in drought-affected contexts.
- Aims to explore mechanisms by which drought and habitat fragmentation impact biodiversity.

## Experimental design and data collection
- Origin: females from an outbred laboratory stock from St. Hubert, Belgium.
- Maternal flight treatment: females assigned to control (no forced flight) or forced flight. Forced flight involved 5 minutes of flight per event, repeated on three oviposition days (the day after mating and on days 4 and 8 of oviposition).
- Reproductive output data: longevity (days from adult eclosion to death), lifetime fecundity (total eggs laid), total lifetime egg hatch success, and mean egg size.
- Embryonic development data: on days 2, 4, 6, 8, and 10 of oviposition, five eggs per day were photographed for size, then monitored for hatching; recorded egg survival and embryonic development time (days from laying to hatch).
- Offspring performance on drought-stressed hosts: on hatching day, one larva per female per oviposition day reared on drought-stressed plants. Recorded development time to pupation, pupal mass, survival to eclose, adult sex, dry body mass, dry thorax mass, and flight muscle mass (as a proxy for flight ability).

## Datasets and key variables
- Female_reproductive_output_data.csv
  - FemaleID; FemaleMass_mg (adult mass at eclosion); MaternalFlight (C = control, F = forced flight); LifetimeFecundity; Longevity (days); LifetimeEggHatch; MeanEggSize.
- Embryonic_development_data.csv
  - OffspringID; EggSize (size on day laid); DayLaid; EmbryonicTime (days from lay to hatch); Hatch (y/n); MotherID; MaternalFlight; MaternalLongevity; MaternalMass_mg.
- Offspring_performance_data.csv
  - OffspringID; DryAdultMass_mg; DryThoraxMass_mg; EggSize; DayLaid; PupalMass_mg; TotalDevTime; Sex (F/M); MotherID; MaternalFlight; SurviveToEclose (y/n).

- Notes
  - Empty cells indicate missing data (e.g., due to death).
  - All measurements taken under standardized laboratory conditions with published methods.

## Data quality and provenance
- Standardised laboratory procedures and data collection methods.
- Data entry supported by quality assurance tools (input masks, conditions) to ensure data coherence.

## Relevance to data leadership and governance
- Comprehensive, well-documented data with clear identifiers, units, and coding for categorical variables, supporting discoverability and reuse.
- Three linked datasets enable cross-domain analyses (reproductive output, embryonic development, and offspring performance) and potential meta-analyses on drought-stress effects and maternal influences.
- Clear metadata and methodological transparency help assess data suitability, gaps, and quality for broader data ecosystems and collaborations.

## Potential uses for data leaders
- Assess data strategy for ecological experiments: provenance, metadata completeness, and discoverability.
- Inform data governance decisions around standardizing experimental ecology data (units, coding, and file structure).
- Enable cross-study comparisons and integration to study biodiversity responses to drought and habitat fragmentation.
- Identify data gaps (e.g., additional trait measures, broader environmental conditions) and plan for harmonized data collection in future projects.