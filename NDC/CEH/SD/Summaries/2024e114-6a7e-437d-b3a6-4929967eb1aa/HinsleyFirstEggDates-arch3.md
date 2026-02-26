# First egg dates for Great Tits and Blue Tits breeding in three deciduous woods in Cambridgeshire, England in 1993 to 2014.

## Overview
- Long-term dataset (1993–2014) of first egg dates for Great Tit and Blue Tit breeding in three Cambridgeshire deciduous woods.
- Used as an indicator of spring phenology and a proxy for climate warming; complements broader research on habitat, landscape factors, and woodland bird breeding success.

## Rationale
- Breeding timing in tits is influenced by daylength, ambient temperature, and prey (tree-dwelling caterpillars) phenology, which themselves respond to temperature and bud burst.
- First egg date provides a consistent, comparable measure of spring phenology across sites and years.
- Breeding timing is a common indicator in studies of climate warming effects on birds.

## Study species and sites
- Species: Great Tit (Parus major) and Blue Tit (Cyanistes caeruleus).
- Nest boxes: monitored at heights of 1–2 m; box access governed by hole size to control species access.
- Study woods (Cambridgeshire, eastern England):
  - Monks Wood National Nature Reserve (52°24'N, 0°14'W; 157 ha): 1993–2000 = 22 boxes; 2001–2014 = 35 boxes.
  - Brampton Wood Wildlife Trust Nature Reserve (52°19'N, 0°16'W; 132 ha): 1993–2014 = 22 boxes.
  - Wennington Wood (private woodland, 52°23'N, 0°10'W; 72 ha): 1993–1999 = 21 boxes; 2000–2014 = 35 boxes.
- Box design influences species use (e.g., common dormouse boxes may affect blue tits in Brampton Wood).

## Data collection and processing
- Inspection frequency: approximately weekly during the laying period (from late March).
- First egg date calculation: counted backwards from the observed number of eggs, assuming one egg per day; eggs laid early morning, inspections occur after the day’s laying.
- Inclusion criteria: only nests active at the time of observation (at least one more egg to be laid); only first breeding attempts included (replacement clutches and second broods excluded).

## Data structure and contents
- File: GTBTfirsteggdates.CSV (Unicode CSV; 39.4 KB).
- Columns:
  - Species code: 1 = Great Tit; 2 = Blue Tit
  - Site: 1 = Monks Wood; 2 = Brampton Wood; 3 = Wennington Wood
  - Year number: Year 1 = 1993 through Year 22 = 2014
  - Nest box identifier (noting site-specific box availability; e.g., Monks Wood boxes 23–30 did not exist)
  - First egg date: converted such that April 1 = 1; March dates appear as negative values (3 negative values in Year 5, 1997)
  - Sample size (N) for the number of clutches included per year

## Quality control and data integrity
- Field data collected by trained personnel.
- Egg dates checked against original paper records.
- Data lines checked; values screened for outliers.
- Individual egg dates cross-validated against yearly means per site.

## Relevance for monitoring frameworks
- Provides a standardized, multi-site, long-term indicator of spring phenology and potential climate warming effects.
- Demonstrates robust data collection, validation, and documentation practices suitable for monitoring governance.
- The dataset’s structured metadata and quality control support reuse, integration with other environmental health indicators, and transparent reporting.

## Limitations and considerations
- Focused only on first breeding attempts; does not capture second or replacement clutches.
- Box availability and site management changes over time (e.g., box counts per site) may affect comparability.
- March dates may yield negative values; dataset limited to three deciduous woods in Cambridgeshire, which may affect generalizability.