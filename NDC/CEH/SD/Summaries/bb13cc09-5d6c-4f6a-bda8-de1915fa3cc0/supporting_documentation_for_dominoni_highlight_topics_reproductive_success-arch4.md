# Collection/generation methods

- Scope and design
  - Monitoring a ~35 km urban–non-urban gradient from Glasgow city centre to Loch Lomond National Park, Scotland.
  - Annual monitoring from 2014 to 2022, across 5–20 sites per year.

- Nestboxes and site deployment
  - Nestboxes installed at all sites (Woodcrete, Schwegler, 26 cm high × 17 cm wide × 18 cm deep; entrance hole 32 mm).
  - Approximately 50 m spacing between nestboxes; 5–161 nestboxes per site depending on year and site size.

- Field protocol and timing
  - Breeding season monitoring: April–June; weekly checks during nest-building and incubation.
  - First egg date recorded directly or back-calculated if observed during laying; assumed one egg per day.
  - Clutch size recorded as maximum observed during incubation.
  - 14 days after incubation starts: nestboxes checked every other day until chicks observed.
  - 13 days after hatching: chicks ringed with unique metal rings.
  - Final check at ≥20 days after hatching to record any dead chicks and compute fledging success.

- Data captured and structure
  - Data collected per breeding event; data structure comprises rows for events and columns for event details.

- Quality control
  - End-of-year data checks and upload to a central database.

- Metadata and data structure specifics
  - Metadata fields include: ID, DATA_ENTRY_ID, YR, NESTBOX_NUMBER, SITE, OCCUPIED, REPLACEMENT_CLUTCH, SPECIES, FIRST_EGG_DATE, LAYING_COMPLETE, CLUTCH_SIZE, CLUTCH_COMPLETE, EXPECTED_HATCH, OBSERVED_HATCH, HATCH_DEVIATION, MALE_CAUGHT, FEMALE_CAUGHT, HATCHLINGS, UNHATCHED_EGGS, FLEDGLINGS, SUCCESS, MALE_RING, FEMALE_RING, NOTES.
  - DESCRIPTION: Table 1 provides five-letter BTO species codes for recorded species.

- Table 1: species codes and mappings
  - BLUTI: Cyanistes caeruleus (blue tit)
  - GRETI: Parus major (great tit)
  - HOUSP: Passer domesticus (house sparrow)
  - NUTHA: Sitta europaea (nuthatch)
  - PIEFL: Ficedula hypoleuca (pied flycatcher)
  - TRESP: Passer montanus (tree sparrow)

- Data management implications for data leaders
  - Long-term, site-based, longitudinal data with standardized event-level records.
  - Centralized quality control and yearly data integration into a central repository.
  - Structured metadata and coded species identifiers to support interoperability and reuse.