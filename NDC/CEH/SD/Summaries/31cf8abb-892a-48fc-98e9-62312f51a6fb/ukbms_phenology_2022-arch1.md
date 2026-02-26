# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (UKEHL), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC). Volunteers contribute data, forming a long-running, site-based monitoring program since 1976 with over 3,000 actively recorded sites per year.
- Purpose: provide annual data on butterfly population status and support policy questions related to biodiversity status and trends.

## Data collection methods and sampling framework

- Standard butterfly transects (Pollard walks): fixed-route transects at a site; 2–4 km long; 5 m wide transect band; weekly counts from early April to late September (ideally 26 counts/year); typically 45 minutes to 2 hours per walk; more than 2,000 sites monitored yearly as of 2022.
- Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects; 2–3 visits per year (minimum two in July/August); around 800 squares sampled annually to cover common habitats like farmland.
- Targeted surveys: single-species transects and alternative methods such as timed counts and egg/larval web counts focused on specific species.
- All sampling data from these methods are analyzed together to assess population changes.

## Nature of the data collected

- Phenology focus: timing of adult butterfly flight periods recorded on UKBMS transects.
- Data availability for phenology is strongest for standard transects with weekly counts; WCBS data do not support robust phenology metrics due to reduced sampling frequency.
- Phenology metrics include:
  - First/last recording dates per species per site per year per brood
  - Peak date and peak count
  - Mean flight date (weighted mean) and the standard deviation (SD) around this date to reflect synchronisation and flight period length
  - Flight period range (days between first and last observation)
- For species with multiple generations (multivoltine) or with unique life histories (univoltine, overwintering adults), the data may be split into separate flight periods (first and second) where feasible. For some species, complete separation into multiple generations is not possible due to overlap.

## Quality control and data validation

- Field data are recorded on standard forms and entered online (via UKBMS MyData) or via Transect Walker software.
- Automated checks flag implausible entries (e.g., unusually high counts, records outside known flight periods).
- Regional transect coordinators perform ongoing quality checks, with further automated/manual validations to identify records outside known distributions, out-of-season records, first-time site records, and anomalous abundances.
- Corrections are made through queries and consultations with coordinators or recorders, ensuring data integrity before updating the main UKBMS dataset.

## Details of this data download

- This download provides phenology data for all species across all sites and years with sufficient data, in CSV format.
- For thirteen species, data are available for the entire flight period and separately for two distinct flight periods within each year; for all other species, data are available for the entire flight season only.
- Key columns:
  - SITENO, SITENAME, GRIDREF: site identifiers and location details
  - SPECIES_NAME, COMMON_NAME: scientific and common names
  - YEAR, NUMBER_OF_BROODS, BROOD: year and flight-period breakdown (0 = entire flight period; 1 = first brood; 2 = second brood)
  - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT: timing and magnitude of first/last/peak observations
  - MEAN_FLIGHT_DATE: weighted mean day of year for records within a brood
  - FLIGHTPERIOD_SD: variability around the mean flight date
  - FLIGHTPERIOD_RANGE: duration of the flight period (days between first and last records)

## Licence and attribution

- Data are provided under an Open Government Licence (OGL), permitting free use with minimal conditions.
- When citing, include the Digital Object Identifier (DOI) as provided in the metadata record.
- Attribution: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, CEH, BTO, and JNCC.

## Collaboration and contact details

- UKBMS partners offer guidance on dataset use and interpretation, and may contribute co-authorship or intellectual input to publications resulting from UKBMS data.
- Contacts:
  - UK Centre for Ecology & Hydrology: Marc Botham (ukbms@ceh.ac.uk)
  - Butterfly Conservation: Transect co-ordinator (transect@butterfly-conservation.org)