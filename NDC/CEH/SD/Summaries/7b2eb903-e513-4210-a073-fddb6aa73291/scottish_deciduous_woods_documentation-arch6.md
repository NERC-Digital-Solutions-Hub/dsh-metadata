# Extent and tree species composition from a Scottish deciduous woodland survey, 1976-1979 Dataset Summary

## Overview
- A census of Scotland’s deciduous woodlands (including some admixture of conifers) to estimate extent and canopy species composition.
- Combined desk-based OS map search with ground-truthing to map woodland extent and quantify canopy by species.

## Geographic and Temporal Coverage
- Geographic scope: Scotland
- Time period: 1976–1979
- Data category: Location of deciduous woodlands and canopy percentage by species

## Survey Design and Methods
- Source material: 7th Series OS maps at 1:63,360; woods over 5 ha were targeted; mixed stands included due to difficulty in estimating composition.
- Ground survey: Determine existence of each wood and canopy species composition.
- Total woods surveyed: 3744 (1976: 926; 1977: 1913; 1978–1979: remainder)
- Canopy estimation: Visual, focusing on canopy-forming species; understorey not systematically recorded unless part of the canopy.
- Data rules and adjustments:
  - Canopy percentages compiled for each wood, adjustments made to ensure totals are coherent.
  - Gaps in canopy ignored if uniform open canopy; if gaps >50%, wood deleted from record.
  - Woods recently underplanted, or being felled, marked "delete" in most cases.
  - Exotics (planted) treated separately; if exotics >50% canopy, wood often deleted; mixed blocks handled by separating conifer/broadleaf areas.
- Data mapping: Distributions created for key species (e.g., Hawthorn, Hazel, Oak, Sycamore, Willow, Alder, Ash, Beech, Elm, Scots Pine, etc.).

## Data Structure and Content
- Per-wood data fields include:
  - Location: map sheet, wood name, Easting/Northing, OS Grid reference
  - Area: Area_ha (hectares)
  - Canopy percentages by species (e.g., Ash, Beech, Elm, Exotics, Sycamore, Willow, Ash, etc.)
  - Totals: Total canopy percentage
  - Remarks: free text notes
  - DEL_NOACCESS flag: reasons for excluding or not surveying a site
- Species coverage and corresponding map representations are provided for major species such as Oak, Ash, Hawthorn, Hazel, Birch, Rowan, Willow, Beech, Cherry, Lime, Yew, Pine, and others.

## Data Quality and Validation
- Field procedures developed by J.E.A. Proctor; cross-observer checks to ensure consistency.
- Comparisons with Nature Conservancy Council (NCC) surveys showed broad agreement in wood selection.
- Field checks against the data bank and boundary verifications were used to minimize discrepancies.
- Data reconciliation and name checks circulated among NCC staff.

## Data Rescue and Provenance
- Data entry conducted 2019–2024 as part of a data rescue effort; original digital database was not usable.
- Data entered from original paper summaries and printouts; double-checked against final 1979 report data.
- Handwriting and naming may introduce some errors; site locations checked for obvious discrepancies (e.g., marine locations).
- Summaries compared with Bunce et al. (1978) and Parr (1981) where possible; major discrepancies rectified.

## Availability and Limitations
- Main dataset: ScottishDecWoods_1976_79.csv includes per-wood canopy data and metadata.
- Notable data gaps:
  - Woods smaller than 5 ha are excluded or inconsistently treated.
  - Riverine/gully patches not distinct woods may be missing.
  - Scrub not colored green on OS maps and non-canopy species are not systematically captured.
  - Data on wood age, regeneration, or non-canopy woody components are not collected.
- Caution in interpreting OS map backdrops: OS map revision dates (1954–1967) are not known; maps served as a starting point rather than a strict baseline.

## Outputs and Visualizations
- Maps available showing species distributions (e.g., Hawthorn, Hazel, Oak, Sycamore, Willow, Alder, Ash, Beech, Aspen, Birch, Cherry, Rowan, etc.).
- Data rescued to enable re-analysis and comparison with historical reports.

## Acknowledgements
- 1970s survey: Bunce, Munro, Parr, Procter
- Data entry/management (2019–2024): Wood, Dodd, Balmer, Walker, Draycott, Wright
- Additional 1970s support as detailed in Bunce et al. (1979)

## References and Further Reading
- Bunce, R.G.H., Munro, R.C., and Parr, T.W. 1979. Deciduous woodland survey of Scotland. Final report.
- Parr, T.W. 1981. Scottish deciduous woodlands: a cause for concern?
- Shaw, M. W. & Bunce, R.G.H. (1971) National Woodlands Classification.