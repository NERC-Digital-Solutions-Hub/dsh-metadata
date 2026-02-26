# About the UK Butterfly Monitoring Scheme

- Purpose: Provides annual data on butterfly population status across the UK to support understanding of insect population changes and biodiversity policy questions.
- Organisers and funders: Butterfly Conservation, UK Centre for Ecology & Hydrology, British Trust for Ornithology, Joint Nature Conservation Committee; significant contribution from volunteers.
- Coverage and history: Active monitoring since 1976 with over 2,500 sites sampled each year; data from all sampling methods are analyzed together.

## Data collection methods

- Standard butterfly transects (Pollard walks): Fixed-route transects (typically 2–4 km) with weekly counts (April–September), across ~2,000 sites.
- Wider Countryside Butterfly Survey (WCBS): Stratified-random 1 km squares with two parallel 1 km transects; 2–3 visits per year, sampling ~750 squares annually.
- Targeted surveys:
  - Single-species transects (focus on specific species during part of the flight period)
  - Alternative methods: timed counts, egg and larval web counts
- Sampling scope: Includes multiple methods to capture both common and targeted species; data are integrated for analysis.

## Nature of the data

- Phenology focus: Timing of adult butterfly flight periods derived from UKBMS transects; metrics account for the variable sampling intensity across sites and years.
- Phenology metrics:
  - Dates of first and last records per site per year
  - Peak date and peak count
  - Mean flight date (weighted mean) and standard deviation (SD) around mean
  - Flight period range (days between first and last records)
- Generation handling:
  - Many species have multiple generations; data can be separated into first and second flight periods for up to 13 species
  - For bivoltine and multivoltine species, separate data where feasible; for some uni-voltine species (e.g., Brimstone, Peacock) two distinct flight periods may be identified
  - For some species, only the entire flight period is provided
- Limitations: Separate-generation phenology is constrained by difficulty in separating overlapping flight periods and incomplete weekly coverage for some sites.

## Quality control

- Field recording: Data collected on standard forms and entered online (UKBMS data entry site) or via Transect Walker software.
- Validation steps:
  - Automatic checks for data entry errors (e.g., anomalously high counts, out-of-season records)
  - Regional transect coordinators review records for questionable entries
  - Additional automated and manual validation to flag out-of-range species, atypical abundances, or records at new sites
- Corrections: Data queries and edits are issued as needed in consultation with coordinators or recorders.

## Details of this data download

- Content: Phenology data for all species across all sites and years with sufficient data; available as CSV (.csv).
- Scope: For 13 species, data are available for the entire flight period and separately for two distinct flight periods per year; for other species, data are for the entire flight season only.
- Column descriptions:
  - SITENO: unique site number within UKBMS
  - SITENAME: site name
  - GRIDREF: OS grid reference for site
  - SPECIES_NAME: scientific name (Fauna Europaea)
  - COMMON_NAME: vernacular name (Emmet & Heath)
  - YEAR: year of metrics
  - NUMBER_OF_BROODS: number of distinct flight periods separated
  - BROOD: flight period (0 = entire; 1 = first; 2 = second)
  - FIRSTDAY: day after 1 April of first record for the brood
  - LASTDAY: day after 1 April of last record for the brood
  - PEAKDAY: day of largest count for the brood
  - PEAKCOUNT: largest count for the brood
  - MEAN_FLIGHT_DATE: weighted mean day after 1 April for the brood
  - FLIGHTPERIOD_SD: standard deviation around mean flight date
  - FLIGHTPERIOD_RANGE: days between firstday and lastday

## Licence and attribution

- Licence: Open Government Licence (OGL) for free use and reuse with few conditions.
- Citation: Include the dataset citation and DOI in references when describing research using the data.
- Attribution statement: Include the text “Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC” with any information or images derived from the data.

## Offer of collaboration and contact details

- Access and interpretation: UKBMS partners are available to advise on dataset details and outputs.
- Collaboration: Opportunities for co-authorship and intellectual input in publications, conferences, or posters using UKBMS data.
- Contacts:
  - UK Centre for Ecology & Hydrology, Marc Botham (ukbms@ceh.ac.uk)
  - Butterfly Conservation, Transect Co-ordinator (transect@butterfly-conservation.org)