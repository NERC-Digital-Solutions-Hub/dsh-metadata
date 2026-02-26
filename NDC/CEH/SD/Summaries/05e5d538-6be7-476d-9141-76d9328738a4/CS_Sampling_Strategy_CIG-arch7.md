# The Sampling Strategy for Countryside Survey (up to 2007)

- Purpose
  - Describes how Countryside Survey field sampling has evolved using the ITE Land Classification to stratify Great Britain for consistent, map-based ecological surveys.
  - Aims to produce robust, map-enabled habitat and landscape estimates for policy, science, and public audiences.

- Core concepts for GIS use
  - ITE Land Classification: a stratification system that groups land into classes based on environmental attributes (altitude, geology, climate, etc.) to ensure representative sampling across the landscape.
  - Units of sampling: 1 km² squares representing land classes; early strategy used centre squares of a 15 × 15 km grid with surrounding squares assigned to the same or nearby classes.
  - Indicator Species Analysis (ISA): multivariate method used to derive the land classes.
  - National estimates: calculated by combining mean habitat area per square within each land class with the total area of that class.
  - Cross-survey comparability: evolving classifications affect national estimates; consistency considerations guided methodological choices.

- Chronology of developments
  - 1978 – Initial Land Classification and field survey
    - ISA used to classify based on environmental attributes into 32 land classes from 1228 centre 1 km squares; surrounding four squares also classified.
    - 256 squares surveyed (8 per class) for national habitat estimates.
  - 1984 – Second field survey (land use focus)
    - Framework retained but sample size increased by 50% to 12 squares per class (total 384 squares); eight squares per class revisited.
  - 1990 – All Squares Land Classification and first “all squares” survey
    - Land Classification updated to classify every GB square; 508 squares surveyed.
    - Added Land Cover Map (from satellite data); extended features recorded from 1984 survey.
  - 1998 – Revised Land Classification (CS1998) and fourth survey
    - Classification expanded to 40 land classes; enabled separate Scottish reporting.
    - 569 squares surveyed in CS1990 data integrated; national estimates updated accordingly.
  - 2000 – Countryside Survey (CS2000) planning and changes
    - Considered regional (country-level) estimates; addressed representation and reliability for England, Scotland, Wales.
    - Separate country estimates introduced: land classes subdivided into country-unit versions; 40 strata created; additional squares added to ensure adequate representation.
    - Upland habitat module included: 30 extra squares in uplands of England and Wales to improve upland estimates.
  - 2007 – Revised Land Classification for Wales and England-Wales Scotland
    - Wales-only reporting needs drove country-unit refinements; five new country-unit classes created (5w, 6w, 7w, 15w, 18w); total strata increased to 45.
    - Wales received 43 additional squares to guarantee a minimum of 6 squares per Welsh class; adjustments to England not extended similarly.
    - Wales-specific sub-division for Land Class 17 further refined Wales estimates.
    - Two Welsh classes (or adjusted classes) left with 4–6 squares to balance precision and reporting needs.
    - Maps and tables (Figure 6, Table 3) illustrate revised sampling framework and square allocations.

- Sampling framework and outputs
  - CS1978 – 256 squares (8 per class) across 32 Land Classes; national habitat estimates derived per class.
  - CS1984 – 384 squares; maintained 32-class structure; enhanced sample size for better precision.
  - CS1990 – All Squares approach; 508 squares; Land Classification aligned to all GB squares; added urban/seascapes corrections; results published in Countryside Survey 1990 main report.
  - CS2000 – English and Welsh, plus Scottish reporting capabilities; 40 strata; added country-unit subdivision and logic to enable England+Wales and Scotland estimates; upland module added.
  - CS2007 – Wales-focused refinements; 45 strata; expanded Welsh sampling to support Wales-only reporting; mapped England-Wales-Scotland sampling framework; adjusted per-class square counts to balance precision.

- Data considerations for GIS specialists
  - Classification evolution: changing Land Classification affects comparability; crosswalks and consistent reporting decisions are necessary when integrating trajectories across surveys.
  - Spatial resolution: field sampling uses 1 km² units aligned to land-class maps; outputs feed map-based habitat area estimates and change detection.
  - Country-unit reporting: framework allows England+Wales and Scotland estimates, with Wales-specific sub-divisions to improve accuracy; implications for regional GIS products and policy analyses.
  - Class proliferation: increasing from 32 to 40 to 45 classes over time, with some country-specific subdivisions (e.g., Welsh 5w, 6w, 7w, 15w, 18w); ensure GIS data models accommodate multiple classification schemes or crosswalks.
  - Upland emphasis: dedicated upland module improves reliability of highland habitat statistics in England and Wales; relevant for highland-focused map products.

- References and helpful notes
  - Earlier and successive CS reports document the methodological changes, sample sizes, and country-specific adaptations.
  - The series emphasizes that national estimates are contingent on the classification used; the 1990 classification supports GB-wide estimates, while later surveys favor country-specific classifications for consistency with devolved policy needs.

- Takeaways for GIS workflows
  - Use the ITE Land Classification as the primary stratification framework for GB-wide sampling-derived GIS products.
  - Track classification versioning to maintain temporal comparability; apply appropriate crosswalks when integrating across CS surveys.
  - Leverage 1 km² sampling units for mapping habitat extents, changes over time, and country-level reporting (England & Wales, Scotland, and Wales-specific outputs).
  - Incorporate upland and country-unit modules when generating region-specific maps and statistics.