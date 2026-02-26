# First egg dates for Great Tits and Blue Tits breeding in three deciduous woods in Cambridgeshire, England in 1993 to 2015.

## Overview
- A dataset of first egg dates for Great Tit (Parus major) and Blue Tit (Cyanistes caeruleus) breeding in three Cambridgeshire woods (Monks Wood, Brampton Wood, Wennington Wood) from 1993 to 2015.
- Purpose: measure spring phenology and climate-warming signals via breeding timing; part of a broader long-term study on habitat factors affecting woodland birds.

## Species, sites, and study context
- Species: Great Tit and Blue Tit; nest boxes used for data collection.
- Study woods and box details:
  - Monks Wood: 22–35 boxes over time (1993–2015); some box numbers do not exist (23–30 in Monks Wood).
  - Brampton Wood: 22 boxes (1993–2015); contains some dormouse boxes that may influence blue tits.
  - Wennington Wood: 21 boxes (1993–1999), then 35 boxes (2000–2015).
- Box accessibility varies by species due to hole sizes.

## Data collection and structure
- Data collection:
  - Boxes inspected roughly weekly during the laying period (late March onward).
  - First egg dates derived by counting days from observed eggs (one egg per day).
  - Only nests active at observation are included; only first clutches are recorded (replacements and second broods excluded).
- Data file:
  - Single Minitab Worksheet saved as CSV (Unicode).
  - File name: GTBTfirsteggdates.CSV; size: 42 KB.

- Data columns (Column definitions):
  1) Species code: 1 = Great Tit; 2 = Blue Tit
  2) Site: 1 = Monks Wood; 2 = Brampton Wood; 3 = Wennington Wood
  3) Year number: 1993 = Year 1; 1994 = Year 2; …; 2015 = Year 23
  4) Nest box identifier (note: Monks Wood boxes 23–30 do not exist)
  5) First egg date: April 1 = 1; March dates appear as negative values (3 negative values observed in Year 5)
  6) Sample size (N) for clutches included per year

## Quality control and data integrity
- Field data collected by trained personnel; egg dates cross-checked against original paper records.
- Data checks include: line/record counts, outlier checks, and validation of individual egg dates against yearly means per site.

## Usability, analysis opportunities, and considerations
- Enables longitudinal phenology analyses: species comparisons, site comparisons, and temporal trends (1993–2015).
- Aggregation possibilities: compute per-site per-year mean first egg dates; examine relationships with habitat factors or climate proxies.
- Important considerations:
  - Negative dates indicate March; most values cluster around March–April.
  - Variation in box availability and site structure over time must be accounted for in analyses.
  - Exclusion of replacement clutches and second broods limits scope to first-breeding events; box accessibility and hole-size differences may influence catch.