# Data on flight-induced maternal effects and offspring performance on drought stressed plants in the Speckled Wood butterfly, Pararge aegeria

## Overview
- Laboratory dataset examining whether repeat periods of intense flight during female oviposition affect egg provisioning and offspring performance on drought-stressed host plants.
- Tests the potential for flight-induced maternal effects to influence adult offspring dispersal ability from drought-stricken areas.
- Species: Speckled Wood butterfly (Pararge aegeria); origin of stock: outbred laboratory population from St. Hubert, Belgium.
- Outcomes include maternal reproductive output, embryonic development, and offspring performance metrics.

## Experimental design
- Maternal flight treatment:
  - Two groups: control (no forced flight) and forced flight.
  - Forced flight: females stimulated to fly for 5 minutes per session, repeated on days 4 and 8 of oviposition (3 total periods).
  - First oviposition: after the flight treatment, females laid eggs; males removed after the first egg laid.
- Data collection components:
  - Maternal reproductive output: longevity (days from adult eclosion to death), total lifetime eggs laid (fecundity), lifetime egg hatching success.
  - Embryonic development: egg size measurements on days 2, 4, 6, 8, 10 of oviposition; hatching success; embryonic development time (days from laying to hatching).
  - Offspring performance on drought-stressed host plants: one larva per female per day of oviposition (from each day) reared on drought-stressed plants; outcomes include development time to pupation, pupal mass, survival to eclose; post-eclosion measurements include sex and weights (dry body mass, thorax mass) as flight muscle proxies.
- Overall aim: explore mechanisms by which drought and habitat fragmentation influence biodiversity via maternal effects and offspring performance.

## Datasets and variables (3 CSV files)
- Female_reproductive_output_data.csv
  - FemaleID: unique identifier for an individual.
  - FemaleMass_mg: adult mass at eclosion (mg).
  - MaternalFlight: treatment; C = control, F = Forced flight.
  - LifetimeFecundity: total eggs laid over female’s life.
  - Longevity: days from adult eclosion to death.
  - LifetimeEggHatch: proportion of eggs hatched out of total laid.
  - MeanEggSize: mean egg size over life (mm^2).

- Embryonic_development_data.csv
  - OffspringID: unique identifier for an individual (egg/larva lineage).
  - EggSize: size of egg on day laid (mm^2).
  - DayLaid: day of oviposition when egg was laid.
  - EmbryonicTime: days from laying to hatching.
  - Hatch: whether larva hatched (y/n).
  - MotherID: mother’s unique identifier.
  - MaternalFlight: treatment; C = control, F = Forced flight.
  - MaternalLongevity: days mother lived after eclosion.
  - MaternalMass_mg: mother’s mass at eclosion (mg).

- Offspring_performance_data.csv
  - OffspringID: unique identifier for an individual.
  - DryAdultMass_mg: total dry body mass at adulthood (mg).
  - DryThoraxMass_mg: total dry thorax mass (mg).
  - EggSize: size of egg from which the offspring hatched (mm^2).
  - DayLaid: day of oviposition on which the egg was laid.
  - PupalMass_mg: mass of the pupa prior to eclosion (mg).
  - TotalDevTime: development time from egg hatching to adult eclosion (days).
  - Sex: offspring sex; F = female, M = male.
  - MotherID: mother’s unique identifier.
  - MaternalFlight: treatment; C = control, F = Forced flight.
  - SurviveToEclose: whether offspring survived to adult eclose (y/n).

- Note: empty cells indicate missing data (e.g., due to butterfly death).

## Data quality and provenance
- Collected under standardised laboratory conditions using published methods.
- Data entry performed with quality assurance tools (input masks, input conditions) to ensure coherence.
- Explicitly notes missing values as empty cells.

## Potential GIS and data-product considerations
- Although the data are not geospatial (lab-origin stock from Belgium), they can inform GIS-enabled biodiversity analyses when linked with spatially explicit drought data, host-plant distributions, or habitat fragmentation layers.
- Possible map-based visualizations:
  - Temporal plots of reproductive outputs and offspring performance by maternal flight treatment across oviposition days.
  - Spatially-informed risk or impact models by integrating drought severity proxies and landscape connectivity with experimental results at the population or landscape scale.
  - Network-style visualizations of relationships between maternal traits (mass, longevity) and offspring outcomes (development time, mass, survival).

## Limitations and considerations for integration
- Laboratory-derived data from a controlled population may limit direct extrapolation to wild populations.
- Data are organized around individual mothers and their offspring, with multiple measurements per female; explicit nesting or hierarchical structure may be relevant for analyses.
- Missing data should be considered in analyses due to empty cells.
- No direct geospatial coordinates are provided; integration with GIS requires linking to external spatial datasets (drought indices, habitat data, plant distributions).

## Access and completeness
- Three CSV files listed for download:
  - Female_reproductive_output_data.csv
  - Embryonic_development_data.csv
  - Offspring_performance_data.csv
- All described variables and measurements are included as specified in the dataset descriptions.