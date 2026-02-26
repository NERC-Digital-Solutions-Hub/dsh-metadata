# About the UK Butterfly Monitoring Scheme

- The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee, with active voluntary data contributions from the public.
- Purpose: to provide annual data on butterfly population status from a large-scale, site-based monitoring program; data are used to understand population changes and answer policy questions related to biodiversity status and trends.

- Data collection and sampling framework:
  - Standard butterfly transects (Pollard walks): fixed-route transects at sites chosen by recorders; 2–4 km in length; count all butterflies within a fixed 5 m width; weekly counts from early April to late September (up to 26 counts/year); nearly 2,000 sites currently sampled each year.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares; two parallel 1 km transects subdivided into 10 sections; 2–3 visits per year (minimum two visits in July/August; spring visits encouraged); around 800 squares sampled/year.
  - Targeted surveys: single-species transects or alternative methods (e.g., timed counts, egg/larval web counts) focused on specific species.
- Coverage: UKBMS has monitored butterfly abundance since 1976 and now includes over 2,500 actively recorded sites annually. All sampling methods’ data are analyzed together.

- Nature of data collected (phenology-focused):
  - Phenology refers to timing of life-history events; UKBMS phenology data track adult butterfly flight periods.
  - Available metrics include:
    - First/last recording dates at a site per year and brood
    - Peak date and peak count
    - Mean flight date and standard deviation (SD) to reflect timing and synchronisation
    - Flight period range (days between first and last observation)
  - For species with multiple generations (multivoltine), data may be split into first and second flight periods when separable; for some species with overlapping generations, full-flight-period data are provided. Two univoltine species (Brimstone and Peacock) may have two distinct flight periods (early and summer) plus the entire flight period.
  - Limitations: data accuracy can be affected by incomplete weekly coverage and the April 1–September 30 recording window.

- Quality control:
  - Field data are collected on standard forms and entered online or via Transect Walker; automated checks flag unusual values or out-of-season records.
  - Regional transect coordinators review records for each region; ongoing validation throughout the season.
  - Further automated/manual validation checks identify records outside known distributions, outside normal flight periods, first sightings at a site, atypical abundances, or large deviations from typical site values; corrections are made through queries and coordination with recorders.

- Data download details (phenology dataset):
  - The download provides phenology data for all species across all sites and years with sufficient data, in CSV format.
  - For thirteen species, data are available for the entire flight period and, where possible, for two distinct flight periods per year per site; for all other species, data cover the entire flight season only.
  - Key columns include:
    - SITENO, SITENAME, GRIDREF
    - SPECIES_NAME (scientific) and COMMON_NAME
    - YEAR, NUMBER_OF_BROODS, BROOD
    - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT
    - MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE
  - Brood values: 0 = entire flight period; 1 = first flight period; 2 = second flight period.
  - Twenty-first-century taxonomy follows Agassiz et al. updates; thirteen species noted for dual-flight-period data (eleven multivoltine species plus Brimstone and Peacock).

- Licence and attribution:
  - Data are provided under the Open Government Licence (OGL), allowing free use with few conditions.
  - Required to cite the dataset with the DOI in any reports/publications describing research using the data.
  - Attribution statement to include: Contains UK Butterfly Monitoring Scheme (UKBMS) data © copyright and database right Butterfly Conservation, CEH, BTO, and JNCC.

- Collaboration and contact details:
  - UKBMS partners offer guidance on dataset usage and interpretation, potential co-authorship, and intellectual input for publications.
  - Contacts:
    - UK Centre for Ecology & Hydrology, Marc Botham: ukbms@ceh.ac.uk
    - Butterfly Conservation, Transect co-ordinator: transect@butterfly-conservation.org