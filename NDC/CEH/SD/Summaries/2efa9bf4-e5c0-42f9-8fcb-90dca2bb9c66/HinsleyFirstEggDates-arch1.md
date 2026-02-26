# First egg dates for Great Tits and Blue Tits breeding in three deciduous woods in Cambridgeshire, England in 1993 to 2015.

## Overview
- Dataset captures first breeding attempt egg dates for Great Tit and Blue Tit across three Cambridgeshire deciduous woods from 1993 to 2015.
- Used as an indicator of spring phenology and climate warming; relates breeding timing to temperature and food phenology (caterpillar emergence).

## Study system and sites
- Species: Great Tit (Parus major); Blue Tit (Cyanistes caeruleus).
- Data collected from nests in wooden boxes (approx. 110 x 130 x 200 mm) at 1–2 m height.
- Box accessibility varies by species and site (hole sizes 30–32 mm for both; ~25 mm for Blue Tit only in some boxes).
- Study woods:
  - Monks Wood National Nature Reserve (Monks Wood; Site 1): 157 ha; box counts varied by period (1993–2000: 22; 2001–2008: 35; 2009–2015: 34).
  - Brampton Wood (Site 2): 132 ha; 22 boxes throughout 1993–2015.
  - Wennington Wood (Site 3): 72 ha; 21 boxes (1993–1999) expanding to 35 boxes (2000–2015).
- Habitat context: dominant trees include ash, oak, field maple; understory hawthorn, hazel, blackthorn; Brampton also includes conifers.

## Data collection
- Boxes inspected roughly weekly during the laying period (late March onward).
- First egg date derived by counting backwards from observed eggs (one egg per day).
- Only nests active at observation (at least one more egg expected) included.
- Data represent first breeding attempts; does not include replacement clutches or second broods.

## Data structure and variables
- File: GTBTfirsteggdates.CSV (Unicode CSV; 42 KB).
- Columns:
  1) Species code: 1 = Great Tit; 2 = Blue Tit
  2) Site: 1 = Monks Wood; 2 = Brampton Wood; 3 = Wennington Wood
  3) Year number: Year 1 = 1993 through Year 23 = 2015
  4) Nest box identifier (note: Monks Wood boxes 23–30 do not exist)
  5) First egg date: April 1 = 1; dates in March appear as negative values (only 3 negative values observed in Year 5)
  6) Sample size (N): number of clutches included per year

## Quality control
- Field data collected by trained personnel.
- Egg dates checked against original paper records; data lines and outliers checked.
- Individual egg dates validated against yearly site means.

## Usage considerations for analysts
- Suitable for modeling first egg date as a function of year, site, and box (to explore phenology trends and habitat effects).
- Can be used to compare inter-annual trends and spatial differences in breeding timing.
- Limitations: restricted to three woods in Cambridgeshire; only first clutches; box counts vary by site and year; occasional March dates (negative values) are rare.
- Data ready for import into analysis tools (e.g., R, Python) with accompanying metadata.