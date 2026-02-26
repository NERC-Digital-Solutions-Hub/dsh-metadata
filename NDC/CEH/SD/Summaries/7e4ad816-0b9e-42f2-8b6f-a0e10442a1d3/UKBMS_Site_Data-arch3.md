# UK Butterfly Monitoring Scheme (UKBMS)

## Overview
- UKBMS gathers data from over 2,000 sites annually across the UK to monitor butterfly populations and inform conservation policy.
- Data are collected using standardised methods to enable consistent year-to-year comparisons and trend analysis.

## Experimental design and sampling regime
- All-species transects (Pollard walks): fixed-route 2–4 km, 5 m wide, weekly counts April–September; routes fixed to sample habitat types and management; aims for ~26 counts per year.
- Observation times and conditions: 10:45–15:45, dry conditions, wind Beaufort < 5, temperature thresholds (≥13°C with ≥60% sunshine or ≥17°C if overcast).
- Single-species transects: follow the same methodology as all-species transects but record only during a few weeks of the focal species’ flight period.
- Timed counts and egg/larval web counts: species-specific counts over a set area and period; egg/larval webs counted in suitable habitats.
- Wider Countryside Butterfly Survey (WCBS): reduced-effort surveys since 2009 sampling wider countryside habitats; two parallel 1-km transects within randomly selected 1-km squares, following the fixed-route transect methodology; 2–4 visits per year with a minimum of 2 visits in July/August and encouraged spring visits.

## Data collection methods
- Site location data recorded in the field when transects, timed counts, or larval web counts are set up.
- Data entered online via the UKBMS data entry site or via Transect Walker software; route changes create a new site with a new site number.
- Online data and Transect Walker files are uploaded into an Oracle database.

## Nature and units of recorded values
- Site location data include: OS grid reference, transect length (metres), number of sections, and WCBS status (whether WCBS applies).
- Grid reference is broken down into Easting and Northing coordinates.
- WCBS sites may have incomplete information due to randomised 1-km-square sampling.

## Quality control
- Each site is managed by a regional transect coordinator with local site knowledge.
- Records undergo preliminary validation followed by automated and manual checks to verify accuracy of site location data.

## Format of stored data
- Site Location Data stored as CSV with columns:
  - Site number, Site name, Gridreference, Easting, Northing, Length, Country, No. Sections, No. Yrs surveyed, First year surveyed, Last year surveyed, Survey type (WCBS for WCBS sites; UKBMS for all other transects and surveys).