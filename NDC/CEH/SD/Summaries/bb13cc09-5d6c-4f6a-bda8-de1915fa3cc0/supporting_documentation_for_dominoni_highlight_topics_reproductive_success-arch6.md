# Collection/generation methods

## Study design and setting
- Longitudinal field data collection monitoring an approximately 35 km urban–non-urban gradient in Scotland, from Glasgow city centre to Loch Lomond National Park.
- Monitoring period: annually from 2014 to 2022.
- Sites: between 5 and 20 sites per year.
- Nestboxes: Woodcrete boxes (Schwegler, Germany; 26 H x 17 W x 18 D cm; entrance hole 32 mm) installed at all sites, roughly 50 m apart; 5 to 161 nestboxes per site depending on size/year.

## Data collection procedures
- Breeding season monitoring: April–June, with weekly checks during nest-building and incubation.
- Data captured per occupied nestbox (blue tits and great tits): first egg date (directly observed or back-calculated), clutch size (maximum observed during incubation).
- Post-incubation monitoring: 14 days after incubation starts, nestboxes checked every other day until chicks observed.
- Ringing: 13 days after hatching, chicks ringed with unique metal rings.
- Disturbance control: nests not checked again until at least 20 days after hatching to avoid premature fledging.

## Data structure and content
- Rows: individual breeding events.
- Columns: details of each event, including site, nestbox, occupancy, clutch and hatch data, and outcomes.
- Nature and units: described in a metadata table appended to the file.
- Data entry and quality control: each year’s data are quality checked and uploaded to a central database.

## Key variables and metadata (examples)
- IDENTIFIERS: ID (unique record number), DATA_ENTRY_ID (initials of data entrant/checker), YR (year, yyyy).
- LOCATION: SITE, NESTBOX_NUMBER, OCCUPIED (1 = yes, 0 = no).
- BREEDING EVENT DETAILS: REPLACEMENT_CLUTCH (code for breeding attempts), SPECIES (5-letter BTO code), FIRST_EGG_DATE, LAYING_COMPLETE, CLUTCH_SIZE, CLUTCH_COMPLETE, EXPECTED_HATCH, OBSERVED_HATCH, HATCH_DEVIATION.
- OUTCOMES: HATCHLINGS, UNHATCHED_EGGS, FLEDGLINGS, SUCCESS (1 = at least one fledged, 0 = none, 2 = unknown).
- CONTACTS AND NOTES: MALE_CAUGHT, FEMALE_CAUGHT, MALE_RING, FEMALE_RING, NOTES (free text).
- DATA MANAGEMENT: metadata describes units and data types; data entries rely on a central database.

## Species coverage and codes
- BTO five-letter codes and common names:
  - BLUTI = blue tit (Cyanistes caeruleus)
  - GRETI = great tit (Parus major)
  - HOUSP = house sparrow (Passer domesticus)
  - NUTHA = nuthatch (Sitta europaea)
  - PIEFL = pied flycatcher (Ficedula hypoleuca)
  - TRESP = tree sparrow (Passer montanus)

## Practical implications for data use
- Enables analysis of breeding success, hatch timing, and fledging outcomes across multiple sites and years.
- Supports self-service data exploration via structured breeding event records and derived metrics (e.g., fledging success, hatch deviation).
- Facilitates data quality improvements and potential sharing or re-use through standardized metadata and centralized storage.