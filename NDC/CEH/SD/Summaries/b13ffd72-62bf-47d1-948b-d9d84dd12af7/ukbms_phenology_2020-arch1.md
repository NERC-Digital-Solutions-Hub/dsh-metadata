# About the UK Butterfly Monitoring Scheme

- Overview and purpose
  - The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology (UKCEH), the British Trust for Ornithology (BTO), and the Joint Nature Conservation Committee (JNCC).
  - It relies on volunteers to collect annual, site-based data to understand changes in butterfly populations and to inform biodiversity policy questions.
  - Since 1976, UKBMS has monitored butterfly abundance across the UK, with over 2,500 actively recorded sites each year.

- Data collection framework
  - Standard butterfly transects (Pollard walks): fixed-route, 2–4 km, 5 m belt, recording all species weekly (up to 26 counts/year) at ~2,000 sites; conducted under suitable weather.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares sampled with two parallel 1 km transects; 2–3 visits/year to sample common habitats (around 800 squares/year).
  - Targeted surveys: single-species transects and alternative methods (timed counts, egg/larval web counts) for specific species.
  - Data are analyzed together across methods; data collection emphasizes weekly counts for phenology.

- Nature of data collected (phenology)
  - Focuses on timing of adult butterfly flight periods (phenology).
  - Phenology metrics are derived from standard transects; less complete for WCBS due to reduced effort.
  - Simple metrics: first/last recording dates, date of peak count, and flight period length (days between first and last observation).
  - Alternative metrics used to accommodate sampling limitations: mean flight date and standard deviation (SD) around mean date to reflect timing and synchrony.
  - Many species are multivoltine; flight period data may be split into up to two distinct generations for eleven multivoltine species and two univoltine species (Brimstone and Peacock) that overwinter as adults.
  - For some species, generations overlap, limiting separation of distinct flight periods; data may represent the entire flight period or be split into first/second periods where feasible.

- Quality control
  - Field data are recorded on standard forms and entered online into the UKBMS system or via Transect Walker.
  - Automated checks flag anomalies (e.g., unusually high counts or out-of-season records); regional transect coordinators perform ongoing validation.
  - Further automated and manual validation checks ensure records align with known distributions and typical flight periods; discrepancies are resolved with coordinators or recorders.

- Details of this data download
  - Provides phenology data for all species across all sites and years where data are sufficient.
  - Data supplied as a CSV (.csv) file.
  - Thirteen species may have data available for the entire flight period plus two distinct flight periods within each year; other species have data for the entire flight season only.
  - Columns include:
    - SITENO, SITENAME, GRIDREF
    - SPECIES_NAME, COMMON_NAME
    - YEAR
    - NUMBER_OF_BROODS, BROOD
    - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT
    - MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE

- Licence and attribution
  - Data are provided under the Open Government Licence (OGL); free use with few conditions.
  - Citations must include the dataset DOI in any publications using the data.
  - Attribution statement: Contains UK Butterfly Monitoring Scheme (UKBMS) data © Butterfly Conservation, UKCEH, BTO, and JNCC.

- Offer of collaboration and contact details
  - UKBMS partners offer guidance on dataset use and interpretation; possible co-authorship and intellectual input for publications.
  - Contacts:
    - UK Centre for Ecology & Hydrology (Marc Botham): ukbms@ceh.ac.uk
    - Butterfly Conservation (Transect co-ordinator): transect@butterfly-conservation.org