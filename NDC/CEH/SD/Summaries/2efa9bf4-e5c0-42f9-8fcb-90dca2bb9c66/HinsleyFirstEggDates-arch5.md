# First egg dates for Great Tits and Blue Tits breeding in three deciduous woods in Cambridgeshire, England in 1993 to 2015.

## Overview
- Dataset records the first egg dates for Great Tits and Blue Tits breeding in three Cambridgeshire deciduous woods from 1993 to 2015.
- Breeding timing serves as an indicator of spring phenology and broader climate warming trends; data contribute to a long-term study on habitat, landscape factors, and woodland bird breeding success.

## Study and species context
- Study species: Great Tit (Parus major) and Blue Tit (Cyanistes caeruleus).
- Birds breed in wooden nest boxes (mostly accessible to both species; some boxes only for Blue Tits due to hole sizes).
- Study woods: Monks Wood National Nature Reserve, Brampton Wood, and Wennington Wood (Cambridgeshire, eastern England).
- Box configuration varies by site and over time; 1993–2015 box counts range from 21 to 35 per site, with differences in accessibility and box availability.

## Data collection method
- Boxes inspected approximately weekly during the laying period (starting late March).
- First egg date derived by counting backward from observed eggs (one egg laid per day).
- Only nests that are active at observation (at least one more egg to be laid) are included.
- Only first breeding attempts are recorded; replacement clutches and second broods are excluded.

## Data structure and contents
- File: GTBTfirsteggdates.CSV (CSV, Unicode), 42 KB.
- Columns:
  - 1) Species code: 1 = Great Tit; 2 = Blue Tit
  - 2) Site: 1 = Monks Wood; 2 = Brampton Wood; 3 = Wennington Wood
  - 3) Year number: 1–23, where Year 1 = 1993 and Year 23 = 2015
  - 4) Nest box identifier (note: in Monks Wood, boxes 23–30 do not exist)
  - 5) First egg date: April 1 = 1; March dates appear as negative values (only 3 negative values in Year 5, 1997)
  - 6) Sample size (N) for the number of clutches included per year
- Data are organized per year-site-box with corresponding first-egg-date values.

## Temporal and spatial scope
- Temporal scope: 1993–2015 (23 years).
- Spatial scope: three deciduous woods in Cambridgeshire, England (Monks Wood, Brampton Wood, Wennington Wood).

## Quality control and data validation
- Field data collected by trained, experienced personnel.
- Egg dates cross-checked against original paper records.
- Consistency checks: line counts, detection of outliers, and alignment of individual egg dates with yearly site means.

## Metadata and governance considerations
- Metadata include explicit definitions for each column, site box availability, and handling of March dates (negative values).
- Clear documentation of data processing (derivation of first egg dates from daily laying, inclusion criteria).
- Suitable for discovery and reuse within larger long-term datasets on habitat, landscape factors, and avian breeding success; ensure proper standards for metadata, provenance, and versioning when sharing or updating.