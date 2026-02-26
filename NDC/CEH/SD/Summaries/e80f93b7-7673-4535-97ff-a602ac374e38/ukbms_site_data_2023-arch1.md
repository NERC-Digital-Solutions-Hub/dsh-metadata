# About the UK Butterfly Monitoring Scheme

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.
  - It relies on volunteers to collect annual population data across the UK, with over 3000 actively recorded sites each year.
  - Data from all sampling methods are analyzed together to understand butterfly population changes and inform biodiversity policy questions.

- Data collection and sampling framework
  - Standard butterfly transects (Pollard walks): fixed-route 2–4 km transects, 5 m wide, recording all species, typically 26 counts per year (weekly April–September). Sites exceed 2000 by 2022.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel 1 km transects, 2–3 visits per year (minimum two in July/August), focusing on common habitats; ~800 squares sampled per year.
  - Targeted surveys: single-species transects (same method as standard transects but for one species), timed counts, egg and larval web counts for specific species.
  - Data from all methods are combined for analysis.

- Nature of data and trend analysis
  - Data are expressed as abundance indices (relative measures, not absolute population sizes).
  - Indices reflect a constant proportion of butterflies present; detectability varies by species.
  - Seasonal indices are produced with the Generalised Abundance Index (GAI) method (introduced 2016), which weights site data by the proportion of the species flight period surveyed that year, and accounts for gaps in recording while giving more weight to observed data.

- Quality control
  - Field data are recorded on standard forms and entered online or via Transect Walker, with automatic checks for errors (e.g., unusually high counts, records outside known flight periods).
  - Regional transect coordinators review data for questionable entries; ongoing checks during the season.
  - Automated and manual validation checks identify records outside distribution ranges, unusual timing, first-time site records, or atypical abundances; edits are made after discussion with coordinators or recorders.

- Details of this data download
  - Provides location and attribute data for UK sites monitored under UKBMS from 1976 to 2023 (sensitive sites omitted).
  - Data provided as a CSV file.
  - Key columns:
    - Site_number: unique site identifier
    - Site_name: transect location name
    - Gridreference: OS grid reference (central transect)
    - Easting / Northing: coordinate values
    - Length: transect length in meters (if provided)
    - Country: UK country
    - N_Sections: number of transect sections
    - N_Yrs_surveyed: years with data up to 2023
    - First_year_surveyed / Last_year_surveyed: data span per site
    - Survey_type: UKBMS (standard transect) or WCBS

- Licence and attribution
  - Open Government Licence (OGL) applies, enabling free use with minimal conditions.
  - Must include the specified citation with any reports/publications using the data and include the provided attribution statement.
  - Since 2017, submitters agreed to OGL; historic data may have IP considerations—please notify if issues arise.

- Offer of collaboration and contact details
  - UKBMS partners can advise on dataset interpretation and outputs; open to co-authorship and intellectual input for publications, conferences, or posters.
  - Contact:
    - Marc Botham, UK Centre for Ecology & Hydrology (ukbms@ceh.ac.uk)
    - Butterfly Conservation Transect Co-ordinator (transect@butterfly-conservation.org)