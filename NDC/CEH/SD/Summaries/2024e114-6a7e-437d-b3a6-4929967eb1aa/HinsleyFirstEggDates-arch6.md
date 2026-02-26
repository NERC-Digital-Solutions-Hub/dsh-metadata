# First egg dates for Great Tits and Blue Tits breeding in three deciduous woods in Cambridgeshire, England in 1993 to 2014.

## Overview
- Dataset documenting the timing of breeding (first egg dates) for Great Tits and Blue Tits across three Cambridgeshire deciduous woods from 1993 to 2014.
- Part of a long-term study on how habitat factors influence woodland bird abundance, distribution, and breeding success.

## Rationale
- Breeding timing is influenced by daylength, ambient temperature, and the phenology of main prey (tree-dwelling caterpillars), which themselves respond to temperature and tree bud burst.
- Timing of breeding serves as an indicator of spring phenology and climate warming.

## Study species and nest boxes
- Species: Great Tit (Parus major) and Blue Tit (Cyanistes caeruleus).
- Data collected from birds breeding in wooden nest boxes (approx. 110 x 130 x 200 mm) at 1–2 m height.
- Box availability and accessibility:
  - Boxes with 30–32 mm holes accessible to both species; ~25 mm holes accessible only to Blue Tits.
  - Most boxes accessible to both species except Wennington Wood, where some boxes are Blue Tit–exclusive.
- Box context:
  - Brampton Wood has dormouse boxes since the mid-1990s, likely increasing Blue Tit density there.
- Study Woods (sites, areas, and box counts):
  - Monks Wood National Nature Reserve (Site 1): 157 ha; 1993–2000: 22 boxes; 2001–2014: 35 boxes.
  - Brampton Wood (Site 2): 132 ha; 1993–2014: 22 boxes.
  - Wennington Wood (Site 3): 72 ha; 1993–1999: 21 boxes; 2000–2014: 35 boxes.
  - Box distribution and counts vary by site and over time; box numbers 23–30 do not exist in Monks Wood.

## Data collection and structure
- Data collection:
  - Boxes inspected approximately weekly during the laying period (from roughly the last week of March).
  - First egg dates estimated by counting backwards from observed eggs (one egg laid per day).
  - Only nests active at observation time (at least one more egg laid) are included.
  - Data reflect first breeding attempts only; replacement clutches and second broods are excluded.
- Data format:
  - Single Minitab worksheet saved as CSV (Unicode).
  - File name: GTBTfirsteggdates.CSV; file size: 39.4 KB.
- Column definitions:
  - Column 1: Species code (1 = Great Tit; 2 = Blue Tit).
  - Column 2: Site (1 = Monks Wood; 2 = Brampton Wood; 3 = Wennington Wood).
  - Column 3: Year (Year 1 = 1993; Year 22 = 2014).
  - Column 4: Nest box identifier (note: Monks Wood boxes 23–30 do not exist).
  - Column 5: First egg date (April 1 = 1). March dates appear as negative values; only three negative values in Year 5 (1997).
  - Column 6: Sample size (N) for the number of clutches included per year.

## Quality control
- Data collected by trained and experienced personnel.
- Egg dates cross-checked against original paper records.
- Line counts and data values checked for outliers.
- Individual egg dates validated against yearly site means.

## Uses and considerations for data support
- Enables analysis of breeding phenology as an indicator of spring onset and climate warming.
- Suitable for cross-site comparisons, long-term trend analysis, and linkage with habitat/landscape factors in the broader study.
- Clear coding for species, sites, and dates supports integration with other datasets and meta-analyses.

## Notes and limitations
- Dates with March occurrences are negative relative to April 1.
- Some boxes were added or removed over time (e.g., Wennington Wood box changes; Monks Wood box nonexistence for certain IDs).
- Dormouse boxes in Brampton Wood may influence Blue Tit abundance in that wood.