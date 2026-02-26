# Extent and tree species composition from a Scottish deciduous woodland survey, 1976-1979 Dataset Summary

- A dataset documenting the extent and species composition of Scotland’s deciduous woodlands (with some conifer admixture) surveyed between 1976 and 1979.
- Geographic coverage: Scotland; time period: 1976–1979.
- Data categories: woodland locations, canopy species percentage estimates, and related metadata.

## Overview and purpose

- Purpose of the survey:
  - Estimate extent and canopy species composition of deciduous woodlands, including admixture with conifers.
  - Determine distribution by species and administrative regions.
  - Compare 1976–79 extent with 1947 and 1965 censuses.
  - Provide floristic data for ecological classification and distribution mapping.
- Original outputs include maps and a final report describing woodland types and distributions.

## Survey design and methods

- Sample design:
  - Begin with a desk-based map search of OS 7th Series 1:63,360 maps for woods >5 ha labeled as deciduous.
  - Ground survey to confirm existence and determine canopy composition by species.
  - Mixed stands were included when possible; otherwise, exclusions/deflations applied as described.
- Field procedures:
  - Visual estimates of canopy composition, focusing on species forming the canopy; understorey recorded only if part of the canopy.
  - A canopy-based approach to ensure percentages sum plausibly to 100%.
  - Exclusion criteria: woods underplanted with conifers or in active felling were often marked “delete.”
  - Handling of exotics: separate recording for certain planted species; if exotics dominated (>50% canopy), many woods were deleted unless justified.
  - Mixed stands: detailed recording when exotics were ≤50%; otherwise treated as separate woods or deleted in some cases.
- Survey execution:
  - 1976: 926 woods inspected.
  - 1977: 1,913 woods surveyed by three teams.
  - 1978–1979: remaining woods completed; total surveyed woods = 3,744.
- Data creation and modification:
  - Field observations were converted into a structured database with per-woods canopy percentages and related attributes.
  - OS map boundaries and classifications used as starting points, but field checks led to revisions.

## Data structure and content

- For each wood (site), the dataset includes:
  - Location identifiers: map sheet, wood name, OS grid references (eastings/northings), and grid reference text.
  - Area in hectares and wood identifiers.
  - Canopy percentages for a wide range of species (e.g., Ash, Beech, Elm, Oak, Scots Pine, Hazel, Willow, Birch, Rowan, Sycamore, Hawthorn, Yew, etc.), plus total canopy percentage and associated counts.
  - Exotic species and conifer-related fields (EX, SP, O, etc.) and notes on data quality or peculiarities.
  - Remarks field for site-specific notes.
  - DEL_NOACCESS field indicating reasons for exclusion or non-use (e.g., wood no longer exists, inaccessible, no species data).
- Distribution outputs:
  - Maps illustrating canopy presence by species (e.g., Oak, Ash, Sycamore, Willow, Hazel, etc.).
- Data quality notes:
  - Field procedures included inter-observer checks and cross-validation with NCC surveys in some regions.
  - Boundaries and wood identifications were circulated for verification; some inconsistencies could remain due to historical data handling.

## Data quality, provenance, and governance

- Quality assurance:
  - Independent estimates among observers; internal consistency checks; cross-checks with Nature Conservancy Council surveys.
  - Boundary verification and name checks against NCC records.
- Provenance:
  - Original survey team: Bunce, Munro, Parr, Proctor (1970s).
  - Data rescue (2019–2024): transcription from original paper summaries and printouts; double-checked against final 1979 report data.
  - Handwritten-era data may contain transcription or naming errors; efforts made to reconcile with maps and historical documents.
- Data governance and sharing:
  - Raw OS-based maps and original data were used as the baseline; later data rescue aimed to preserve and share the dataset.
  - Researchers note that distributing underlying data can be a barrier in some contexts, reflecting broader governance considerations for public data sharing.

## Data rescue and availability

- Data rescue project (2019–2024) to digitize and curate the 1970s dataset from paper summaries and printouts.
- Verification steps:
  - Double-checking entered data against historical Bunce et al. (1979) outputs and Parr (1981) material where possible.
  - Acknowledgment of potential remaining discrepancies due to transcription and historic naming conventions.
  
## References and context

- Key sources:
  - Bunce, R.G.H., Munro, R.C., and Parr, T.W. 1979. Deciduous woodland survey of Scotland. Final report.
  - Parr, T.W. 1981. Scottish deciduous woodlands: a cause for concern? In Forest and woodland ecology: an account of research in ITE.
  - Shaw, M. W. & Bunce, R.G.H. 1971. National Woodlands Classification.
- Accessibility note:
  - Final report and related documents referenced for methodological details and validation; dataset entries in CSV include extensive metadata fields for traceability.