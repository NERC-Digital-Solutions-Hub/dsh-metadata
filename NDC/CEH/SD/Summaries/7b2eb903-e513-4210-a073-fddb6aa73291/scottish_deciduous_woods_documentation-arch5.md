# Extent and tree species composition from a Scottish deciduous woodland survey, 1976-1979 Dataset Summary

## Overview
- Dataset documenting the extent and canopy species composition of Scotland’s deciduous woodlands (with some conifer admixture) surveyed from 1976 to 1979.
- Based on a desk-based OS map search (7th Series 1:63,360) followed by ground-truth checks.
- Aims to estimate extent, determine distribution by species/region, compare with 1947 and 1965 censuses, and provide ecological classification and maps.

## Dataset Scope and Content
- Geographic coverage: Scotland; time period: 1976–1979.
- Data categories: woodland locations and canopy percentages by tree species.
- Survey scale: census of deciduous woodlands >5 ha identified on OS maps; mixed stands recorded with rules for exotics and deletions.
- Output: a CSV file (ScottishDecWoods_1976_79.csv) with per-wood records including location, area, canopy composition, and status notes.
- Example data fields include: site sheet, wood identifier, name, Easting/Northing, OS Grid Reference, Area (ha), canopy percentages for multiple species (e.g., Ash, Beech, Oak, Scots Pine, Oak, Birch, Sycamore, Willow, exotics, etc.), total canopy, remarks, and a DEL_NOACCESS flag.

## Survey Design & Methods
- Original purpose: quantify extent, distribution by species/regions, and ecological classification; compare with earlier censuses; produce distribution maps.
- Sample design: map-based identification of woods >5 ha; ground survey to estimate canopy composition by dominant species.
- Teams and effort: 1976 (926 woods), 1977 (1,913 woods), 1978–1979 (remainder); total woods surveyed: 3,744.
- Canopy estimation rules:
  - Only canopy species recorded; understorey not included unless part of the canopy.
  - Exotics recorded separately; if exotics >50% canopy, wood often marked "delete" unless justified.
  - Mixed blocks of conifers and broadleaves treated as separate woods or deletions, depending on dominance.
  - Gaps ignored if uniformly scattered; extensive gaps (>50%) may lead to deletion from the record.
  - Recently underplanted or felled stands may be deleted.
- Data integrity considerations:
  - Boundaries and canopy estimates checked among observers; cross-checks with NCC surveys.
  - OS map revisions used as starting points; not treated as a fixed baseline.

## Data Content and Structure
- Data file: ScottishDecWoods_1976_79.csv.
- Key fields:
  - Location: Site_Sheet, Easting, Northing, OS_GridRef, Area_ha.
  - Identification: Number (wood ID), Name.
  - Canopy composition: percentages for multiple species (e.g., Ash, Beech, Elm, Oak, Scots Pine, Alder, Birch, Rowan, Willow, Aspen, Cherry, Lime, Hawthorn, Hazel, Holly, Yew, Poplar, etc.) plus Total canopy.
  - Exotics: EX and related notes; inclusion/exclusion decisions ("delete" or not).
  - Remarks: free-text notes.
  - DEL_NOACCESS: status flag describing reasons for exclusion or inaccessibility (e.g., wood no longer exists, inaccessible, no species data).
- Maps: supplementary distribution maps show wood presence by species (e.g., Oak, Ash, Sycamore, Hazel, etc.).

## Data Quality, Limitations, and Documentation
- Data quality: systematic field checks and inter-observer comparisons; corroboration with NCC surveys; boundary standardization checks.
- Limitations and caveats:
  - Potential transcription errors from handwriting; data rescue (2019–2024) aimed to recover from paper/printouts, with some residual name/grid-reference errors possible.
  - Some woods under 5 ha were inconsistently included due to differing rules over time.
  - Certain data not collected (e.g., woods <5 ha, riverine patches, scrub not mapped as woodland, non-canopy species, age/regeneration status).
  - OS maps used as starting points; not a strict baseline; revisions/changes post-1954–1967 data uncertain.
  - Gaps in canopy data or discrepancies may exist due to historical data recording practices.

## Data Rescue and Accessibility
- Data rescue performed 2019–2024 to re-enter data from original sheets and printouts; cross-validated against the 1979 final report.
- Post-rescue checks compared with Bunce et al. (1978) and Parr (1981) where feasible; significant discrepancies addressed.
- Acknowledges potential residual errors in site names and locations due to transcription.

## Acknowledgements and References
- Management and analysis (1970s): Bunce, Munro, Parr, Procter.
- Data entry/management (2019–2024): Wood, Dodd, Balmer, Walker, Draycott, Wright; additional support noted.
- References: Bunce et al. (1979) Final Report; Parr (1981); Shaw & Bunce (1971).

## Governance, Use, and Stewardship Implications
- Large-scale, multi-year woodland dataset with rich metadata and explicit data handling rules.
- Demonstrates robust quality checks, provenance, and alignment with historical surveys.
- Useful for data discovery, governance of historic forestry datasets, and future updates or reconciliations, with clear notes on limitations and data rescue provenance.