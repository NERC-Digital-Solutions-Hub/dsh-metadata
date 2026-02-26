# About the UK Butterfly Monitoring Scheme

- Overview and purpose
  - The UK Butterfly Monitoring Scheme (UKBMS) is organized and funded by Butterfly Conservation, the UK Centre for Ecology & Hydrology, the British Trust for Ornithology, and the Joint Nature Conservation Committee.
  - It relies on volunteers and provides annual, site-based population data for butterflies to support understanding of biodiversity status and policy questions.
  - Since 1976, the scheme has monitored butterfly abundance across the UK, with over 3,000 actively recorded sites each year.
  - Data from all sampling methods are analyzed together to give a comprehensive view.

- Data collection framework
  - Standard butterfly transects (Pollard walks): fixed-route transects (2–4 km) with weekly counts (typically 26 per year) across Apr–Sep.
  - Wider Countryside Butterfly Survey (WCBS): stratified-random 1 km squares with two parallel transects, 2–3 visits per year (minimum two in July/August).
  - Targeted surveys: single-species transects, timed counts, and egg/larval web counts.
  - The program uses multiple methods to cover various habitats and species, enabling broad trend analyses.

- Nature of the data collected
  - Phenology data: timing of adult butterfly flight periods (imago stage) on UKBMS transects.
  - Phenology metrics include first/last recording dates, peak date and count, mean flight date, standard deviation around mean, and flight period range.
  - For species with multiple generations (multivoltine) or two univoltine species, data can be split into distinct flight periods where possible; for some species, data reflect the entire flight period due to overlapping generations.
  - Data limitations due to uneven weekly coverage and the March–September recording window are acknowledged; alternative phenology metrics are provided to mitigate these limitations.

- Quality control and data integrity
  - Field data are entered via online forms or Transect Walker; automatic checks flag potential errors.
  - Regional transect coordinators perform ongoing validation; additional automated and manual checks screen out-of-range records, unusual abundances, or records outside known distributions or flight periods.
  - Corrections are made through queries and coordination with recorders before finalizing the UKBMS dataset.

- Details of this data download
  - Provides phenology data for all species, at all sites and years with sufficient data.
  - Data are delivered as a CSV file.
  - For 13 species, data may include entire flight periods plus separate first and second flight periods; other species are provided for the entire flight season only.
  - Key columns include:
    - SITENO, SITENAME, GRIDREF
    - SPECIES_NAME, COMMON_NAME
    - YEAR, NUMBER_OF_BROODS, BROOD
    - FIRSTDAY, LASTDAY, PEAKDAY, PEAKCOUNT
    - MEAN_FLIGHT_DATE, FLIGHTPERIOD_SD, FLIGHTPERIOD_RANGE

- Licence and attribution
  - Data are provided under an Open Government Licence (OGL), enabling free use with few conditions.
  - Publications using the data must include the citation and DOI as specified in the metadata record.
  - Attribution statement: Contains UKBMS data © Butterfly Conservation, CEH, BTO, and JNCC.

- Offer of collaboration and contact details
  - UKBMS partners offer advisory support and interpretation help.
  - Potential for co-authorship and intellectual input in resulting publications, conference presentations, or posters.
  - Contacts:
    - UK Centre for Ecology & Hydrology: ukbms@ceh.ac.uk
    - Butterfly Conservation: transect@butterfly-conservation.org

- Practical governance takeaways for data stewards
  - Clear provenance and governance: data come from a coordinated UK-wide program with defined recording methods and QA processes.
  - Standardized formats and metadata: consistent field names and column definitions facilitate interoperability and reuse.
  - Access and licensing: open license (OGL) supports wide reuse, with required attribution and citation.
  - Quality assurance: multi-layer validation (field checks, regional coordinators, automated/manual QC) ensures data reliability before sharing.
  - Collaboration framework: explicit offers of support and co-authorship help foster responsible data use and dissemination.