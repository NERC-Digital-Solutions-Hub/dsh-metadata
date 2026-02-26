# The Sampling Strategy for Countryside Survey (up to 2007)

- Purpose and scope
  - Describes the sampling framework and land classification used to guide Countryside Survey field surveys up to 2007.
  - Grounded in the ITE Land Classification, developed over 30 years to stratify Great Britain for ecological surveying.
  - Aims to produce robust, comparable national and country-level habitat/change estimates and to support map-based data products for GIS users.

- Core concepts for GIS and data products
  - Stratified, random sampling to ensure representative coverage of ecological variation.
  - Use of a fixed 1 km square sampling unit, with a design that links field observations to classified landscape strata.
  - Land Classification as the spatial framework to allocate samples and to enable regional and national estimates.
  - Cross-temporal compatibility: classifications evolve, requiring crosswalks or documented transitions to maintain time-series consistency.

- Development arc of the ITE Land Classification and Countryside Survey
  - 1978 (Initial survey)
    - ISA (Indicator Species Analysis) used on environmental attributes to define 32 land classes across GB.
    - Sampling unit: 1 km squares; eight samples per class (total 256 squares) drawn from centers of a 15 x 15 km grid plus surrounding squares classified.
  - 1984 (2nd field survey)
    - Emphasis on land use and habitat mapping; sampling increased by ~50% to 12 squares per class (total 384).
  - 1990 (All Squares land classification; 3rd field survey)
    - Expansion to classify every 1 km square in GB; 508 squares surveyed.
    - Integration with the first Land Cover Map from satellite imagery; some reclassification of squares.
  - 1998 (Revised Land Classification; 4th field survey)
    - Land Classification extended to enable separate Scottish reporting; total classes increased to 40.
    - GB-wide sampling aligned with 40 strata.
  - 2000 (CS2000)
    - Introduction of separate country estimates (England with Wales, Scotland) reflecting devolution.
    - Sub-division of Land Classes into country-unit versions; aggregation of rare country-class combinations to stabilize estimates.
    - Additional squares added to ensure representation of new classes; upland habitat sampling module introduced for England & Wales uplands.
  - 2007 (CS2007; Welsh reporting adjustments)
    - Welsh-only reporting requirements led to Wales-specific class subdivisions (creating 5w, 6w, 7w, 15w, 18w; plus Welsh-scope refinements).
    - Additional Welsh squares (43 more in Wales; minimum of 6 squares per new Welsh class) and adjustments to England to maintain balance.
    - Wales becomes the most intensively sampled country unit; overall framework expands to 45 strata.

- Sampling design and class structure
  - Class counts and structure evolved from 32 to 40 (1990/1998) and then to 45 (2007) to support country-specific estimates (England, Wales, Scotland) and upland modules.
  - Core sampling mechanics remained: stratified random sampling across Land Classes, with targeted enrichment in underrepresented classes or regions to improve precision.
  - Separate country estimates required subdivision of classes by country, with some aggregation to maintain adequate sample sizes per class.

- Country-specific adjustments and upland module
  - England with Wales vs. Scotland-based estimates introduced for country-specific reporting.
  - Isle of Man squares were replaced in later adjustments to better serve country-level estimates.
  - Uplands module (CS2000) added 30 squares in upland/marginal upland areas to improve habitat estimates in those terrains.

- Outputs and national estimation approach
  - Tables and maps detailing the number of squares surveyed per class and per survey year, plus sampling rates (e.g., CS1978, CS1984, CS1990, CS2000, CS2007).
  - National habitat estimates historically computed as: mean habitat area per square in each Land Class × total land area of that class.
  - Acknowledgement of methodological issues when changing classifications across surveys; cross-survey consistency is maintained by referencing a preferred classification approach for each estimation task.

- Practical GIS implications
  - Requires careful management of land-class maps across time, including crosswalks when classifications are revised (e.g., 1990 reclassification and subsequent country-specific subdivisions).
  - Metadata and documentation are essential to align sample locations with their corresponding Land Classes in each survey year.
  - Outputs include country-specific estimates and upland modules, necessitating GIS layers that reflect England, Wales, Scotland, and upland strata separately.

- Acknowledgements and references
  - Acknowledgements credit statisticians and data specialists; the document includes an extensive reference list and an Appendix with a brief history of the ITE Land Classification.

- Appendix overview
  - Appendix i: Brief History of the ITE Land Classification documents the evolution of the classification system and key methodological milestones across successive Countryside Surveys.