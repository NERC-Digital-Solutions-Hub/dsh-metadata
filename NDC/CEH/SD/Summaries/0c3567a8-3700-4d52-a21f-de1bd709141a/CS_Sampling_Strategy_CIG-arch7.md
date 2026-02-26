# The Sampling Strategy for Countryside Survey (up to 2007)

- Purpose and scope
  - Describes the evolution of the ITE Land Classification and its use as the sampling framework for Countryside Survey field work from 1978 to 2007.
  - Explains how stratified, random sampling within land classes supports national, regional, and country-specific habitat and land-use estimates.
  - Emphasises the link between ground surveys and later map-based products (e.g., land cover mapping) and how the framework supports policy-relevant outputs.

- Core concepts for GIS-focused readers
  - Stratified random sampling: carve GB into discreet strata (land classes) to ensure representative sampling and reduce bias.
  - ITE Land Classification: environmental attributes (altitude, geology, climate, etc.) define classes used as strata; evolved across surveys.
  - Sampling units: 1 km2 squares; the centre of larger grids (and occasionally surrounding squares) used to build class representations.
  - Temporal linkage: early classifications underpin later surveys; national estimates are sensitive to changes in classification schemes.

- Chronology of major developments
  - 1978 (Initial Land Classification)
    - 32 ITE Land Classes derived from 1228 central 1 km squares (centre of 15x15 km grid).
    - 8 samples per class, total of 256 field squares.
  - 1984 (Second field survey)
    - Framework retained; 12 km2 squares surveyed per land class (384 total).
    - Emphasis on land use and landscape features; revisiting earlier quadrats.
  - 1990 (All Squares Land Classification; CS1990)
    - Shift to classify every GB square; satellite land cover mapping linked to the program.
    - 508 squares surveyed; expanded data collection to include prior quadrats.
    - Resulted in a consolidated Land Classification with broader coverage, but later needed updates for regional/local estimates.
  - 1990s (Developments to the Land Classification)
    - Recognition that not all GB squares could be classified at the same level of detail; adopted surrogates for cores of climatic, geological, and physiographic factors.
    - Original 1228-class framework had only partial correspondence (≈62%) with the new approach; most mismatches fell into neighboring classes, preserving overall class means.
  - 2000 (CS2000; separate country estimates)
    - Programme adjusted to enable England with Wales and Scotland reporting, using country-specific sampling.
    - Land Classes subdivided by country units; 40 strata created through sub-divisions and aggregation; 19 additional squares added to ensure representation; 11 more to balance between England and Wales.
    - Isle of Man squares removed from country-unit estimates and replaced.
    - An uplands module was introduced to improve habitat estimates in upland areas, with an additional 30 squares placed in relevant classes.
  - 2007 (CS2007; Wales-focused reporting)
    - Welsh-only estimates driven by devolved policy needs necessitated Wales-specific sampling refinements.
    - Welsh-specific sub-divisions created: five new Wales/England variants (5w, 6w, 7w, 15w, 18w); total strata increased to 45.
    - Wales received 43 additional squares to ensure at least 6 squares per Welsh class; England adjustments did not add squares and, for two classes (5e, 15e), some classes ended with as few as 4 squares.
    - England, Scotland sampling maps updated to reflect new framework; Wales became the most intensively sampled country unit.

- Country-level sampling and class structure
  - The framework evolved from a single GB-wide system to country-specific (England & Wales; Scotland) estimates.
  - Sub-division and aggregation of Land Classes create 40–45 strata, with additional squares to maintain representation across country units.
  - Wales required targeted Wales-only class subdivisions to support policy-relevant reporting.

- Uplands module
  - Added to CS2000 to improve statistical accuracy for upland habitats in England and Wales.
  - Involves allocating additional squares within upland-related Land Classes.

- Data products and GIS implications
  - Land Classification maps underpin the sampling framework and are used to design and interpret map-based data products.
  - The approach supports country-specific habitat status estimates and allows integration with satellite-derived land cover maps.
  - The evolving classification affects comparability across surveys; cross-survey consistency is addressed through guidance on using the latest classification for country estimates.
  - For GIS work, practitioners should expect:
    - Stratum-based layers (land classes) with country-unit subdivisions.
    - Sample square locations linked to class definitions and temporal versions.
    - Updated maps showing revised class distributions (e.g., England with Wales, Scotland; Wales-specific Wales-only maps).

- Key considerations and challenges for GIS practitioners
  - Changes in Land Classification over time can affect national estimates and cross-survey comparability.
  - Representation imbalances across classes and countries required corrective sampling and sub-divisions.
  - Data resolution and consistency: class definitions and country-unit subdivisions influence spatial joins and metadata needs.
  - Need to align ground-truth sampling data with satellite-derived land-cover products for integrated GIS analyses.

- Acknowledgements and references
  - The document builds on a long lineage of methodological work (e.g., Barr, Bunce, Howard, and colleagues) defining land classification and sampling for Countryside Survey.
  - Detailed tables, figures, and appendices document class descriptions, sampling counts, and class maps across years.

- Takeaways for GIS Specialists
  - The Countryside Survey uses a robust, stratified sampling framework anchored in evolving ITE Land Classifications to generate landscape-level habitat and land-use estimates.
  - For map-based data products, anticipate multiple versions of Land Class Maps corresponding to CS1978, CS1984, CS1990, CS2000, and CS2007, with country-unit and Welsh-specific variants.
  - When combining CS data across years or with other GIS datasets, account for classification changes and country-unit subdivisions to maintain comparability and accuracy.