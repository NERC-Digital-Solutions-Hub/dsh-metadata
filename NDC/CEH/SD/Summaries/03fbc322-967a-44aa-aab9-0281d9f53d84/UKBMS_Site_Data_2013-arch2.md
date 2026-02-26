# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK to monitor butterfly abundance and habitat management effects.
- Monitoring relies on fixed transect methods to enable year-to-year comparability of sightings.

## Sampling methods

- All-species transects: fixed-route line transect at each site; record all butterflies along the route on a weekly basis under standardised weather conditions; transects are typically 2–4 km long and divided into habitat/management sections; aim for 26 counts per year from April to September; transects are kept fixed to maintain comparability.
- Single-species transects: follow the all-species method but record for only one or a few weeks during the focal species’ flight period.
- Timed counts: record abundance of a particular species over a set period and area, following the same daily time window and weather criteria as transects.
- Egg/larval web counts: count eggs or larval webs of target species in suitable habitat areas (e.g., Marsh Fritillary).

## Temporal and environmental constraints

- Walking windows: counts conducted between 10:45 and 15:45.
- Weather conditions: suitable butterfly activity required; specifics include dry conditions, wind speed below Beaufort scale 5, and temperature thresholds (at least 13°C with 60% sunshine, or more than 17°C if overcast).

## Data collection and processing

- Field data are recorded at site setup and entered into Transect Walker, a bespoke software (free download from ukbms.org).
- Data entry can be by the recorder or a regional transect coordinator; route changes create a new site with a new site number.
- Transect Walker files are uploaded into an Oracle database that stores all records.

## Nature and units of recorded values

- Site location data include: OS grid reference, transect length (metres), number of transect sections, and for most sites, incomplete data may occur.
- Grid reference is broken down into Easting (X) and Northing (Y) coordinates.

## Quality control

- Data are managed regionally by transect coordinators who validate and verify records.
- A sequence of automated and manual validation steps follows initial regional checks to ensure accuracy of site location and other key fields.

## Format and storage of site location data

- Stored as a CSV file with columns:
  - Site number
  - Site name
  - Gridreference (OS)
  - Easting
  - Northing
  - Length (m)
  - Country
  - No. Sections
  - No. Yrs surveyed
  - First year surveyed
  - Last year surveyed

- The dataset captures the start location of transects, their spatial extent, and historical surveying coverage (up to specified years in the document).