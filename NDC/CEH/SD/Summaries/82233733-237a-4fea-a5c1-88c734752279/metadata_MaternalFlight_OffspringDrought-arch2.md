# Data on flight-induced maternal effects and offspring performance on drought stressed plants in the Speckled Wood butterfly, Pararge aegeria

- A laboratory dataset testing whether repeat periods of intensive flight during female oviposition affect egg provisioning and offspring performance when larvae develop on drought-stressed host plants, and whether these maternal effects persist to influence adult offspring dispersal potential from drought-impacted areas.
- Aims to explore mechanisms by which drought and habitat fragmentation influence biodiversity.

## Experimental design and collection methods

- Maternal flight treatment
  - Two groups derived from an outbred lab stock from St. Hubert, Belgium: control (no forced flight) and forced flight.
  - Forced flight: butterflies stimulated to fly for 5 minutes per session with flight periods on days 1, 4, and 8 of oviposition.
- Maternal reproductive output
  - Life-long metrics: longevity (days from adult eclosion to death), lifetime fecundity (total eggs laid), and lifetime egg hatch proportion.
  - Eggs collected daily; egg hatching monitored.
- Embryonic development
  - Five eggs per female laid on days 2, 4, 6, 8, 10 were photographed for size; all eggs monitored for hatching; embryonic development time recorded when hatched.
- Offspring performance on drought-stressed host plants
  - On hatching day, one larva per female per oviposition day reared on drought-stressed plants.
  - Drought stress: water withheld 20 days prior to hatching; minimal watering thereafter.
  - Measured: development time from hatching to pupation, pupal mass, survival to eclose; at eclosion, sex, body mass, thorax mass (flight muscle), and used flight muscle mass as proxy for flight ability.
- Overall aim: understand how maternal flight-induced effects relate to offspring viability and potential dispersal under drought conditions.

## Data files and key variables

- Female_reproductive_output_data.csv
  - FemaleID; FemaleMass_mg; MaternalFlight (C = control, F = forced); LifetimeFecundity; Longevity; LifetimeEggHatch; MeanEggSize
- Embryonic_development_data.csv
  - OffspringID; EggSize; DayLaid; EmbryonicTime; Hatch (y/n); MotherID; MaternalFlight; MaternalLongevity; MaternalMass_mg
- Offspring_performance_data.csv
  - OffspringID; DryAdultMass_mg; DryThoraxMass_mg; EggSize; DayLaid; PupalMass_mg; TotalDevTime; Sex (F/M); MotherID; MaternalFlight; SurviveToEclose (y/n)

Notes:
- Missing data are indicated by empty cells (e.g., due to mortality).
- Each offspring’s development and size metrics provide a link between maternal treatment, embryonic development, and adult flight-related performance.

## Quality control and data provenance

- Data collected under standardised laboratory conditions using published methods.
- Data entry performed manually with quality assurance tools (input masks, conditions) to ensure coherence.
- Clear linkage across datasets via identifiers (FemaleID, MotherID, OffspringID) to enable integrated analyses.

## Relevance for environmental monitoring and analysis

- Enables assessment of how repeated maternal flight behavior and drought stress interact to influence reproductive output, development rates, and adult dispersal potential—key components in understanding biodiversity responses to habitat fragmentation and climate-induced drought.
- Provides standardized, comparable metrics (fecundity, hatch success, embryonic timing, growth, and flight-related traits) for longitudinal environmental health monitoring and policy performance evaluations.
- Facilitates data integration with other environmental datasets to enhance value beyond a single study and supports open data access for broader scrutiny and reuse.