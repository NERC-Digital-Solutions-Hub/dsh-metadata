# Collection/generation methods

- A long-term, gradient-based field study in Scotland (approximately 35 km from Glasgow city centre to Loch Lomond National Park) monitored annually from 2014 to 2022.
- Conducted across 5 to 20 sites per year, with nestboxes installed at all sites (50 metres apart); number of boxes per site ranged from 5 to 161 depending on site size and year.
- Focused on blue tits and great tits; other species recorded per the metadata table and species code table.

## Study design and field methods

- Nestboxes: Woodcrete boxes (dimensions 26 H x 17 W x 18 D cm; entrance hole 32 mm) installed at each site.
- Breeding-season monitoring: Weekly checks during nest-building and incubation (April–June).
- Key dates and measurements:
  - First egg date either observed directly in the field or back-calculated if observed mid-laying (assume one egg per day).
  - Clutch size recorded as the maximum observed during incubation.
  - Incubation began after clutch completion; nestboxes checked every other day from day 14 after incubation commenced until chicks observed.
  - Chicks marked with unique metal rings at 13 days post-hatching.
  - Final check conducted at least 20 days after hatching to record any remaining dead chicks and determine fledging success.
- Nesting outcomes:
  - Fledging determined by subtracting dead chicks from the total number fledged by day 13.
  - Data recorded per breeding event; no cross-year aggregation noted in the method description.

## Data collection protocol and data content

- Data structure: Each row represents an individual breeding event; columns contain event-specific details.
- Metadata and data fields (as described in the appended metadata table):
  - IDs: unique record number (ID), data entry initials (DATA_ENTRY_ID).
  - Year and site: YR, SITE; nestbox identifier (NESTBOX_NUMBER).
  - Occupancy and breeding details: OCCUPIED, REPLACEMENT_CLUTCH, SPECIES.
  - Phenology and clutch data: FIRST_EGG_DATE, LAYING_COMPLETE, CLUTCH_SIZE, CLUTCH_COMPLETE.
  - Hatch data: EXPECTED_HATCH, OBSERVED_HATCH, HATCH_DEVIATION, HATCHLINGS, UNHATCHED_EGGS, FLEDGLINGS, SUCCESS.
  - Observer information and notes: MALE_CAUGHT, FEMALE_CAUGHT, MALE_RING, FEMALE_RING, NOTES.
- Species coding: Five-letter BTO codes are used (e.g., BLUTI for blue tit, GRETI for great tit) with scientific and common names provided in a separate table.
- Notes: Free-text field for important notes about the breeding attempt, data extraction, or samples.

## Data quality control and management

- Year-end data quality check: Data collected within the year is verified and uploaded to a central database.
- Data structure and governance: Clear separation between individual breeding events and their associated metadata; data are organized to support transformation, analysis, and reporting.

## Species codes (Table 1)

- BLUTI: Cyanistes caeruleus (blue tit)
- GRETI: Parus major (great tit)
- HOUSP: Passer domesticus (house sparrow)
- NUTHA: Sitta europaea (nuthatch)
- PIEFL: Ficedula hypoleuca (pied flycatcher)
- TRESP: Passer montanus (tree sparrow)