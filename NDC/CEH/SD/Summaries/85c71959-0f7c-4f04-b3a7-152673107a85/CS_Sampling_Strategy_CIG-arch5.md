# The Sampling Strategy for Countryside Survey (up to 2007)

## Overview for Data Stewards
- Documents the evolution of the ITE Land Classification and the sampling framework used to survey Countryside Survey field work from 1978 to 2007.
- Emphasizes the need for representative, stratified sampling and consistent data to support national and country-specific environmental reporting.
- Describes how classifications and sample allocations have been revised over time to improve accuracy, regional representation, and Wales/Scotland reporting.

## Core concepts and dataset structure
- Land Classification as sampling frame: environmental attributes (altitude, geology, climate, etc.) used to create Land Classes for stratified random sampling.
- Sample units: primarily 1 km squares; initial surveys used 1 km squares, with surrounding squares classified for context.
- Gradient of data: field survey data (habitat areas, land cover, vegetation, etc.) collected within selected squares; later estimates derived from class-level means and land area.
- National estimates: calculated by combining mean habitat area per square within a class with the total area of that class.
- Time-series linkage: methodology is tightly coupled to previous surveys to maintain comparability across years.

## Evolution by survey year

- 1978 – Initial Land Classification and first field survey
  - ISA (Indicator Species Analysis) used to form 32 land classes from environmental data across 1228 central 1 km squares.
  - Surrounding four squares added to each central square classification (total 6039 km squares classified).
  - Eight samples per land class (256 total squares) surveyed for habitat and vegetation.
  - National estimates derived from mean habitat area per square within each Land Class times the land area of that class.

- 1984 – Second GB land-use survey
  - Expanded framework: 12 squares surveyed per Land Class (total 384).
  - Used 1978 Land Classification for national estimates; enhanced focus on land-use and habitat mapping.

- 1990 – All Squares Land Classification and third field survey
  - Classification updated to include data from all 1 km squares in GB.
  - 508 squares surveyed; repetition of 1978 vegetation quadrats; urban and sea corrections incorporated.
  - Linked to first Land Cover Map of GB.

- 1998 – Revised Land Classification and fourth field survey
  - Land Classification expanded to support separate Scottish reporting; total classes increased to 40.
  - 569 squares surveyed; improved framework for national habitat estimates.
  - National reporting aligned with the revised classification; led to later England/Wales reporting needs (CS1990 results reused with updated framework).

- 2000 – Developments for Countryside Survey 2000
  - Aim to enable separate country estimates (England with Wales; Scotland) using only squares within the target country.
  - Sub-division of Land Classes into country-unit versions; aggregation of sparse country-class representations to maintain balance.
  - Added 19 (and then 11 additional) squares to ensure adequate representation of new classes; Wales sampling increased to support Wales-only reporting.
  - Introduction of upland habitat surveying module to strengthen England/Wales upland estimates.

- 2007 – Developments for Countryside Survey 2007
  - Wales-only reporting requirements led to further Welsh-class subdivisions (five new classes: 5w, 6w, 7w, 15w, 18w) increasing strata to 45.
  - Additional 43 squares surveyed in Wales for Wales representation; no equivalent English expansion in response.
  - England adjustments acknowledged: some classes remain with as few as four squares, but precision deemed acceptable based on scoping studies.
  - Final framework supports English, Welsh, and Scottish reporting with refined country-unit classifications and sampling rates.

## Sampling design and logistics
- Stratified random sampling to ensure representation of ecological variation across GB.
- Class-based allocation: squares allocated to Land Classes; the number of squares per class varied by survey and country reporting needs.
- Country-unit reporting: separate estimates prepared for England with Wales and Scotland; entails class sub-division, class aggregation where necessary, and targeted additional sampling in Wales and upland regions.
- Upland module: targeted sampling in uplands to improve accuracy of habitat estimates in English/Welsh uplands.

## Data governance implications for data stewards
- Provenance and versioning: each survey year updates Land Classification and sampling framework; maintain clear lineage and versioned metadata to support longitudinal analyses.
- Metadata requirements: document Land Class definitions, classification rules, and changes across years; capture the rationale for sub-divisions (e.g., country-unit classifications) and added squares.
- Data quality and comparability: note how changes in classification and sampling affect comparability of national estimates over time; provide guidance on translating estimates between classifications when needed.
- Cross-border data handling: maintain explicit separation of England, Wales, and Scotland estimates; ensure country-specific datasets reflect the correct class structure and sampling rates.
- Documentation and reproducibility: reference original methodological reports and subsequent CS2000/CS2007 adjustments; include figures and tables that map class maps and sampling grids.
- Data availability and governance: track access to class maps, square coordinates, and habitat estimates; manage embargoes or restrictions associated with country-specific reporting modules.

## Notable limitations and considerations
- Shifts in Land Classification across surveys affected sample representation and regional estimates; some classes became under-represented and required new squares.
- Wales reporting required more refined country-unit classes and increased Welsh sampling, impacting England-only precision in some classes.
- The report emphasizes the balance between statistical precision and practical surveying constraints, particularly for smaller classes and country-specific strata.

## Acknowledgements and references
- Acknowledges contributions from DETR, CEH, ITE, and researchers who developed and refined the Land Classification and sampling strategy.
- Provides a comprehensive bibliography for further reading on land classification, sampling strategies, and Countryside Survey results.