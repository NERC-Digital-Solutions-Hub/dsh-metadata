# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 1,000 sites annually across the UK, primarily via fixed linear transects known as Pollard walks, with some sites using alternative methods (timed counts, egg/larval web counts) for certain species.
- All-species transects: fixed-route line transects (2–4 km) where all butterflies are recorded along a 5 m wide band each week from April to September, yielding up to ~26 counts per year. Routes are chosen to sample habitat types and management; routes remain fixed to enable year-to-year comparisons.
- Weather and timing constraints for transects: walks occur between 10:45 and 15:45 under suitable butterfly activity conditions (dry; Beaufort windspeed < 5; temperature thresholds: ≥13°C with at least 60% sunshine, or ≥17°C if overcast).

- Other sampling methods:
  - Single-species transects follow the all-species methodology but are recorded only in a few weeks.
  - Timed counts measure abundance of a focal species over a set period/area.
  - Egg/larval web counts record eggs or larval webs in suitable habitat areas.

- Spatial design and terminology:
  - Transects are fixed routes designed to represent habitat and management variation on each site.
  - The route of a transect is the primary spatial unit; changes to a route are treated as a new site with a new site number.

# Data collection workflow

- Field data collection: site location data are recorded in the field when transects are set up (or counts are conducted) and entered into Transect Walker (free software).
- Data entry: records are entered directly by the recorder or by the regional transect coordinator.
- Data submission and storage: Transect Walker files are uploaded into an Oracle database holding all records.
- Route changes: if a transect route changes, data for the new route are submitted as a new site with a new site number.

# Spatial data and coordinate handling

- Geographic information captured at site setup includes:
  - OS grid reference (primary) for each site, with Easting and Northing (X, Y) coordinates derived from the grid reference.
  - Transect length (in metres) and the number of sections along the transect.
- Coordinates and site geometry are used for GIS mapping and spatial analyses; the grid reference is typically 6-figure accuracy.

# Data structure, storage, and scope

- Primary data format for site location data: CSV.
- Key columns in the Site Location Data CSV:
  - Site number: unique sequential identifier for each site.
  - Site name: name of the transect location.
  - Gridreference: Ordnance Survey grid reference for the site (start point of the transect route).
  - Easting: X coordinate derived from the grid reference.
  - Northing: Y coordinate derived from the grid reference.
  - Length: total transect length (metres).
  - Country: country within the UK where the site is located.
  - No. Sections: number of sections the transect route is divided into.
  - No. Yrs surveyed: number of years with butterfly abundance data collected at the site up to 2013.
  - First year surveyed: first year with UKBMS data collection at the site.
  - Last year surveyed: most recent year with UKBMS data collection (up to 2012).

# Quality control and data validation

- Regional coordinators are responsible for verifying site data and have in-depth knowledge of the sites.
- After initial checks by coordinators, data undergo automated and manual validation to confirm accuracy of site location and related fields.

# Practical implications for GIS use

- Spatial datasets are anchored to fixed transect routes, enabling robust temporal comparisons and trend mapping.
- Data quality is reinforced by regional oversight and multi-stage validation, with route changes treated as new spatial features (sites) in the database.
- Data are stored in a CSV format for site location, with coordinates derived from OS grid references, suitable for integration into GIS workflows, alongside the Oracle-backed repository of all records.