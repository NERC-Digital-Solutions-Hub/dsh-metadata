# Experimental design/sampling regime

## Overview
- UK Butterfly Monitoring Scheme (UKBMS) collects data from over 2,000 sites per year across the UK.
- Data come from multiple collection methods: all-species transects, reduced-effort WCBS transects, single-species transects, timed counts, and egg/larval web counts.
- Most sites use fixed-route all-species transects; other methods provide additional species- or habitat-specific data.
- Transect routes are fixed to enable year-to-year comparisons of butterfly sightings.

## Data collection methods
- All-species transects
  - Fixed-route line transect; 2–4 km long; weekly counts from early April to late September (ideally 26 counts/year).
  - Record all butterfly species within a typical 5 m belt along the transect.
  - Transects divided into sections corresponding to habitat/management units.
  - Weather-dependent: conducted 10:45–15:45, dry conditions, Beaufort wind ≤ 5, temperature thresholds (≥13°C with sun or >17°C if overcast).
- Single-species transects
  - Follows all-species transect methodology but focused on one focal species and conducted on a few weeks.
- Timed counts and egg/larval web counts
  - Timed counts: abundance of a focal species over a set time and area within the same daily time window as transects.
  - Egg/larval web counts: count eggs or larval webs in suitable habitats for a species (e.g., Marsh Fritillary).
- Wider Countryside Butterfly Survey (WCBS)
  - Reduced-effort survey of wider countryside habitats (farmland, etc.).
  - Based on the BTO Breeding Bird Survey methodology: two parallel 1-km transects within randomly selected 1-km squares, 2–4 visits (minimum two in July/August; spring visits encouraged).

## Data collection workflow
- Field data: site location data captured in the field when a transect/timed count/larval web count is setup.
- Data entry: online via the UKBMS data entry site or Transect Walker (free download).
- Data submission: entered by the recorder or regional transect coordinator.
- Route changes: if a transect route changes, data for the new route are submitted as a new site with a new site number.
- Data integration: online data and Transect Walker files uploaded into an Oracle database.

## Nature and units of recorded values
- Site location data include:
  - OS grid reference, transect length (metres), number of sections on a transect.
  - WCBS flag to indicate inclusion in WCBS.
  - Grid reference decomposed into Easting (X) and Northing (Y) coordinates.
- Data completeness: some information for WCBS sites may be incomplete due to randomised 1-km squares.

## Quality control
- Regional transect coordinators validate records with local knowledge.
- Follow-up with preliminary validation checks, then automated and manual validation to ensure accuracy of site location data.

## Format of stored data
- Site Location Data stored as a CSV file with columns:
  - Site number, Site name, Gridreference, Easting, Northing, Length, Country, No. Sections, No. Yrs surveyed, First year surveyed, Last year surveyed, Survey type.
- Survey type field designations:
  - 'WCBS' for Wider Countryside Butterfly Survey sites.
  - 'UKBMS' for all-species transects and other standard/reduced-effort UKBMS surveys.
- 6-figure grid references provide the start location precision for transect routes.