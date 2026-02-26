# The Sampling Strategy for Countryside Survey (up to 2007)

- Overview
  - Documents the evolution of the ITE Land Classification and its use as the sampling framework for Countryside Survey field surveys from 1978 to 2007.
  - Emphasises that the current methodology is deeply linked to its historical predecessors and aims to understand how past decisions shape present and future sampling.

- Core concepts for GIS-focused work
  - Stratified sampling: uses stratification to ensure representative coverage across Britain, reducing bias associated with pure random sampling.
  - Land Classification as stratification: environmental attributes (altitude, geology, climate, etc.) define land classes that guide sample selection and habitat estimation.
  - 1 km square sampling unit: base unit for field surveys, with larger-scale stratification tied to the 1 km squares.
  - Spatial mapping: Land Classification maps serve as the spatial framework for both sampling and estimation of habitat areas.

- Development timeline and key methodological milestones
  - 1978 (Initial Land Classification and first field survey)
    - ISA (Indicator Species Analysis) used on environmental attributes to create 32 land classes from 1228 central 1 km squares; surrounding four squares per center also classified.
    - Final sampling: eight samples per class (256 squares total) for national estimates of habitat areas.
    - Outputs fed into early landscape/habitat estimation efforts.
  - 1984 (Second GB land use survey)
    - Expanded sampling to 12 squares per land class (total 384) while still rooted in the 1978 Land Classification.
  - 1990 (All Squares land classification and third field survey)
    - Land Classification updated to incorporate data from all GB 1 km squares; urban and sea corrections applied.
    - 508 squares surveyed; included repeat of 1978 vegetation quadrats.
    - Introduction of the first Land Cover Map of GB derived from satellite imagery; national estimates still tied to the 1990 classification.
    - Result: some squares changed class; 62% correspondence with the prior classification.
  - 1998–2000 (Developments for CS2000)
    - Need for country-specific estimates (England & Wales; Scotland) led to extending the Land Classification and refining sampling for separate country reporting.
    - Sub-division of Land Classes into country-unit versions; eventual creation of 40 strata.
    - Additional samples added to ensure representation of new classes in each country; Wales gained particular focus to support Wales-only reporting.
    - Uplands module introduced to improve accuracy of upland habitat estimates in England and Wales.
  - 2007 (Developments for CS2007)
    - Wales-only reporting requirements driven further; Wales received more intensive sampling relative to England/Scotland.
    - Five new country-unit Welsh classes created (5w, 6w, 7w, 15w, 18w); total strata increased to 45.
    - Wales received 43 extra squares; England did not receive a proportional increase (some English classes retained as low as 4 squares per class).
    - Wales-specific adjustments maintained representation of Welsh sub-classes within allocations.
    - Revised Land Classification maps published for England with Wales and for Scotland; sampling framework updated accordingly.
  
- Data products and outputs relevant to GIS users
  - Land Classification maps: evolving classification schemas (32 → 40 → 45 strata) used to stratify sampling and estimate habitat extents.
  - Country-specific sampling frames: adaptations to enable England & Wales, Scotland (and later Wales-only) reporting, with country-unit versions of land classes.
  - Upland habitat module: targeted sampling to improve accuracy for upland habitat estimates in England & Wales.
  - Tables/figures (as referenced in the document) document the distribution of sample squares by class and country, and illustrate the sampling framework changes over time.
  
- Implications and considerations for spatial analysis
  - Consistency vs. comparability: changing the underlying Land Classification affects national estimates; the document notes a preference for using the latest classification within a survey for consistency, while acknowledging cross-survey comparability concerns.
  - Representativeness: the stratified approach and adjusted sample allocations aim to maintain balanced representation across land classes and countries, mitigating regional biases.
  - Data integration: shifting classifications and country-unit splits require careful handling when integrating historic and current data layers for time-series analyses.

- Acknowledgements and references
  - Acknowledges contributors and provides references for further reading on the development of the ITE Land Classification and Countryside Survey sampling.

- Notable sections (for quick GIS reference)
  - The origin and rationale for stratified sampling using the ITE Land Classification.
  - The transition from class-based, continent-wide sampling to country-specific (England with Wales; Scotland) reporting.
  - The role of upland habitat modules and Welsh-specific class subdivisions in CS2007.
  - The impact of classification changes on the creation of national estimates and cross-survey consistency.