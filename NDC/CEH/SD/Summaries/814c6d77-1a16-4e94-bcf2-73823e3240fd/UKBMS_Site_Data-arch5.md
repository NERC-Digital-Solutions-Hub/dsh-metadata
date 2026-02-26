# Experimental design/sampling regime

## Overview
- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites annually across the UK, using multiple standardized methods to estimate butterfly abundance.

## Data collection methods and sampling design
- All-species transects (Pollard walks): fixed-route line transects, typically 2–4 km long, recording all butterfly species along a 5 m wide belt each week from April to September; aim for 26 counts per year; routes fixed to enable year-to-year comparability.
- Transect timing and conditions: observations conducted between 10:45 and 15:45 under predefined weather conditions (dry, wind Beaufort ≤ 5, minimum temperature thresholds with sun or overcast adjustments).
- Single-species transects: follow the same all-species transect methodology but limited to a few weeks during the focal species’ flight period.
- Timed counts and egg/larval web counts: focused counts for particular species or life stages.
- Wider Countryside Butterfly Survey (WCBS): reduced-effort sampling in wider habitats; two parallel 1 km transects within randomly selected 1 km squares; 2–4 visits per year with recommended visits in July/August and spring.

## Data capture and storage
- Site location data collected in the field and entered online via the UKBMS data entry site or Transect Walker software.
- If a transect route changes, the new route is recorded as a new site with a new site number.
- All data and Transect Walker files are uploaded into an Oracle database.

## Data formats, units and metadata
- Site location data include:
  - Site number (unique sequential identifier)
  - Site name
  - Grid reference (Ordnance Survey)
  - Easting and Northing (X, Y coordinates)
  - Length of transect (metres)
  - Country
  - Number of sections on the transect
  - Number of years surveyed (to date)
  - First year surveyed and Last year surveyed (up to 2016 in the described dataset)
  - Survey type (WCBS or UKBMS)
- WCBS sites may have incomplete data due to their randomised 1 km-square design.
- Data stored as CSV files with a defined column structure for site location data.

## Quality control
- A regional transect coordinator is responsible for verifying site data, supported by preliminary validation checks.
- Data undergo automated and manual validation procedures after regional validation to ensure accuracy of site location data and consistency across years.

## Implications for Data Stewards
- Emphasize standardized, reproducible data collection and explicit documentation of survey types, routes, and timing.
- Maintain consistent identifiers (site numbers) while correctly handling route changes (new site numbers).
- Ensure data are stored in interoperable formats (CSV) and centralized repositories (Oracle DB) with clear metadata to support discovery, reuse, and long-term governance.
- Track completeness and data quality, including handling incomplete WCBS data where applicable.