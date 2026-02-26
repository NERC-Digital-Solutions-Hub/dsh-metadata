# Data on flight-induced maternal effects and offspring performance on drought stressed plants in the Speckled Wood butterfly, Pararge aegeria

- Purpose and scope
  - Dataset from a laboratory experiment testing whether repeat periods of intensive flight during female oviposition affect egg provisioning and offspring performance on drought-stressed host plants.
  - Tests potential long-lasting maternal effects that could influence adult offspring dispersal out of drought-stricken areas.
  - Overall aim: explore mechanisms by which drought and habitat fragmentation impact biodiversity.

- Experimental design (overview)
  - Maternal flight treatment: females assigned to control (no forced flight) or forced flight; 5 minutes of flight on days 1, 4, and 8 of oviposition.
  - Maternal reproductive output: monitor longevity (days from adult eclosion to death), daily egg counts, total lifetime fecundity, and lifetime egg hatch proportion.
  - Embryonic development: on days 2, 4, 6, 8, 10 of oviposition, photograph 5 eggs per female for size measurements; track hatch success and embryonic development time.
  - Offspring performance on drought-stressed hosts: one larva per female per day of oviposition reared on drought-stressed plants; record development time to pupation, pupal mass, survival to eclose, adult sex, and post-emergence masses (dry body and dry thorax) to index flight muscle investment.
  - Organism source: outbred laboratory stock from St. Hubert, Belgium.

- Datasets included
  - Female_reproductive_output_data.csv
    - Key fields: FemaleID, FemaleMass_mg, MaternalFlight (C or F), LifetimeFecundity, Longevity, LifetimeEggHatch, MeanEggSize
  - Embryonic_development_data.csv
    - Key fields: OffspringID, EggSize, DayLaid, EmbryonicTime, Hatch (y/n), MotherID, MaternalFlight, MaternalLongevity, MaternalMass_mg
  - Offspring_performance_data.csv
    - Key fields: OffspringID, DryAdultMass_mg, DryThoraxMass_mg, EggSize, DayLaid, PupalMass_mg, TotalDevTime, Sex, MotherID, MaternalFlight, SurviveToEclose (y/n)

- Data fields and units
  - Mass and size: mg (adult mass, thorax mass, pupal mass), mm^2 (egg size)
  - Time: days (longevity, embryonic time, total developmental time)
  - Categorical: MaternalFlight (C = no flight, F = forced flight), Hatch (y/n), Sex (F/M), SurviveToEclose (y/n)

- Data quality and provenance
  - Data collected under standardised laboratory conditions using published methods.
  - Manual data entry with quality assurance tools (input masks, input conditions) to ensure coherence.
  - Documentation includes clear variable definitions and descriptions to support reuse.

- Data completeness and notes
  - N.B. empty cells indicate missing data (e.g., due to death of the butterfly).

- Governance and reuse considerations
  - Aligns with data stewardship goals: well-structured, cross-referenced datasets enabling discovery, reuse, and meta-analyses.
  - Metadata provides explicit linkages from maternal treatment to offspring outcomes, supporting provenance tracking.
  - Considerations for sharing include potential data availability constraints (e.g., embargoes or sharing restrictions) and the need for consistent formats and complete metadata.

- Recommendations for data stewardship
  - Provide a machine-readable data dictionary and a data license to clarify reuse terms.
  - Assign persistent identifiers to mothers and offspring to strengthen traceability.
  - Offer a consolidated data dictionary that maps field names to units, descriptions, and measurement methods.
  - Consider publishing alongside analysis code or scripts to enhance reproducibility.
  - Plan for versioning and update procedures if data are expanded or corrected.