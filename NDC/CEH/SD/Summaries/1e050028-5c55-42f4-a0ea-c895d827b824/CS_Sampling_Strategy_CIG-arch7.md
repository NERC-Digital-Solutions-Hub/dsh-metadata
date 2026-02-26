# The Sampling Strategy for Countryside Survey (up to 2007)

- Purpose and scope
  - Documents the sampling framework for the field element of the Countryside Survey (CS) and the evolution of the ITE Land Classification used to stratify sampling.
  - Highlights how the framework supports national, regional, and country-specific habitat estimates and trend analyses over time.
  - Emphasizes the linkage between stratification (ITE Land Classification) and allocation of survey squares (1 km squares) for robust, representative data.

- Core concepts for GIS and data products
  - Stratified random sampling to ensure representative coverage across ecological land classes.
  - Sampling unit: 1 km square, with the center square classified and the four surrounding squares allocated to the same class.
  - National estimates are produced by combining class-level statistics (mean habitat area per square) with the total area of each class.
  - Data products include land-class maps and time-series estimates of habitat features, supporting policy, planning, and public information.

- Evolution of the ITE Land Classification (timeline and impact)
  - 1978: First Land Classification (ITE) used to stratify GB field sampling.
    - 32 classes derived from environmental attributes; 1228 center squares classified, plus surrounding squares.
    - Resulting framework created 6039 km2 of classified squares and 256 field survey squares (8 per class).
  - 1984: Land Use survey expanded sampling; framework retained but increased to 12 squares per class (384 total).
  - 1990 CS1990: All Squares Land Classification.
    - Extended classification to every GB square using surrogates for climatic, geological, and physiographic factors.
    - 508 squares surveyed; Land Cover Map linked to the program.
    - Classification update caused some reassignments; 62% correspondence with prior classification when squares were reassigned.
  - 1998: Revised Land Classification for CS1990 results.
    - Expanded to 40 classes; prepared for Scotland reporting; began addressing regional estimation needs.
  - 2000 CS2000: Separate country estimates and refined sampling.
    - Sub-divided Land Classes to produce country-unit versions (England with Wales, Scotland).
    - Increased strata to 40; added 19 extra squares (minimum 6 per new class); 11 more squares to balance England/Wales.
    - Upland habitat module added to improve accuracy for uplands in England and Wales.
    - Isle of Man squares removed for country-unit estimates; replaced to maintain representation.
  - 2007 CS2007: Wales-focused revisions and Wales-only reporting.
    - Wales required stronger representation for Wales-only estimates; five new country-unit classes created (5w, 6w, 7w, 15w, 18w).
    - Strata increased to 45; 43 additional Welsh squares added; England retained some lower-representation classes.
    - Wales became the most intensively sampled country unit; Wales-specific maps and reporting prepared.

- Sampling framework and allocation (how GIS data is organized)
  - 1 km square sampling unit as the geographic basis; center square classified, with surrounding squares assigned to the same class.
  - Initially, at least eight samples per land class were targeted; later adaptations increased sample counts to support country-specific estimates.
  - Strata and class maps (land-class maps) drive where squares are drawn and how estimates are aggregated.
  - Tables and figures (e.g., Table 2, Table 3; Figures 4–7) illustrate the distribution and counts of sample squares by class and country.

- Country-specific reporting and upland modules
  - England & Wales vs Scotland reporting requirements influenced the sampling design.
  - Wales-specific class subdivisions and increased Welsh sampling improved precision for Wales-only reporting.
  - An upland module (CS2000) added 30 upland squares to improve habitat estimates in upland areas of England and Wales.

- Data interpretation and implications for national estimates
  - The choice of land classification directly affects the comparability of national estimates across survey waves.
  - 2006 scoping work notes that changing the classification basis can impact the consistency of stock estimates; two approaches exist: latest-country-classification-based estimates or original cross-survey classifications.
  - National estimates in CS2000 and CS2007 reflect the need for consistent country-unit reporting and improved sampling density in Wales.

- Summary of outputs and references
  - Outputs include revised land-class maps for each country unit, detailed counts of sample squares by class and country, and time-series habitat estimates.
  - The document provides cross-references to major CS reports and methodological papers detailing the evolution of the ITE Land Classification and its application to Countryside Survey.
  - Acknowledgements note contributions from statisticians and ecologists who supported methodological guidance and data synthesis.

- Practical takeaways for GIS specialists
  - The Countryside Survey exemplifies how a multi-temporal GIS-based stratification system (ITE Land Classification) underpins robust, policy-relevant habitat and land-use estimates.
  - For GIS data products, ensure clear documentation of classification versioning, cross-wwalks between classifications, and country-unit distinctions to maintain comparability over time.
  - When designing or updating GIS workflows, incorporate upland modules and country-specific sampling adjustments to meet policy reporting needs and improve spatial representativeness.