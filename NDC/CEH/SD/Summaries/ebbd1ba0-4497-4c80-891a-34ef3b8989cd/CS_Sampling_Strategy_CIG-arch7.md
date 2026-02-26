# The Sampling Strategy for Countryside Survey (up to 2007)

- Purpose and scope
  - Document outlines the sampling strategy used for Countryside Survey fieldwork up to 2007.
  - Builds on a 30-year evolution of the ITE (Institute of Terrestrial Ecology) Land Classification, which serves as the basis for stratifying GB landscape and guiding sampling.
  - Emphasizes understanding the historical development to inform current and future sampling frameworks.

- Core concepts for GIS and map-based data
  - Stratified sampling: Partitioning land into discrete, objective strata to ensure representative sampling and reduce bias.
  - ITE Land Classification: A hierarchical, multivariate framework describing environmental attributes (altitude, geology, climate, etc.) to define land classes used as sampling strata.
  - Sampling units: 1 km squares (center square plus surrounding squares) used to capture landscape-scale variation and enable national estimates.

- Historical development and key milestones
  - 1978 (Initial Land Classification): ISA (Indicator Species Analysis) applied to environmental attributes for 32 land classes from 1 km grids; 8 samples per class (256 total) for national estimates; groundwork for stratified ecological surveys.
  - 1984 (Land Use Survey): Sampling expanded to 12 squares per class (384 total) to better reflect land use and habitat mapping.
  - 1990 (All Squares Land Classification): Land Classification updated to classify every square in GB; 508 squares field-surveyed; integration with a national Land Cover Map derived from satellite imagery; early national estimates published.
  - 1998 (Revised Land Classification): Increased accuracy for regional reporting; number of land classes expanded to 40; preparations for Scotland-specific reporting.
  - 2000 (CS2000 – separate country estimates): Framework adjusted to enable England with Wales and Scotland-only estimates; introduced country-unit class subdivisions and aggregation to create 40 strata; added 19–43 extra squares to improve country representation; uplands module introduced later.
  - 2007 (CS2007 – Welsh reporting and Wales-specific refinements): Further sub-division of land classes into country-unit classes (including five new Welsh-specific classes); more Welsh samples to ensure Wales-only reporting precision; England samples slightly reduced in some classes but deemed acceptable for maintained precision.

- Sampling framework and data structure
  - Stratification by land class: Land Classes (32 → later 40 → 45 with Wales adjustments) form the basis for strata.
  - Sample allocation: Sizable, yet practical, numbers of squares per class; adjustments across surveys to balance representation across England, Scotland, and Wales.
  - Separate country units: England with Wales and Scotland reporting units enable policy-relevant, country-specific habitat and land-use estimates.
  - Upland module (CS2000): Additional sampling in upland/marginal uplands to improve accuracy of upland habitat estimates in England and Wales.

- Data products and implications for GIS
  - National estimates: Derived by combining per-square data with land-class area statistics (class-level means × class area; with adjustments for country units).
  - Consistency vs comparability: Changing land classifications affects cross-survey comparability; two approaches exist:
    - Use the latest classification for country-unit reporting.
    - Use the original 1990 classification for cross-survey consistency.
  - Wales-focused outputs: Wales-specific land-class subdivisions and increased Welsh sampling improve Wales-only habitat/change reporting.
  - Map-based outputs: The Land Classification framework enables map-friendly visualization of habitat types, land-use change, and policy-relevant spatial patterns across GB and its constituent countries.

- Practical considerations and challenges
  - Data distribution: Data are held across multiple surveys, years, and country units; requires careful harmonization for GIS products.
  - Resolution and representation: Ensuring appropriate resolution and representative sampling for each country and upland areas.
  - Data standards and integration: Aligning land-class maps, sample locations, and attribute data across surveys for reliable GIS visualization and analysis.
  - Prototyping and iteration: The evolving framework necessitates testing and refinement of GIS-ready outputs (maps, change indicators, habitat estimates).

- Endnotes and further reading
  - Includes an extensive appendix detailing the ITE Land Classification history (1978–2007) and additional references for deeper methodological and historical context.
  - Emphasis on the ongoing linkage between stratification methodology and map-based environmental reporting.