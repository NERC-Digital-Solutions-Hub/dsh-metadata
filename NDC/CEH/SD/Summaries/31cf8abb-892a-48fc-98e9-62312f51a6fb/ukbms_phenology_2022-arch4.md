## About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with thanks to volunteers.
- Purpose: provide annual population status data for butterflies to inform biodiversity policy and research.
- Sampling framework:
  - Standard butterfly transects (Pollard walks): fixed routes, weekly counts, 2–4 km, 26 counts/year at many sites.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares, 2–3 visits/year.
  - Targeted surveys: single-species transects and alternative methods (timed counts, egg/larval counts).
- Scope: active at >3000 sites annually, data from all methods analyzed together; ongoing since 1976.

## Nature of data collected

- Focus: phenology – timing of adult butterfly flight periods on UKBMS transects.
- Metrics:
  - Simple: first/last recording dates, peak date, peak count, and flight period length (days between first and last observation).
  - Alternative metrics: mean flight date (weighted), and flight period standard deviation (SD) to assess synchronisation.
- Generational handling:
  - Multivoltine species: data can be split into first and second flight periods where possible.
  - Univoltine species (e.g., Brimstone, Peacock): two distinct flight periods may be possible due to overwintering emergence.
  - For some species, generations overlap and separation is not always feasible.
- Limitations: incomplete weekly coverage can affect accuracy; for many species only the entire flight season data may be available.

## Quality control

- Data workflow: field recording on standard forms, online entry via UKBMS data site or Transect Walker, then central data storage.
- Validation:
  - Automatic checks for data entry errors (e.g., unusually high counts, records outside flight period).
  - Regional transect coordinators review entries and perform ongoing checks.
  - Automated and manual validation processes flag records outside known distribution, out of flight period, first-time site records, or anomalous abundances.
- Corrections: data queries and coordination with coordinators/recorders to edit the main UKBMS dataset as needed.

## Details of this data download

- Content: phenology data for all species at all sites and years with sufficient data.
- Format: comma-separated values (.csv).
- Brood handling: data available for the entire flight period for most species; 13 species have separate first/second flight period data where possible.
- Columns available:
  - SITENO, SITENAME, GRIDREF, SPECIES_NAME, COMMON_NAME, YEAR
  - NUMBER_OF_BROODS, BROOD
  - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT
  - MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE
- Taxonomy references: standardized checklists (Agassiz et al. 2013, 2019, 2020).

## Licence and attribution statement

- Licence: Open Government Licence (OGL) for free use and reuse with conditions.
- Citation: include the dataset citation and DOI in any publications describing analyses.
- Attribution: Contains UKBMS data © Butterfly Conservation, CEH, BTO, JNCC.

## Offer of collaboration and contact details

- UKBMS partners offer advisory support and help interpreting outputs.
- Co-authorship and intellectual input into publications are possible.
- Contacts:
  - UK Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)
  - Butterfly Conservation: Transect co-ordinator (transect@butterfly-conservation.org)