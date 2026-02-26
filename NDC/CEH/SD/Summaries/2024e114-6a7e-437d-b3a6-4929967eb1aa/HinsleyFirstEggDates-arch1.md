# First egg dates for Great Tits and Blue Tits breeding in three deciduous woods in Cambridgeshire, England in 1993 to 2014.

## Overview
- Purpose: Use breeding timing in Great Tits and Blue Tits as a measure of spring phenology and climate warming, linked to temperature and prey (caterpillar) phenology.
- Context: Part of a long-term study on how habitat, landscape factors, and climate influence woodland bird abundance, distribution, and breeding success in English lowland deciduous woodland.
- Outcome: Provides first-egg dates to analyze temporal and spatial patterns in breeding timing.

## Study species and boxes
- Species: Great Tit (Parus major) and Blue Tit (Cyanistes caeruleus).
- Nest boxes: Wooden boxes (approx. 110 x 130 x 200 mm) used at 1–2 m height; low box density to minimize population impact.
- Access controls: Box hole sizes determine which species can use a box (30–32 mm accessible to both; ~25 mm for Blue Tits only); in Wennington Wood most boxes are accessible to both; some boxes added after 2000.

## Study sites
- Cambridgeshire, eastern England; three deciduous woods:
  - Monks Wood National Nature Reserve (Site 1)
    - Area: 157 ha
    - 1993-2000: 22 boxes; 2001-2014: 35 boxes
  - Brampton Wood (Site 2)
    - Area: 132 ha
    - 1993-2014: 22 boxes
  - Wennington Wood (Site 3)
    - Area: 72 ha
    - 1993-1999: 21 boxes; 2000-2014: 35 boxes
- Principal tree species: Ash, oak, field maple; understory includes hawthorn, hazel, blackthorn; Brampton Wood contains conifer blocks that do not house the boxes.

## Data collection
- Frequency: Boxes inspected approximately weekly during the laying period (from late March).
- Measurement: First egg date is inferred from counting backward from observed eggs (assuming one egg per day); eggs usually laid early morning; boxes inspected after the day’s egg is laid.
- Inclusion criteria: Only nests active at the time of observation (at least one more egg to come) and only first breeding attempts are included (no replacement clutches or second broods).

## Data structure and format
- File: GTBTfirsteggdates.CSV (Unicode CSV), 39.4 KB.
- Columns:
  1) Species code: 1 = Great Tit; 2 = Blue Tit
  2) Site: 1 = Monks Wood; 2 = Brampton Wood; 3 = Wennington Wood
  3) Year number: 1993 = Year 1 through 2014 = Year 22
  4) Nest box identifier (note: Monks Wood boxes 23–30 do not exist)
  5) First egg date: April 1 = 1; March dates appear as negative values (3 negative values, all in Year 5, 1997)
  6) Sample size (N) for clutches included per year

## Quality control
- Data collected by trained personnel; egg dates checked against original paper records.
- Data lines and values checked for outliers; egg dates validated against yearly means per site.

## Usage notes and context
- The dataset enables analysis of spring phenology and its relation to climate variables (e.g., temperature, bud burst) and habitat factors.
- Useful for cross-site comparisons and long-term trend analysis of breeding timing in relation to environmental change.
- Provides a local, box-based, multi-site view with explicit data on first breeding attempt timing across 22 years.