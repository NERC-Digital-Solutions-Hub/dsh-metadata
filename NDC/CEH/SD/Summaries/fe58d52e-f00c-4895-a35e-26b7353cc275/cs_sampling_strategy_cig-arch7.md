# The Sampling Strategy for Countryside Survey (up to 2007)

- An historical overview of how the ITE Land Classification underpins the Countryside Survey sampling framework from 1978 to 2007.
- Central idea: stratified random sampling using a land classification to ensure representative coverage of Great Britain’s ecological variation.
- Purpose of the strategy: to derive national and country-level habitat estimates from field surveys by mapping sampling across land classes.

## Core concepts for GIS work

- Land Classification as the sampling scaffold:
  - Classifies land into discrete environmental strata (land classes) used to select survey squares.
  - Enables estimation of habitat areas by combining the mean habitat area per class with the class’s total land area.
- Sampling units and adaptation over time:
  - Primary unit: 1 km x 1 km squares; core of the stratified framework.
  - Survey work historically focused on central squares (and surrounding context squares) to calibrate class boundaries.
- Time-series data needs:
  - Class definitions and the spatial distribution of squares changed across surveys, affecting comparability and requiring careful handling in GIS analyses.

## Chronology of developments

- 1978 (Initial Land Classification and first field survey)
  - ISA-based classification produced 32 Land Classes from 1228 centre 1 km squares; surrounding four squares also classified.
  - Final sampling: 256 field squares (8 per class) across GB.
  - National estimates calculated as mean habitat per class times the area of that class.
- 1984 (Second GB land-use survey)
  - Framework reused; increased sample size to 12 squares per class (384 total); eight squares per class pre-1984 still revisited.
  - Estimates reported using the 1978 Land Classification.
- 1990 (CS1990; All Squares Land Classification)
  - Expanded to classify every GB 1 km square; 508 squares surveyed.
  - Linked to the first Land Cover Map of GB; additional fields repeated from CS1984.
  - National estimates based on the revised, GB-wide classification framework.
- 1998 (Revised Land Classification; CS1990 refinement)
  - GB-wide classification updated to 40 Land Classes; enabled Scotland-only reporting.
  - Field survey increased to 569 squares; implications for regional estimates.
- 2000 (CS2000; separate country estimates)
  - Motivation: policy needs for England, Scotland, and Wales to have reliable country-level estimates.
  - Implemented country-unit versions of Land Classes (40 strata expanded to 45 in practice) and aggregation where necessary.
  - Additional squares added to ensure adequate representation; upland habitat module added (30 upland squares) to boost upland estimate precision.
  - Wales became the most intensively sampled country; Isle of Man squares removed from country-unit estimates.
- 2007 (CS2007; Wales-focused reporting)
  - Wales-only reporting requirements led to further Wales-specific sub-division of Land Classes (five new Wales-only classes: 5w, 6w, 7w, 15w, 18w).
  - 43 additional Welsh squares added; minimum of 6 squares per Welsh class.
  - England saw limited additions in two classes (5e, 15e) capped at 4 squares per class to maintain precision assumptions.
  - Resulting framework: 45 strata for Wales/England mix; revised class maps for England with Wales and Scotland.

## Data products and outputs

- Land Classification maps (for each survey version) and class descriptions.
- Tables and figures documenting sample square distributions:
  - Table 2 (CS1990): distribution of squares by class.
  - Table 3 (CS2007): distribution of squares by class and country units.
  - Table 4: number of squares per class under the original 1990 Land Classification across CS1978, CS1984, CS1990, CS2000, CS2007.
- Visuals:
  - Figure 1: original ITE Land Classification map (1978).
  - Figure 2–3: sample square maps and reclassifications across surveys.
  - Figure 4–6: revised Land Classification maps for England with Wales, Scotland, and Wales-specific sampling frameworks; maps of sample squares.
- Output considerations:
  - National estimates depend on the chosen classification version; consistency considerations are discussed for cross-survey comparability.

## National estimates and cross-survey consistency

- Changing the fundamental Land Classification used for national estimates can affect stock estimates.
- The preferred approach for CS2007 onward is to use the latest country-specific classification for country estimates, while the older classification can be used for cross-survey consistency.
- Table 4 demonstrates sample sizes per class across surveys under the Original (1990) Land Classification.

## Practical implications for GIS specialists

- Time-series alignment:
  - Must account for reclassification and country-unit subdivisions when integrating data across CS1978–CS2007.
- Class management:
  - Retain awareness of 32, 40, and 45-class configurations and their geographic extents per survey.
- Spatial analyses:
  - Use Land Class as a stable stratification basis for habitat-area estimation, but normalize or transform when comparing across surveys with different classifications.
- Upland and country-specific modules:
  - Incorporate upland module data (CS2000) and Wales/England/Scotland distinctions for accurate, policy-relevant outputs.

## Acknowledgements and references

- Acknowledgements and further reading sections detail contributors, statistical guidance, and bibliographic sources for deeper methodological context.