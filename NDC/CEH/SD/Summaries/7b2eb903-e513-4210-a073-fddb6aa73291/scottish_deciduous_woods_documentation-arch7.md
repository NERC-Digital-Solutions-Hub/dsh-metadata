# Extent and tree species composition from a Scottish deciduous woodland survey, 1976-1979 Dataset Summary

## Scope and Coverage
- Geographic area: Scotland
- Time period: 1976–1979
- Data type: Deciduous woodland locations and canopy percentages by tree species (including some admixture of conifers)

## Purpose and Original Design
- Primary aim: Estimate the extent and species composition of Scotland’s deciduous woodlands, including some conifer admixture
- Distribution: Map distribution by species and by regions relative to administrative boundaries
- Change over time: Compare 1976–79 figures with 1947 and 1965 censuses
- Classification: Provide ecological classification via intensive surveys of representative sites
- Output: Findings with types described and maps of their distribution
- Sample design: Census of woods marked on 7th Series OS maps at 1:63,360 scale
  - Minimum size: 5 ha (with allowances for mixed stands)
  - Ground truthing: Visual canopy composition estimates validated for reliability

## Methods and Procedures
- Field workflow: Identify woods on maps; determine existence and canopy species composition
- Survey scale and progress: 1976 (926 woods); 1977 (1,913 woods); 1978 (remainder); total woods surveyed = 3,744
- Canopy estimation approach: Visualize an aerial view focusing on canopy-forming species; understorey typically not recorded unless part of the canopy
- Data recording: Species percentages allocated from a compiled list, rounded in increments (e.g., 1%, 2%, etc.)
- Handling of gaps and deletions:
  - Uniform open canopy gaps ignored; if gaps >50% open, mark as delete
  - Woods underplanted with conifers, recently felled, or in felled state marked delete
- Exotic species: Planted species recorded separately; exotics >50% canopy may lead to delete; coherent conifer/broadleaf blocks treated separately
- Additional notes: Woods seen but not on OS maps recorded; some woods marked on maps but without a symbol inspected

## Data Structure and Content
- Primary dataset: ScottishDecWoods_1976_79.csv
- Key fields per wood:
  - Location: Site_Sheet (map sheet), Easting, Northing, OS_GridRef
  - Identification: Number (wood identifier), Name
  - Area: Area_ha (hectares)
  - Canopy composition: percentages for multiple species (e.g., Ash, Beech, Elm, Exotics, Scots Pine, Hazel, Oak, Willow, Alder, Birch, Rowan, Willow, Aspen, Cherry, Lime, Blackthorn, Hawthorn, Holly, Yew, Poplar, etc.)
  - Totals: Total canopy percentage
  - Remarks: Text notes
  - DEL_NOACCESS: flags indicating deletion or inaccessible status (e.g., wood no longer exists, inaccessible, no species data)
- Mapping outputs: Species-specific distribution maps (e.g., Hawthorn, Hazel, Oak, Sycamore, Willow, Alder, Ash, Aspen, Beech, Cherry)

## Data Quality, Validation and Rescue
- Quality controls: Field procedures developed by J.E.A. Proctor; inter-observer checks; cross-validation with NCC surveys; boundary verifications
- Validation: Spot checks against field data and cross-referencing with Nature Conservancy Council work
- Data rescue (2019–2024): Digitization from original paper summaries and printouts; double-checked against final 1979 report data
- Potential issues:
  - Handwriting interpretation may introduce site name errors
  - Some discrepancies possible when reconciling with historical reports due to changes in administrative boundaries
  - Baseline maps (OS) updated at unknown revision dates; not a strict baseline

## Access, References and Documentation
- Data availability: UKCEH Archive
- Primary sources:
  - Bunce, Munro, Parr (1979). Deciduous woodland survey of Scotland. Final report
  - Parr (1981). Scottish deciduous woodlands: a cause for concern?
  - Shaw & Bunce (1971). National Woodlands Classification (method handbook)
- Related notes: Data rescue and validation conducted to align newly entered data with historic publications where possible

## Use in GIS and Spatial Analysis
- Spatial data are provided as precise grid references (OS grid) and coordinates suitable for GIS mapping
- Useful for:
  - Creating map-based representations of canopy composition by species
  - Analyzing spatial distribution of deciduous woodlands across Scotland
  - Integrating with other ecological or administrative boundary datasets
- Limitations to consider:
  - Some woods were deleted or excluded due to underplanting, felled status, or high exotic dominance
  - Not all small woods (<5 ha) or non-canopy species data are included
  - Historical baseline and possible data entry errors may affect exact site names and coordinates

## Acknowledgements
- 1970s survey team: Bunce, Munro, Parr, Proctor
- Data rescue and management (2019–2024): Wood, Dodd, Balmer, Walker, Draycott, Wright