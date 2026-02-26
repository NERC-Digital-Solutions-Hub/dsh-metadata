# Supporting documentation for bird ringing data

- Location and timing: Wytham woods, Oxfordshire, UK; collected in 2020 and 2021 as part of a long-term monitoring project on breeding biology and behaviour of birds.
- Purpose: Support population monitoring and study of breeding biology; data collected to enable analyses of individuals over time, including immigrants to the population.
- Data collection window: April–June for nest trapping and ringing; additional ringing in autumn and winter.

## Data collection and scope

- Procedures:
  - Unringed breeding pairs trapped at the nest and fitted with a BTO metal leg ring.
  - Great tits and blue tits additionally fitted with a plastic PIT tag (RFID).
  - All nestlings tagged at 2 weeks old.
  - Additional trapping across the woodland outside primary breeding season.
  - Immigrants to the population also tagged.
  - Birds trapped using mist nets; biometrics collected (mass, wing length, tarsus length, fat score, bill length).
  - Birds released after processing.
- Data handling:
  - Data entered into the internal Edward Grey Institute Bird Data Management Project (EBMP).
  - Underwent quality checks (e.g., identifying erroneous nestbox identities).
  - Primary data entry performed by named individuals (Keith McMahon, Sam Crofts) with involvement from additional field workers.

## Data structure and metadata

- Dataset format: One CSV file named Ringing_data.
- Contents: 23 columns detailing each ringing event or observation.
- Key fields and concepts:
  - Record.type: physical (bird held) vs. diurnal (identified without capture).
  - Retrap: whether the record is a new capture or retrapped bird.
  - Bto.ring: BTO ring number.
  - Pit.tag: alphanumeric PIT tag or blank if none.
  - Pit.tag.state: status codes (0 none, 1 new, 2 present but not scanned, 3 present and scanned, 4 replaced, 5 removed and not replaced, 6 faulty tag removed and replaced).
  - Bto.species.code: species code (reference PDF available).
  - Age, Sex, Sexing method: coded per defined references.
  - Date.time: date and time of capture.
  - Location: capture location (e.g., nestbox identifiers and woodland locations).
  - Morphometrics: Wing.length (mm), Weight (g), Bill.length (mm), Bill.depth (mm), Tarsus.length (mm with method), etc.
  - Bill.length.method, Bill.depth.method, Tarsus.length.method: measurement methods (e.g., skull, feathers, nostril; deepness; max/min).
  - Pox: pox status (NA, FALSE, TRUE).
  - Leg.condition.description, Tick.description: qualitative notes.
  - Comments: additional remarks.
- Coding references:
  - Species codes link to external BTO resource.
  - Age codes link to external age-code resources.
- Data quality features:
  - Explicit metadata for each field (column meanings, coding schemes) to aid reuse and interoperability.
  - Fields allow NA where information is unknown or not collected.

## Data management and quality assurance

- Data management system: EBMP (internal data management application).
- Quality assurance:
  - Routine checks to identify outliers and data inconsistencies (e.g., nestbox identity issues).
  - Data entry performed by named personnel with supervision and review.
- Data provenance:
  - Records tied to specific field activities, dates, and operators.
  - Clear lineage from field collection to internal data management.

## Key variables, codes, and measurements

- Physical capture status: Record.type (physical vs diurnal) and Retrap status.
- Individual identifiers: Bto.ring (BTO ring), Pit.tag (PIT tag) and state.
- Biological data: Species code, Age, Sex, Sexing method.
- Location and timing: Date.time, Location.
- Morphometrics: Wing.length, Bill.length, Bill.depth, Tarsus.length, Weight, Bill.length.method, Bill.depth.method, Tarsus.length.method.
- health/condition notes: Pox, Leg.condition.description, Tick.description.
- Data completeness: Some fields may be NA; reliance on external code references for standardization.

## Data provenance and accessibility

- Primary data source: Field operations in Wytham Woods, 2020–2021.
- Documentation purpose: Provide structured metadata and column-level definitions to facilitate reuse and transparency.
- Accessibility note: Data are stored in an internal system (EBMP); sharing and external reuse would require alignment with governance and metadata standards outlined in the documentation.

## Relevance to monitoring frameworks and stakeholder considerations

- Supports building monitoring frameworks by:
  - Defining standardized data structures and coding schemes for long-term population monitoring.
  - Documenting data collection methods, provenance, and quality checks to ensure traceability and reproducibility.
  - Highlighting the need for clear metadata to interpret complex datasets (e.g., PIT-tag statuses, morphometrics, and location codes).
  - Providing a model for integrating field data collection with governance practices and data management workflows.
- Practical insights for framework authors:
  - Emphasizes the importance of metadata completeness, external code references, and transparent data processing pipelines.
  - Demonstrates how to handle data quality issues and maintain data provenance across long-term monitoring efforts.
  - Illustrates potential data-sharing considerations arising from internal data management systems and tagging metadata.