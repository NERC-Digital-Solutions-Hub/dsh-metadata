# Collection/generation methods

## Study scope and gradient
- Monitoring an approximately 35 kilometre urban–non-urban gradient in Scotland, from Glasgow city centre to Loch Lomond National Park.
- Monitoring occurred annually from 2014 to 2022.
- Data collected across 5 to 20 sites per year, with nestboxes installed at each site (numbers per site range from 5 to 161 depending on site size/year).

## Nestbox deployment and occupancy
- Nestboxes: Woodcrete (Schwegler, Germany), dimensions 26 H x 17 W x 18 D cm, entrance hole diameter 32 mm.
- Boxes installed ~50 metres apart at all sites.
- Site-level occupancy recorded (occupied vs. unoccupied).

## Breeding monitoring protocol
- Breeding season: April–June.
- Nestboxes checked weekly during nest-building and incubation.
- First egg date recorded when observed or back-calculated if observed during laying.
- Clutch size: maximum number of eggs observed during incubation.
- 14 days after incubation began: nestboxes checked every other day until chicks observed.
- 13 days after hatching: chicks marked with a unique metal ring.
- Final check occurs ≥20 days after hatching; dead chicks recorded and subtracted to yield the number of chicks that fledged.

## Data structure and recording
- Data entries: each row represents an individual breeding event; columns capture event-specific details.
- Key fields include:
  - ID, DATA_ENTRY_ID, YEAR (YYYY)
  - NESTBOX_NUMBER, SITE, OCCUPIED
  - REPLACEMENT_CLUTCH, SPECIES (five-letter BTO codes)
  - FIRST_EGG_DATE, LAYING_COMPLETE
  - CLUTCH_SIZE, CLUTCH_COMPLETE
  - EXPECTED_HATCH, OBSERVED_HATCH, HATCH_DEVIATION
  - MALE_CAUGHT, FEMALE_CAUGHT
  - HATCHLINGS, UNHATCHED_EGGS, FLEDGLINGS
  - SUCCESS, MALE_RING, FEMALE_RING
  - NOTES

## Metadata and species coding
- Table 1 provides five-letter BTO species codes and mappings to common names; examples include:
  - BLUTI = blue tit (Cyanistes caeruleus)
  - GRETI = great tit (Parus major)
  - HOUSP = house sparrow (Passer domesticus)
  - NUTHA = nuthatch (Sitta europaea)
  - PIEFL = pied flycatcher (Ficedula hypoleuca)
  - TRESP = tree sparrow (Passer montanus)

## Data quality control
- Year-end quality checks performed and data uploaded to a central database.

## Potential analyses and uses
- Assess phenology, breeding success, and clutch dynamics across sites and years.
- Examine correlations between site characteristics, urbanization gradient, and reproductive metrics (e.g., clutch size, hatch rates, fledging success).
- Develop predictive models linking nestbox occupancy, dates, and ring-recapture data to survival and fledging outcomes.

## Considerations for analysts
- Data at the level of individual breeding events enables granular analyses but requires careful handling of repeated measures across years and sites.
- Variables include temporal (dates, day counts) and event-level data (per nestbox and per breeding attempt); standardization and quality checks are essential for combining datasets across years and sites.