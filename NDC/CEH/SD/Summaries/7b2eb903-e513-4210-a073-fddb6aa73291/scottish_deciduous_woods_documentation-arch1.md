# Extent and tree species composition from a Scottish deciduous woodland survey, 1976-1979 Dataset Summary

- Scope and aims
  - Census of deciduous woodlands in Scotland (1976–1979), including some admixture of conifers.
  - Objectives: estimate extent, canopy species composition, distribution by region/admin boundaries, and provide ecological classification data.
  - Ground-truthing followed desk-based map search using OS 1:63,360 maps (7th Series); field estimates recorded canopy composition.

- Geographic and temporal coverage
  - Area: Scotland
  - Time period: 1976–1979
  - Surveyed 3,744 woods in total (1976: 926 woods; 1977: 1,913 woods; 1978–1979: remainder)

- Survey design and methods
  - Initial step: identify woods >5 ha on OS maps; mixed stands included due to difficulty estimating composition.
  - Field methods: visual estimation of canopy species composition, focusing on species forming the canopy; understorey not recorded unless part of the canopy.
  - Canopy estimation process: compile a species list for each wood, assign percentages from 1% increments, adjust to ensure consistency with the overall canopy.
  - Boundaries and status: used map boundaries (OS) as a starting point; certain woods deleted from records if gaps >50% or conifer underplanting/being felled.
  - Exotics and mixtures: exotics recorded separately; woods with >50% exotics marked delete; coherent blocks of mixed conifers/broadleafs treated as separate woods or deleted depending on context.
  - Data included both woods seen on maps but not marked, and woods on maps without tree symbols when appropriate.

- Data content and structure
  - For each wood: 
    - Identifiers: Site_Sheet (map sheet), Number (wood ID), Name (wood/neighbouring feature)
    - Location: Easting, Northing, OS_GridRef, Area_ha
    - Canopy composition: percentages for multiple species (Ash, Beech, Elm, Exotics, Sycamore, Whitebeam, Alder, Birch, Rowan, Willow, Aspen, Scots Pine, Hazel, Holly, Oak, Other, Cherry, Lime, Blackthorn, Hawthorn, Yew, Poplar, Total)
    - Additional fields: Remarks, DEL_NOACCESS flag (indicating delete, inaccessible, or no data)
  - Data file: ScottishDecWoods_1976_79.csv
  - Maps: distribution maps for key species (e.g., Oak, Ash, Sycamore, etc.)
  - Data content notes: 
    - Exotics recorded separately; mixed stands with ≤50% exotics detailed; >50% exotics typically deleted unless locally justified.
    - Area and canopy totals anchored to a wood-level assessment; gaps in canopy ignored if evenly scattered; large open gaps >50% lead to deletion.
    - Original surveys did not consistently define “wood” vs. “scrub”; inclusive approach adopted.

- Data quality and validation
  - Consistency checks: independent estimates by team members, cross-checks among observers.
  - External validation: broad survey in Dumfries and Galloway by NCC with similar methods; close correspondence found.
  - Spot checks of database against field observations; boundary verification among staff.
  - Data rescue (2019–2024) to recover 1970s digital database from paper summaries and printouts; double-entry verification against final 1979 report data.
  - Limitations: potential errors in site names and grid references due to handwriting; some discrepancies may remain after rescue; OS map revision dates and sources not fully known; exact administrative boundary alignment may differ from historical reports.

- Data rescue, provenance, and references
  - Data entry conducted 2019–2024; sources include original paper summaries, computer printouts, and UKCEH Archive materials.
  - Cross-comparisons performed with Bunce et al. (1979) final report and Parr (1981) outputs; major discrepancies investigated and rectified where possible.
  - Key references: Bunce, Munro & Parr (1979) Final Report; Parr (1981) Scottish deciduous woodlands; related field methods (Shaw & Bunce, 1971).

- Usage considerations and caveats
  - Historic dataset with methodological nuances (canopy-only focus, exclusion of understorey, delete rules for certain changes).
  - Not all forest types or non-canopy species are captured; some data gaps noted (e.g., small woods under 5 ha, riverine gullies, scrub not mapped as wood).
  - Users should account for potential postcode/administrative boundary shifts and potential minor data transcription errors from handwriting-to-digital conversion.

- Acknowledgements and sources
  - Original survey management and analysis (1970s): Bunce, Munro, Parr, Proctor
  - Data entry and management (2019–2024): Wood, Dodd, Balmer, Walker, Draycott, Wright
  - Supporting references: Bunce et al. 1979; Parr 1981; Shaw & Bunce 1971