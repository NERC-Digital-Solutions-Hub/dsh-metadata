# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK, using fixed transects (Pollard walks) and other standardized methods (timed counts or egg/larval web counts) to estimate butterfly abundance.

- All-species transects:
  - Fixed-route line transect at a site; all butterflies recorded along the route on a weekly basis under set weather conditions.
  - Transsects are 2–4 km long and divided into sections by habitat/management units; routes are fixed to enable year-to-year comparisons.
  - Recording is done in a 5 m wide band along the transect, ideally 26 counts per year from early April to end of September.
  - Observation window: 10:45 am to 3:45 pm; weather requirements: dry, Beaufort wind < 5, and temperature thresholds (≥13°C with ≥60% sunshine, or >17°C if overcast).

- Single-species transects:
  - Follow the all-species transect methodology but record only for one or a few weeks during the focal species’ flight period.

- Timed counts and egg/larval web counts:
  - Timed counts record abundances over a set period/area; conducted within the same time window and weather constraints as above.
  - Egg/larval web counts record eggs or larval webs in suitable habitat areas.

- Data collection methods:
  - Site location data are recorded in the field and entered into Transect Walker (free software) and uploaded to an Oracle database.
  - Data can be entered directly by the recorder or by a regional transect coordinator.
  - If a transect route changes, the new route is treated as a new site with a new site number; data for the new route follow the same submission process.

- Nature and units of recorded values:
  - Site location data include OS grid reference, transect length (metres), and the number of sections on a transect.
  - Grid reference is broken down into Easting and Northing coordinates.
  - For a minority of sites, some information may be incomplete.

- Quality control:
  - A regional transect coordinator validates records; followed by automated and manual validation procedures to check site location data accuracy.

- Format of stored data:
  - Site Location Data stored as CSV with columns:
    - Site number
    - Site name
    - Gridreference (OS grid reference)
    - Easting
    - Northing
    - Length (metres)
    - Country
    - No. Sections
    - No. Yrs surveyed
    - First year surveyed
    - Last year surveyed (up to 2012)