# Experimental design/sampling regime

- Purpose and scope
  - UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites per year across the UK.
  - Butterfly counts are primarily via fixed linear transects (Pollard Walk) with additional methods for some species.

- Transect methodologies
  - All-species transects
    - Fixed-route line transect at a site; all butterflies recorded along the route weekly.
    - Transects typically 2–4 km; 45 minutes to 2 hours to complete.
    - Route divided into sections by habitat/management; fixed to enable year-to-year comparisons.
    - Counts cover a 5 m wide band along the transect; aiming for 26 counts per year from early April to late September.
    - Observations conducted only during suitable butterfly-activity weather: 10:45–15:45, dry conditions, wind < Beaufort 5, temperature thresholds (≥13°C with ~60% sunshine, or >17°C if overcast).
  - Single-species transects
    - Follow the all-species methodology but focus on one or a few focal species for a subset of weeks.

- Other data collection methods
  - Timed counts: abundance of a focal species recorded over a set period and area.
  - Egg/larval web counts: number of eggs or larval webs recorded in suitable habitat areas (e.g., Marsh Fritillary).

- Data capture and workflow
  - Field data are entered into Transect Walker (free software) by the recorder or regional transect coordinator.
  - If a transect route changes, the new route is treated as a new site with a new site number.
  - Transect Walker files are uploaded to an Oracle database containing all records.

- Site location data and measurement units
  - Data include OS grid reference (start location of transect), length of transect, and number of sections.
  - Grid reference is decomposed into Easting (x) and Northing (y) coordinates.
  - Data completeness may vary for a small number of sites.

- Quality control
  - Each site belongs to a region overseen by a transect coordinator with local knowledge of the sites.
  - Preliminary validation by coordinators, followed by automated and manual validation procedures to verify site location data.

- Format and content of stored data
  - Site Location Data stored as CSV with the following columns:
    - Site number: unique sequential identifier
    - Site name: name of the transect site
    - Gridreference: OS grid reference (start of transect), typically 6-figure accuracy
    - Easting: x-coordinate of the start point
    - Northing: y-coordinate of the start point
    - Length: total transect length in metres
    - Country: UK country where the site is located
    - No. Sections: number of sections the transect route is divided into
    - No. Yrs surveyed: number of years butterfly data has been collected at the site under UKBMS (up to and including 2013)
    - First year surveyed: first year of butterfly abundance data collection at the site under UKBMS
    - Last year surveyed: most recent year of butterfly abundance data collection at the site under UKBMS (up to 2012)

- Notes on data scope
  - Transects are designed to sample representative habitat types and management activities at each site.
  - The design emphasizes longitudinal comparability and linkages between site locations, transect routes, and yearly observations.