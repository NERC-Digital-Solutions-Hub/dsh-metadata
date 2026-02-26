# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects butterfly data from over 2,000 sites annually across the UK, using multiple data collection methods to capture abundance and distribution.

- Data collection methods
  - All-species transects (Pollard walks)
    - Fixed-route line transects sampled weekly under suitable weather conditions.
    - Transects are 2–4 km long, divided into habitat-based sections, and typically yield 26 counts per year.
    - Data recorded as all species within a fixed-width (about 5 m) band along the transect from April to September.
    - Routes must remain fixed to enable year-to-year comparisons.
  - Single-species transects
    - Follow the all-species methodology but record only a focal species, on a subset of weeks.
  - Timed counts and egg/larval web counts
    - Timed counts record abundance of a species over a set period and area, within specified daily time windows.
    - Egg/larval web counts document egg numbers or larval webs in suitable habitats.
  - Wider Countryside Butterfly Survey (WCBS)
    - Established in 2009 to sample wider countryside habitats with reduced effort.
    - Based on the BTO Breeding Bird Survey approach: two parallel 1-km transects within randomly selected 1-km squares.
    - Typically 2–4 visits, with a minimum of 2 visits in July/August; spring visits encouraged.

- Data collection workflow
  - Site location data collected in the field at transect setup and entered online via the UKBMS data entry site or Transect Walker software.
  - If a transect route changes, data for the new route are submitted as a new site (new site number).
  - Online data and Transect Walker files are uploaded into an Oracle database containing all records.

- Nature and units of recorded values
  - Site location data include:
    - OS grid reference (typically 6-figure accuracy), and Easting/Northing coordinates.
    - Transect length, number of sections, whether WCBS is used.
    - Number of years surveyed at the site, first and last year surveyed (up to 2016 in the described dataset).
    - Survey type: WCBS or UKBMS (UKBMS for all-species transects and timed/larval counts).

- Quality control
  - A regional transect coordinator reviews records for their sites.
  - Records undergo preliminary validation, followed by automated and manual validation procedures to check location data and consistency.

- Data storage and formats
  - Site Location Data stored as a CSV file with fields:
    - Site number, Site name, Gridreference, Easting, Northing, Length, Country, No. Sections, No. Yrs surveyed, First year surveyed, Last year surveyed, Survey type (WCBS or UKBMS).