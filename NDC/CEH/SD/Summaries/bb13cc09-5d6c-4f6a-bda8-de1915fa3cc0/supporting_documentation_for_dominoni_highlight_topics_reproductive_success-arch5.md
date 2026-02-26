# Collection/generation methods: Monitoring of an urban-non-urban gradient using nestbox data (Scotland, 2014-2022)

## Overview
- A longitudinal study monitoring an approximately 35 km urban–non-urban gradient from Glasgow city centre to Loch Lomond National Park, Scotland.
- Annual monitoring from 2014 to 2022, with 5–20 sites per year.
- Nestboxes installed at all sites, spaced ~50 meters apart; number of boxes per site ranged from 5 to 161 depending on site size and year.
- Target species include blue tit (BLUTI) and great tit (GRETI); other small passerines noted in metadata.

## Collection/Generation Protocol
- Breeding-season monitoring conducted weekly from April to June.
- For occupied nestboxes, first egg date was observed or back-calculated if detected during laying but before incubation.
- Clutch size recorded at incubation; 14 days after incubation began, boxes checked every other day until chicks were observed.
- Chicks ringed uniquely at 13 days post-hatching; final checks conducted after 20+ days to determine fledging success.
- Data entries include detailed event-level records per breeding attempt.

## Data Structure and Values
- Rows: individual breeding events; Columns: event-specific details.
- Quality control: at year-end, data are validated and uploaded to a central database.
- Data units and structures are documented in an appended metadata table.

## Metadata and Coding
- Metadata fields include:
  - ID, DATA_ENTRY_ID (initials of data enterer/checker; e.g., CB = Claire Branston), YEAR, NESTBOX_NUMBER, SITE, OCCUPIED, REPLACEMENT_CLUTCH, SPECIES, FIRST_EGG_DATE, LAYING_COMPLETE, CLUTCH_SIZE, CLUTCH_COMPLETE, EXPECTED_HATCH, OBSERVED_HATCH, HATCH_DEVIATION, MALE_CAUGHT, FEMALE_CAUGHT, HATCHLINGS, UNHATCHED_EGGS, FLEDGLINGS, SUCCESS, MALE_RING, FEMALE_RING, NOTES.
- Site options include Balmaha, Scene, Sallochy, Cashel, Dawsholm, Drymen (Forest/Village), Garscube, Kelvingrove, Killearn (Forest/Village), Kilmardinny Loch, Mugdock, Old Station Park, St Mungo Avenue, Strathblane (Forest/Village), Tannoch Burn.
- The metadata table also defines the five-letter BTO species codes and common names (Table 1), including BLUTI (blue tit), GRETI (great tit), HOUSP (house sparrow), NUTHA (nuthatch), PIEFL (pied flycatcher), TRESP (tree sparrow).

## Data Model Details
- SPECIES codes follow standard BTO five-letter codes; descriptions provided in the metadata section.
- Key dates include FIRST_EGG_DATE, LAYING_COMPLETE, EXPECTED_HATCH, and OBSERVED_HATCH.
- Reproductive outcomes captured via CLUTCH_SIZE, CLUTCH_COMPLETE, HATCHLINGS, UNHATCHED_EGGS, FLEDGLINGS, and SUCCESS (fledging success status).

## Data Quality and Curation
- End-of-year data checks precede central upload to a shared database.
- Data structure designed so each row represents a discrete breeding event with comprehensive event-level attributes.
- Notes field available for important contextual information, data extraction caveats, or samples.

## Data Access and Stewardship Considerations
- Centralized storage in a central database facilitates discovery and reuse; explicit data entry initials support traceability.
- Metadata completeness (date fields, site identifiers, species codes) supports interoperability and downstream analyses.
- Consistent coding (e.g., SPECIES, SITE, OCCUPIED, REPLACEMENT_CLUTCH) supports data governance and standardization across years.
- Documentation of units and data definitions is maintained in an appended metadata table to aid interpretation and reuse.

## Key Challenges and Stewardship Implications
- Data completeness and timely data submission across multiple sites and years.
- Maintaining interoperability across varying site scales and potential changes in nestbox numbers or site configurations.
- Ensuring consistent application of metadata standards (e.g., accurate age of chick markings, precise hatch/date calculations, and correct clutch status classifications).
- Handling potential gaps in historical data and ensuring traceability of data entry (DATA_ENTRY_ID) for quality assurance.

## Species Coding Reference (Summary)
- BLUTI: Blue tit (Cyanistes caeruleus)
- GRETI: Great tit (Parus major)
- HOUSP: House sparrow (Passer domesticus)
- NUTHA: Nuthatch (Sitta europaea)
- PIEFL: Pied flycatcher (Ficedula hypoleuca)
- TRESP: Tree sparrow (Passer montanus)