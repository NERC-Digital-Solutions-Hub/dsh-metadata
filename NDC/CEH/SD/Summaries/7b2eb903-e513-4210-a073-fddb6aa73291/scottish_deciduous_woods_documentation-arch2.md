# Extent and tree species composition from a Scottish deciduous woodland survey, 1976-1979 Dataset Summary

- Overview
  - Purpose: to estimate the extent and species composition of Scotland’s deciduous woodlands (including some conifer admixture) and to relate distribution to administrative regions.
  - Timeframe and geography: Scotland, 1976–1979.
  - Data categories: woodland locations and canopy species percentage cover estimations; includes maps illustrating species distribution.
  - Approach: desk-based map search (OS 7th Series 1:63,360) followed by ground-truthing; canopy visually estimated to reflect dominant canopy species only.

- Dataset contents and structure
  - Per-wood data (ScottishDecWoods_1976_79.csv): 
    - identifiers and location: map sheet, wood ID, wood name; Easting, Northing, OS Grid Reference; area in hectares.
    - canopy composition: percentage cover by numerous species groups (e.g., Ash, Beech, Elm, Oak, Birch, Hazel, Willow, Yew, Rowan, Sycamore, Scots Pine, Aspen, Hawthorn, Cherry, Lime, Blackthorn, Holly, Oak, Alder, Alder-related categories, Exotics, Total canopy).
    - fields for remarks and deletion status (e.g., DELETE for woods no longer woodland; INACCESSIBLE; NO SP DATA).
  - Outputs: distribution maps by key species (e.g., Oak, Ash, Sycamore, Hazel, Hazel, Hawthorn, Willow, Rowan, Beech, Ash, Aspen, Birch, etc.).
  - Data rescue and provenance: original field sheets and printouts, re-entered 2019–2024; cross-checks against final 1979 report; potential name/grid-reference errors acknowledged.

- Survey design and methods
  - Original purpose (summarized): quantify extent, distribution by region/species, compare with 1947/1965 censuses, provide floristic data for ecological classification, and map distribution types.
  - Sampling design: census of woods marked as deciduous on OS maps; minimum 5 ha threshold used initially; mixed stands included when possible.
  - Field survey approach: ground surveys (1976–1979) with canopy estimates based on visual interpretation of an aerial view; only canopy-dominant species recorded to ensure totals stay within 100%.
  - Handling of peculiar cases:
    - Gaps in canopy: ignored if uniform open canopy; deletions if gaps exceed ~50% or if destruction/underplanting occurred.
    - Exotics and mixtures: woods with up to 50% exotics recorded in detail; >50% exotics generally marked DELETE; coherent conifer/broadleaf blocks treated as separate woods.
    - Underplanted/undergoing felling: often marked DELETE unless justified to retain; recently felled stands likewise.
  - Boundary and data consistency: efforts to verify boundaries and names across NCC and internal checks.

- Data quality, limitations, and caveats
  - Quality controls: independent estimates among observers; cross-checks with NCC surveys in Dumfries and Galloway; boundary verification with NCC; field-based spot checks.
  - Limitations and potential errors: OS map revision dates before 1957–1967 not exactly baseline; transcription handwriting may introduce name/grid-reference errors; some Woods under 5 ha or in inaccessible areas may be missing or inconsistently included; non-canopy data (age, regeneration, non-canopy species) not collected.

- Data accessibility, usage, and outputs
  - Primary data file: ScottishDecWoods_1976_79.csv (per-wood canopy and site attributes).
  - Maps: species-distribution maps (e.g., Hawthorn, Hazel, Oak, Sycamore, Willow, Alder, Ash, Aspen, Beech, Birch, Cherry, Rowan).
  - Reports and context: Final survey report Bunce et al. (1979); related publications Parr (1981); additional methodological notes (Shaw & Bunce, 1971).
  - Documentation and data rescue: 2019–2024 data rescue to preserve and re-enter historic data; data were double-checked against original summaries and later publications.
  - Acknowledgements: survey leadership and data-entry teams from 1970s and 2019–2024 teams.

- Practical relevance for environmental monitoring analysts
  - Enables tracking of woodland extent and canopy composition over time at a national scale.
  - Provides standardized, reproducible canopy data by species for broad-scale monitoring and ecological classification.
  - Suitable for integration with other environmental datasets to enhance data value beyond single-use analyses.
  - Highlights data quality practices (cross-checks, boundary verification, and data rescue) relevant to ongoing monitoring data stewardship.