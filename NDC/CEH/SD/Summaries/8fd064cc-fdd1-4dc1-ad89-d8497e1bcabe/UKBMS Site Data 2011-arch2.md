# Experimental design/sampling regime

- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK to monitor butterfly populations and support environmental health assessments.

- All-species transects
  - Fixed-route line transects established at each site; all butterflies recorded along the route weekly.
  - Transects are 2–4 km long, divided into habitat/management sections; fixed routes enable year-to-year comparisons.
  - Data collected in a 5 m wide belt along the transect; target data collection from early April to late September (approximately 26 counts per year).
  - Walks occur between 10:45 and 15:45 under suitable butterfly-activity weather: dry, Beaufort wind <5, and temperature thresholds (≥13°C with ≥60% sunshine or >17°C if overcast).
  - Routes are chosen to sample habitat types and management activities; changes to a route reclassify it as a new site.

- Single-species transects
  - Follow the all-species transect methodology but focus on a single species and operate only during select weeks of the flight period.

- Timed counts and egg/larval web counts
  - Timed counts record a species' abundance over a fixed time and area under the same weather constraints as transects.
  - Egg and larval web counts record eggs or larval webs in appropriate habitat areas (e.g., for Marsh Fritillary).

- Data collection methods
  - Field site location data captured during setup; entered into Transect Walker software (free download from UKBMS website).
  - Data input by the recorder or by the regional transect coordinator; route changes create a new site with a new site number.
  - Transect Walker files uploaded into an Oracle database housing all records.

- Nature and units of recorded values
  - Site location data include OS grid reference, transect length (metres), and number of transect sections.
  - Grid reference is broken down into Easting (x) and Northing (y) coordinates.
  - Some sites may have incomplete information.

- Quality control
  - Each site belongs to a region with a transect coordinator responsible for data checks.
  - Preliminary validation followed by automated and manual validation procedures to verify site location data.

- Format of stored data
  - Site Location Data stored as CSV with columns:
    - Site number
    - Site name
    - Gridreference (OS)
    - Easting
    - Northing
    - Length
    - Country
    - No. Sections
    - No. Yrs surveyed
    - First year surveyed
    - Last year surveyed (up to 2012)