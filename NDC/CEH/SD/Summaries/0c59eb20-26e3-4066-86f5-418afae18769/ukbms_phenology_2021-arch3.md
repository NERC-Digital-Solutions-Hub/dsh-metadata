# About the UK Butterfly Monitoring Scheme

- Purpose and use: The UK Butterfly Monitoring Scheme (UKBMS) provides annual population status data for butterflies to support understanding of insect population changes and to answer policy questions related to biodiversity status and trends.
- Organization and funding: Coordinated and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (CEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC). Volunteers are essential contributors.
- Time frame and scope: In operation since 1976, with data from over 2,500 active sites annually. Data from all sampling methods are analyzed together to produce a comprehensive resource.

## How data are collected (sampling framework)

- Standard butterfly transects (Pollard walks): Fixed-route 2–4 km transects, recorded weekly (up to 26 visits/year) across habitat units; typically 5 m wide, from early April to late September, at nearly 2,000 sites.
- Wider Countryside Butterfly Survey (WCBS): Stratified-random 1 km squares; two parallel 1 km transects per site with 2–3 visits per year (plus encouraged spring visits), sampling around 800 squares/year to cover common habitats like farmland.
- Targeted surveys: Single-species transects and alternative methods (timed counts, egg/larval web counts) focused on particular species or life stages.

## Nature of data collected (phenology and metrics)

- Phenology focus: Timing of adult butterfly flight periods across transects; measures reflect when species first appear, peak activity, and the duration of flight periods.
- Primary phenology metrics (from standard transects):
  - First and last observation dates per site per year
  - Peak date and peak count
  - Flight period length (days between first and last observation)
- Alternative metrics to address sampling variability:
  - Mean flight date (weighted mean date of counts)
  - Flight period standard deviation (SD) as a measure of synchronisation/length
- Generation structure considerations:
  - For multivoltine species, two distinct flight periods may be reported where separable
  - For uni-voltine species (e.g., Brimstone, Peacock), first and second flight periods may be reported to reflect overwintering emergence and summer emergence
  - For some species, data are reported for the entire flight period when separation is not feasible
- Data limitations: Separation of generations depends on species biology and data quality; overlapping generations can constrain clear partitioning.

## Quality control

- Field data capture: Recorded on standard forms; entered online via UKBMS data entry site or Transect Walker before being stored in a central database.
- Automated checks: Immediate validation for unlikely counts or records outside known flight periods.
- Regional validation: Regional transect coordinators review data for questionable records; continuous checks during the season.
- Further validation: Automated and manual procedures screen for out-of-range distributions, first-time site records, unusually high counts, or unusual trends; discrepancies are resolved through data queries and, if needed, edits to the main dataset.

## Details of this data download (phenology data)

- Scope: Phenology data for all species across all sites and years with sufficient data; provided as a CSV file.
- Special cases: For 13 species, data are available for the entire flight period and separately for two distinct flight periods per year; for other species, data cover the entire flight season only.
- Columns described:
  - SITENO, SITENAME, GRIDREF
  - SPECIES_NAME (binomial), COMMON_NAME
  - YEAR, NUMBER_OF_BROODS, BROOD
  - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT
  - MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE

## Licence and attribution

- Licence: Open Government Licence (OGL) for open use and reuse; citation with DOI required in any publications using the data.
- Attribution: Include the statement “Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, JNCC” in outputs.

## Offer of collaboration and contact details

- Collaboration: UKBMS partners offer advisory support and can contribute intellectual input or co-authorship for publications, conference presentations, or posters arising from UKBMS data.
- Contact information:
  - UK Centre for Ecology & Hydrology: Marc Botham, ukbms@ceh.ac.uk
  - Butterfly Conservation (Transect co-ordinator): transect@butterfly-conservation.org