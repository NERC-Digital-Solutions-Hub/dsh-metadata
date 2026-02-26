# Experimental design/sampling regime

- Overview
  - The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK.
  - Data types include all-species transects, reduced-effort Wider Countryside Butterfly Survey (WCBS) transects, single-species transects, timed counts, and egg/larval web counts.
  - Transects and counts are designed to sample habitats and management activities, enabling year-to-year comparisons.

- Data collection methods
  - All-species transects: fixed-route, 2–4 km, 45 minutes to 2 hours, recorded weekly (April–September) in a 5 m wide band; 26 counts per year; transect routes remain fixed to allow comparison over years.
  - Weather and timing: observations conducted only under suitable butterfly activity conditions (specific temperature, wind, and sunshine criteria) and within 10:45 am–3:45 pm.
  - Single-species transects: follow the same methodology as all-species transects but record data only during a few weeks for the focal species.
  - Timed counts: record abundances of a species over a fixed time/area window under similar weather constraints.
  - Egg/larval web counts: record eggs or larval webs of a species in suitable habitat areas.
  - Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling of wider countryside habitats (2–4 visits, several 1-km squares per site, randomised), modeled after the BTO’s Breeding Bird Survey.

- Data collection and entry
  - Site location data are collected in the field and entered online via the UKBMS data entry site or the Transect Walker software.
  - Data can be entered directly by recorders or by regional transect coordinators.
  - If a transect route changes, the new route is treated as a new site with a new site number.
  - Online data and Transect Walker files are uploaded into an Oracle database.

- Nature and units of recorded values
  - Site location data include OS grid reference, transect length (metres), number of transect sections, and WCBS participation flag.
  - Grid references are broken down into Easting and Northing coordinates.
  - For WCBS sites, data availability may be limited due to randomized 1-km square selection.

- Quality control
  - Each site belongs to a regional transect coordinator responsible for data checks.
  - Records undergo preliminary validation by the regional coordinator, followed by automated and manual validation procedures to verify site location and data integrity.

- Format of stored data
  - Site Location Data are stored as CSV files with columns including:
    - Site number, Site name, Gridreference, Easting, Northing, Length, Country, No. Sections, No. Yrs surveyed, First year surveyed, Last year surveyed, Survey type (WCBS or UKBMS).
  - WCBS sites may have incomplete information due to randomised sampling.
  - The 1-km square designation for WCBS is recorded in the dataset’s survey type field.