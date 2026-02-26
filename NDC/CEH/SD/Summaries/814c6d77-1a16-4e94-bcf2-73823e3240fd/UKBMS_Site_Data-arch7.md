# Experimental design/sampling regime

## Overview
- The UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK.
- Data are gathered through fixed transects (Pollard walks) and various standardized methods to estimate butterfly abundance.
- GIS-friendly data are produced from site location data, transect routes, and survey type.

## Data collection methods and transect types
- All-species transects: fixed-route line transects, weekly counts April–September, 26 counts/year, transect lengths typically 2–4 km, 5 m wide data band.
- Transects are chosen to represent habitat types and management; routes are fixed to enable year-to-year comparisons.
- Weather- and time-of-day constraints apply (approx. 10:45–15:45; suitable butterfly activity conditions).
- Single-species transects: similar method but focused on a focal species for fewer weeks.
- Timed counts: counts of a species over a set period/area under weather constraints.
- Egg/larval web counts: record eggs or larval webs in suitable habitat.
- Wider Countryside Butterfly Survey (WCBS): reduced-effort survey along two parallel 1-km transects within randomly selected 1-km squares; 2–4 visits per year.

## Data collection and storage workflow
- Field data recorded in the field and entered online via UKBMS data entry site or via Transect Walker software.
- If a transect route changes, the new route is treated as a new site with its own site number.
- Data and Transect Walker outputs are uploaded to an Oracle database; online data and Transect Walker files feed the central database.

## Site location data and data attributes
- Site data include: OS grid reference, transect length (m), number of sections, WCBS flag.
- Grid references are decomposed into Easting (X) and Northing (Y) coordinates.
- Some WCBS site data may be incomplete; WCBS sites are based on randomised 1-km squares.
- Key fields: site number, site name, grid reference, easting, northing, length, country, number of sections, years surveyed, first year surveyed, last year surveyed, survey type (WCBS or UKBMS).

## Quality control and data format
- Regional transect coordinators validate site records; followed by automated and manual checks for data correctness.
- Data stored as CSV with defined columns (site number, site name, grid reference, easting, northing, length, country, number of sections, years surveyed, first year, last year, survey type).
- Last full coverage noted up to 2016 in the described dataset.

## Practical GIS implications
- Fixed transect routes enable robust temporal comparisons; suitable for change detection over years.
- Multiple survey types provide varying spatial resolutions and coverage; WCBS offers broader area sampling with fewer visits.
- Spatial coordinates are provided as OS grid references with Easting/Northing, facilitating GIS integration.
- Route changes create new site identifiers, impacting longitudinal analyses; maintain careful tracking of site IDs.
- Data management relies on CSV exports and an Oracle database, requiring data cleaning and schema alignment for GIS workflows.

## Key takeaways for GIS specialists
- Align UKBMS site data with GIS layers using OS grid references and Easting/Northing coordinates.
- Plan for integrating data from diverse survey types (UKBMS vs WCBS) with differing resolutions and temporal coverage.
- Anticipate route changes creating new sites; implement strategies to link historical data to new site identifiers when analyzing trends.
- Ensure quality control processes are accounted for in spatial analyses, given the validation steps by regional coordinators and automated checks.