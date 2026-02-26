# Data on flight-induced maternal effects and offspring performance on drought stressed plants in the Speckled Wood butterfly, Pararge aegeria

## Aim
- Investigate whether repeat periods of intensive flight during female oviposition affect egg provisioning and offspring performance when larvae develop on drought-stressed host plants.
- Test whether flight-induced maternal effects could generate longer-lasting effects influencing adult offspring dispersal traits (proxied by flight muscle mass).

## Experimental design and data collection
- Source population: outbred laboratory stock from St. Hubert, Belgium.
- Maternal flight treatment: control (C) or forced flight (F). Forced flight consisted of 5 minutes of flight, triggered when females alighted, repeated on days 4 and 8 of oviposition (three flight periods total).
- Reproductive output data: eggs collected daily; longevity measured as days from adult eclosion to death; lifetime fecundity as total eggs laid; lifetime egg hatch proportion recorded; mean egg size tracked.
- Embryonic development data: eggs sampled (5 per day on days 2, 4, 6, 8, 10) for size and hatch status; embryonic development time recorded for hatched eggs.
- Offspring performance on drought-stressed hosts: one larva per female per oviposition day reared on a drought-stressed host plant (20 days without water prior to hatching; then water only about every 6 days). Measured development from hatching to pupation, pupal mass, survival to eclose, adult sex, and body masses (dry body mass and dry thorax mass as a proxy for flight ability).

## Datasets and key variables
- 3 CSV files:
  - Female_reproductive_output_data.csv
    - FemaleID, FemaleMass_mg, MaternalFlight (C or F), LifetimeFecundity, Longevity, LifetimeEggHatch, MeanEggSize
  - Embryonic_development_data.csv
    - OffspringID, EggSize, DayLaid, EmbryonicTime, Hatch (y/n), MotherID, MaternalFlight, MaternalLongevity, MaternalMass_mg
  - Offspring_performance_data.csv
    - OffspringID, DryAdultMass_mg, DryThoraxMass_mg, EggSize, DayLaid, PupalMass_mg, TotalDevTime, Sex, MotherID, MaternalFlight, SurviveToEclose (y/n)
- Notes:
  - Empty cells indicate missing data (e.g., death of the butterfly).

## Experimental conditions and measurements
- Standardised laboratory conditions with published methods.
- Drought stress applied to host plants prior to larval development.
- Measurements include life-history traits (fecundity, longevity, hatch rates), embryonic development timing, and offspring performance metrics (development time, masses, survival, sex, and flight-related morphology).

## Quality control and data provenance
- Data collected under standardised procedures.
- Data entry performed with quality assurance tools (input masks, constraints) to ensure coherence.
- Datasets linked via identifiers: FemaleID, MotherID, OffspringID to enable integration across files.

## Potential analyses and uses
- Assess correlations between maternal flight treatment and:
  - reproductive output (fecundity, longevity, hatch success) and egg provisioning (egg size).
  - embryonic development time and hatch success.
  - offspring performance metrics (development time, pupal mass, survival, adult mass, flight muscle proxy) to infer potential impacts on adult dispersal ability.
- Cross-dataset analyses leveraging IDs to study cascading maternal effects from oviposition through to adult dispersal-related traits.
- Modelling potential interactions between maternal treatment and offspring outcomes under drought-stressed conditions.

## Limitations and considerations for interpretation
- Laboratory setting may limit generalisability to natural populations.
- Some data missing by design (e.g., due to mortality); consider missing data mechanisms in analyses.
- Drought treatment is uniform; results reflect one environmental context without field-level variability.