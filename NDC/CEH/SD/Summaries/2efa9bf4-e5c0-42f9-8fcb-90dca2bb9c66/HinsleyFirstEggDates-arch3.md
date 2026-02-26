# First egg dates for Great Tits and Blue Tits breeding in three deciduous woods in Cambridgeshire, England in 1993 to 2015.

## Overview
- Long-term dataset measuring first egg dates as an indicator of spring phenology and climate warming.
- Part of a broader, ongoing study examining how habitat, landscape structure, and composition influence abundance, distribution, and breeding success of woodland birds in English lowland deciduous woodland.

## Study species and sites
- Species: Great Tit (Parus major); Blue Tit (Cyanistes caeruleus).
- Study woods in Cambridgeshire, eastern England:
  - Monks Wood National Nature Reserve (52°24'N, 0°14'W; 157 ha): 1993-2000 (22 boxes); 2001-2008 (35 boxes); 2009-2015 (34 boxes).
  - Brampton Wood Wildlife Trust Nature Reserve (52°19'N, 0°16'W; 132 ha): 1993-2015 (22 boxes).
  - Wennington Wood (private woodland) (52°23'N, 0°10'W; 72 ha): 1993-1999 (21 boxes); 2000-2015 (35 boxes).
- Box setup:
  - Nest boxes used for tit nesting, with access controlled by hole size (30–32 mm for both species; ~25 mm for Blue Tits only).
  - Boxes distributed at low density to minimize population impact; Brampton Wood includes ~200 dormouse boxes since mid-1990s, increasing Blue Tit availability in that wood.
- Habitat context: deciduous woodland dominated by common ash, English oak, and field maple; understory includes hawthorn, hazel, and blackthorn; conifer blocks present in Brampton Wood.

## Data collection and scope
- Data collection window: approximately weekly inspections during the laying period (from late March).
- Primary measure: date of first egg in the clutch (eggs laid at about one per day; dates inferred by counting backward from observed eggs).
- Inclusion criteria: only active nests (at least one more egg expected); only first breeding attempts included (replacements and second broods excluded).
- Longitudinal span: 1993–2015 across all three sites.

## Data structure and format
- File: GTBTfirsteggdates.CSV (Unicode CSV; 42 KB); originally a Minitab worksheet (Release 16) saved as CSV.
- Columns:
  - Column 1: Species code (1 = Great Tit; 2 = Blue Tit).
  - Column 2: Site (1 = Monks Wood; 2 = Brampton Wood; 3 = Wennington Wood).
  - Column 3: Year number (Year 1 = 1993; Year 23 = 2015).
  - Column 4: Nest box identifier (note: Monks Wood boxes 23–30 do not exist).
  - Column 5: First egg date (April 1 = 1; March dates appear as negative values; three negative values observed in Year 5, 1997).
  - Column 6: Sample size (N) representing the number of clutches included per year.

## Quality control and data integrity
- Data collected by trained, experienced personnel.
- Egg dates checked against original paper records.
- Data lines counted and values checked for outliers.
- Individual egg dates cross-verified against yearly mean values per site.

## Data usage and governance notes
- Data designed to support analyses of spring phenology and climate-related breeding timing across sites and years.
- The dataset reflects rigorous field verification and quality control, with a clear structure for cross-site, cross-year comparisons.
- Metadata and accessibility considerations (e.g., public sharing and data governance) are noted in the surrounding context of data sharing and standards, emphasizing data quality and provenance.