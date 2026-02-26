# Data on flight-induced maternal effects and offspring performance on drought stressed plants in the Speckled Wood butterfly, Pararge aegeria

## Purpose and scope
- Examines whether repeat periods of intensive flight during female oviposition affect egg provisioning and reduce offspring performance when larvae develop on drought-stressed host plants.
- Tests potential long-lasting maternal effects that could influence adult offspring dispersal ability from drought-affected areas.
- Context: laboratory experiment using the Speckled Wood butterfly to explore mechanisms linking drought and habitat fragmentation to biodiversity.

## Experimental design
- Maternal flight treatment: two groups—control (no forced flight) and forced flight. Forced flight involved 5 minutes of flight, repeated on days 1, 4, and 8 of oviposition.
- Source population: outbred laboratory stock from St. Hubert, Belgium.
- Reproductive output data: number of days from adult eclosion to death (longevity), daily and lifetime egg counts, and total lifetime egg hatch success.
- Embryonic development data: eggs photographed for size measurements on days 2, 4, 6, 8, and 10; hatching success tracked; embryonic development time recorded.
- Offspring performance data: one larva per female per day of oviposition reared on drought-stressed host plant; measures include development time to pupation, pupal mass, survival to eclose, adult mass, thorax mass, and inferred flight muscle mass.

## Data files and key variables

- Female_reproductive_output_data.csv
  - FemaleID: unique female identifier
  - FemaleMass_mg: adult mass at eclosion
  - MaternalFlight: treatment (C = control, F = forced flight)
  - LifetimeFecundity: total eggs laid in life
  - Longevity: days from eclosion to death
  - LifetimeEggHatch: proportion of eggs hatched across life
  - MeanEggSize: average egg size across life

- Embryonic_development_data.csv
  - OffspringID: unique offspring identifier
  - EggSize: size of egg on day laid
  - DayLaid: oviposition day of the egg
  - EmbryonicTime: days from egg laid to hatching
  - Hatch: whether larva hatched (y/n)
  - MotherID: mother identifier
  - MaternalFlight: treatment (C or F)
  - MaternalLongevity: mother’s days alive post-eclosion
  - MaternalMass_mg: mother’s mass at eclosion
  - (Note: some data may be missing if the egg/larva did not hatch)

- Offspring_performance_data.csv
  - OffspringID: unique offspring identifier
  - DryAdultMass_mg: total dry body mass at adulthood
  - DryThoraxMass_mg: dry thorax mass (flight-related musculature)
  - EggSize: egg size from which the offspring hatched
  - DayLaid: oviposition day of the egg
  - PupalMass_mg: mass of the pupa
  - TotalDevTime: development time from hatching to adult eclosion
  - Sex: offspring sex (F = female, M = male)
  - MotherID: mother identifier
  - MaternalFlight: treatment (C or F)
  - SurviveToEclose: whether offspring survived to eclose (y/n)

- N.B.: Empty cells indicate missing data (e.g., due to death of the butterfly)

## Data quality and collection notes
- Data collected under standardised laboratory conditions using published methods.
- Manual data entry with quality assurance tools (input masks, input conditions) to ensure data coherence.

## How this dataset can be used
- Investigate maternal effects: influence of forced flight on maternal fecundity, longevity, egg provisioning (egg size), and embryonic development time.
- Assess offspring performance under drought stress: development time, mass metrics, survival rates, and flight-related morphology (thorax and flight muscle indicators).
- Explore cross-generational links: maternal flight treatment (group-level) and offspring outcomes across development stages.
- Analyze potential dispersal-related implications: relationships among maternal flight, offspring body and flight-associated traits, and survival to adulthood.
- Support meta-analyses on how environmental stressors (drought) and life-history trade-offs (flight during oviposition) shape population dynamics.