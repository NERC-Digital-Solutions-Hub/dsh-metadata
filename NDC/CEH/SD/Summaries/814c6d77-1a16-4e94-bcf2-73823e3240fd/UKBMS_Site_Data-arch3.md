# Experimental design/sampling regime

- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK to monitor butterfly abundance and distribution through standardized methods.

- Primary monitoring approaches:
  - All-species transects (Pollard walks): fixed-route line transects 2–4 km long, where all butterflies within a ~5 m belt are recorded weekly from April to September to enable year-to-year comparability.
  - Fixed transect design ensures routes remain constant to facilitate longitudinal comparisons; transects are sampled under weather conditions suitable for butterfly activity.
  - Weather criteria: data collection occurs between 10:45 and 15:45, dry conditions, wind below Beaufort scale 5, and minimum temperature thresholds (≥13°C with ≥60% sunshine, or ≥17°C if overcast).
  - Single-species transects: follow the all-species approach but focus on a few focal species during a subset of weeks.
  - Timed counts: counts of a particular species within a defined area and time window, under the same weather constraints as transect counts.
  - Egg/larval web counts: record eggs or larval webs of focal species in suitable habitats.

- Wider Countryside Butterfly Survey (WCBS):
  - Established in 2009 as a reduced-effort survey to sample farmland and wider countryside habitats.
  - Based on the BTO Breeding Bird Survey (BBS) framework; uses two parallel 1-km transects within randomly selected 1-km squares.
  - Typically 2–4 visits per site, with a minimum of 2 visits in July/August; spring visits encouraged.

- Data collection and entry:
  - Field site data are recorded during transect setup and entered online via the UKBMS data portal (MyData) or via Transect Walker software.
  - If a transect route changes, the new route is recorded as a new site; data for the new route follow the same submission process.

- Data storage and management:
  - All data are uploaded to an Oracle database that holds the complete records.

- Nature and units of recorded values:
  - Site location data include OS grid references, transect length (metres), number of transect sections, and WCBS status.
  - For WCBS sites, data may be incomplete due to random 1-km square sampling.
  - Grid references are further broken down into Easting (X) and Northing (Y) coordinates.

- Quality control and validation:
  - Each site is overseen by a regional transect coordinator who validates records.
  - Additional automated and manual validation procedures are applied to ensure accuracy of site location data.

- Format of stored data (site location data example):
  - CSV structure with: Site number, Site name, Gridreference, Easting, Northing, Length, Country, No. Sections, No. Yrs surveyed, First year surveyed, Last year surveyed, Survey type (WCBS or UKBMS).

- Historical context:
  - The methodology references established practices, including Pollard, E. & Yates, T.J. (1993) as foundational guidance.