# The Sampling Strategy for Countryside Survey (up to 2007)

- Scope and purpose
  - Documents the evolution of the ITE Land Classification and the sampling framework behind Countryside Survey (CS) field work up to 2007.
  - Connects current sampling methodology to 30 years of prior work; essential for understanding how time-series data were derived and how changes in classification affect analyses and map-based data products.

- Core concepts
  - ITE Land Classification
    - Stratifies Great Britain into land classes using environmental attributes (altitude, geology, climate, etc.) to ensure representative sampling.
    - Originally produced 32 classes (mid-1970s) using centre squares of a 15 x 15 km grid and surrounding context.
    - Over time expanded to broader schemes (40, then 45 classes) to support regional and country-specific reporting.
  - Sampling framework
    - Uses stratified random sampling of 1 km squares (field survey units).
    - Early surveys used a fixed number of squares per class to balance coverage with resources.
  - Time-series linkage
    - Each CS iteration (1978, 1984, 1990, 2000, 2007) builds on the previous Land Classification, with adjustments to address policy needs and reporting requirements.

- Evolution by CS iterations
  - CS1978 (Initial survey)
    - 32 Land Classes; 8 squares per class; total 256 1 km squares surveyed.
    - Classification based on 1 km squares chosen from a central 15 x 15 km grid, with surrounding 4 squares classified as well.
  - CS1984 (Second field survey)
    - 12 squares per class; total 384 squares; expanded sample size to improve national estimates.
  - CS1990 (All Squares Land Classification)
    - Extended classification to include data from all GB squares; 508 squares surveyed.
    - Linked to first Land Cover Map of GB; results published and used for national estimates.
  - CS2000 (Preparation for separate country reporting)
    - Addressed policy needs for England & Wales vs Scotland reporting.
    - Land Classes subdivided into country-unit versions; total strata increased to 40.
    - Additional squares added to ensure representation of new classes; Isle of Man replaced by new England squares for country-unit reporting.
    - Separate uplands module added to improve habitat estimates in upland areas.
  - CS2007 (Welsh-only reporting and refinement)
    - Wales required Wales-only reporting; Wales was previously underrepresented.
    - Sub-divided Land Classes into Wales-specific variants (creating 5 new Welsh classes: 5w, 6w, 7w, 15w, 18w).
    - 43 additional Welsh squares added; England sampling adjusted accordingly (some classes in England reduced to 4 squares per class).
    - Revised maps showing England with Wales and Scotland classifications for CS2007.

- Data structures and maps
  - Class maps and sample square maps accompany each survey year, showing GB-wide and country-unit classifications.
  - Tables/figures document the distribution of squares by Land Class and country unit; maps illustrate sampling framework changes over time.

- Implications for GIS data products
  - Change management and cross-year comparability
    - national estimates depend on the Land Classification in use; moving between classifications (1990, 2000, 2007) can affect consistency of stock estimates.
    - Best practice for national estimates: use the latest classification per survey while noting cross-year differences.
  - Country-unit reporting
    - CS2000 and CS2007 introduce England & Wales and Scotland-specific sampling, requiring handling of country-unit strata and potential class sub-divisions.
  - Wales uplands and other modules
    - Upland module adds extra squares to improve precision for upland habitats in England and Wales; relevant for GIS analyses focusing on upland ecosystems.
  - Data translation and class crosswalks
    - Users may need crosswalks between Land Classes across survey years (e.g., original 32-class system vs revised 40/45-class systems) to analyze changes over time.
  - Spatial design considerations
    - 1 km square unit, stratified by environmental attributes, with clear documentation of sampling rates per class and per country unit.
    - Important for map-based analyses to account for sampling intensity, class area, and weighting when estimating habitat areas.

- Practical notes for GIS specialists
  - Use case: creating map-based data products that show habitat classes, sampling density, and changes over time.
  - Ensure alignment of class labels and definitions across years; apply appropriate crosswalks where necessary.
  Ensure awareness of country-unit reporting structures (England & Wales, Scotland) and the Welsh-specific classifications introduced in CS2007.
  Consider integrating upland module data for focused analyses in upland regions.
  Incorporate class-area weighting to derive national/regional estimates from sample squares.

- Acknowledgements and references
  - Acknowledges statistical guidance, data graphics, and synthesis efforts; provides references to foundational CS reports and methodological papers for deeper GIS methodological context.