# Dataset title First egg dates for Great Tits and Blue Tits breeding in three deciduous woods in Cambridgeshire, England in 1993 to 2014.

## Overview
- A long-term, map-relevant dataset capturing the first egg dates of two tit species (Great Tit and Blue Tit) breeding in three Cambridgeshire deciduous woods from 1993 to 2014.
- Used to assess spring phenology and climate warming by tracking breeding timing.

## Spatial and temporal scope
- Study sites: Monks Wood National Nature Reserve, Brampton Wood, and Wennington Wood.
- Geographic focus: Cambridgeshire, eastern England (with coordinates and wood-specific area details provided in the dataset description).
- Temporal coverage: 1993–2014 (22 years).

## Study species and nest-box setup
- Species: Great Tit (Parus major) and Blue Tit (Cyanistes caeruleus).
- Nest boxes: Wooden boxes (approx. 110 x 130 x 200 mm) at 1–2 m height; accessibility by species determined by hole size.
- Box distribution varies by wood and over time; Brampton Wood includes some dormouse boxes used by blue tits since the mid-1990s.

## Data collection and structure
- Data collection: Boxes inspected ~weekly during the laying period (late March onward); first egg dates inferred from clutches (one egg per day) and active nests only (at least one more egg). Only first breeding attempts included; replacement clutches and second broods excluded.
- File format: CSV (Unicode), GTBTfirsteggdates.CSV (43 lines roughly; 39.4 KB).
- Columns:
  - 1: Species code (1 = Great Tit; 2 = Blue Tit)
  - 2: Site (1 = Monks Wood; 2 = Brampton Wood; 3 = Wennington Wood)
  - 3: Year number (Year 1 = 1993 to Year 22 = 2014)
  - 4: Nest box identifier (note: Monks Wood boxes 23–30 do not exist)
  - 5: First egg date (April 1 = 1; March dates appear as negative values; three negative values occur in 1997)
  - 6: Sample size N for the number of clutches included per year

## Variables and coding details
- First egg date is the primary phenology metric; negative dates indicate March laying.
- Year numbering is relative to 1993 (Year 1) through 2014 (Year 22).
- Site and box identifiers enable spatial linkage to nest-box location data for GIS analyses.

## Quality control and data provenance
- Collected by trained field personnel; egg dates cross-checked with original paper records.
- Data checked for consistency, outliers, and alignment with yearly site means.

## GIS-focused usage and integration
- Suitable for map-based visualization of breeding phenology across sites and years.
- Can be joined with spatial layers of nest-box locations, woodland boundaries, and habitat/landscape data.
- Enables temporal trend analysis of first-egg timing by site and species, contributing to climate-phenology research and policy-relevant spatial summaries.

## caveats and notes
- Box availability varies by site and year; some box numbers are missing in Monks Wood.
- March hatch dates are rare (few negative values) and should be treated accordingly during analysis.
- Data represents first breeding attempts only; not applicable to second broods or replacement clutches.