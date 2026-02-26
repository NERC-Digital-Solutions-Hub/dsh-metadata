# The Sampling Strategy for Countryside Survey

- Purpose and scope
  - Describes the sampling framework for Countryside Survey fieldwork up to 2007.
  - Uses the ITE Land Classification as the basis for stratified sampling to ensure representative, map-based ecological data across Great Britain.
  - Aims to support time-series analysis by linking field surveys to evolving land classifications and to provide country-specific estimates (England & Wales, Scotland; Wales-only reporting introduced for 2007).

- Core concepts for GIS context
  - Stratified random sampling: dividing land into homogeneous strata (land classes) to obtain representative samples and robust national estimates.
  - 1 km square sampling units: field survey units that balance geographic detail with survey practicality.
  - Land Classification as a data framework: classification maps underpin sampling design, thematic mapping, and estimation of habitat areas.

- Evolution of the ITE Land Classification (high-level timeline)
  - 1978 (Initial Land Classification)
    - Indicator Species Analysis (ISA) used to define 32 land classes from environmental attributes across 1228 center 1 km squares.
    - Surrounding four squares per center square also classified, yielding 6039 squares total for classification-based proportion estimates.
    - Eight samples per land class (256 total) for national habitat estimates.
  - 1984 (Second field survey)
    - Sampling expanded to 12 squares per class (384 total); still based on the 1978 Land Classification.
  - 1990 (All Squares Land Classification; CS1990)
    - Land Classification revised to cover all GB squares; 508 squares surveyed.
    - First link to Land Cover Map (from satellite data).
    - Some centers reclassified; national estimates still tied to the 1990 scheme.
  - 1998 (Revised Land Classification; CS1990 updates)
    - Land classification extended to 40 classes; supports regional and local estimates (including Scotland).
    - Field survey expanded to 569 squares.
  - 2000 (CS2000)
    - Separate country estimates introduced (England & Wales vs Scotland) to align with policy needs.
    - Land Classes subdivided for country units, increasing strata to 40, plus additional squares to ensure representation (total of 40–45 strata across changes).
    - Wales-specific adjustments included, plus a dedicated upland habitat module.
  - 2007 (CS2007; Wales-focused reporting)
    - Wales-only reporting requirements prompted further Welsh subdivisions (five new country-unit classes: 5w, 6w, 7w, 15w, 18w).
    - Strata increased to 45; additional Welsh samples (43 more in Wales) to ensure six squares per Welsh class.
    - England samples adjusted to maintain comparability; some English classes reduced to four squares due to Welsh additions.
    - Complete revised land-class maps for England with Wales and Scotland issued.

- Sampling framework details
  - Stratified, random sampling using the Land Classification strata as the primary stratification level.
  - Class counts and distribution updated across surveys to preserve representation and improve country-specific estimates.
  - Tables and figures document the distribution of squares, strata areas, and sampling rates (e.g., CS2000 and CS2007 tables; maps in figures 4–7).
  - Note on national estimates: changing the underlying Land Classification affects cross-survey comparability; using the latest classification is preferred for consistency within a survey, while older classifications may be used for cross-survey comparisons.

- Uplands and additional modules
  - CS2000 introduced an uplands module, adding 30 squares in upland/marginal upland Land Classes to improve habitat estimates in higher-elevation areas.

- Welsh-only reporting and class subdivisions (2007)
  - Wales required more detailed, Wales-only results; land classes subdivided into 5w, 6w, 7w, 15w, 18w for England & Wales contexts.
  - Wales allocated additional squares to ensure adequate representation; England adjustments kept precision acceptable per scoping guidance.

- Data implications for GIS practice
  - Land Classification maps for each survey version (1990, 2000, 2007) influence how spatial data are joined, aggregated, and compared over time.
  - The shift to country-unit classifications requires careful cross-walking when producing country-specific GIS outputs or time-series analyses.
  - The introduction of country-specific sampling (England & Wales vs Scotland; Wales-focused subdivisions) impacts estimation layers and uncertainty (strata-area and sampling-rate metadata are essential for GIS workflows).
  - The uplands module adds targeted sampling in higher elevations, affecting habitat-status mapping and related statistics.

- Acknowledgements and references
  - Acknowledgements credit statisticians and data synthesizers; further reading lists foundational reports and methodological papers related to the ITE Land Classification and Countryside Survey iterations.

- Appendices and supplementary history (Appendix i)
  - Provides a concise history of the ITE Land Classification development, detailing the progression from the original 32 classes to later expansions (40, then 45 classes) and the cross-walk between surveys.
  - Outlines the progression of field surveys (CS1978, CS1984, CS1990, CS2000, CS2007) and how classifications were adjusted to support national and country-level reporting.

- Key figures and tables referenced (for GIS use)
  - Figure 4–7: Maps of revised land classes and sample squares for England, Wales, and Scotland (CS2000 and CS2007 frameworks).
  - Table 2, Table 3, Table 4: Numerical summaries of class distributions, sample squares per survey, and cross-survey comparisons using different land classifications.
  - Figure 5: Map of CS2000 sample squares; Figure 7: Countryside Survey sample squares by country; Figure 6: CS2007 land-class framework.
  - Appendix tables: Historical crosswalks and methodological notes on national estimates.

- Further reading
  - References to foundational CS reports (CS1990 main report; CS2000 scoping and results; CS2007 Wales-specific reporting work) and notable methodological papers on the ITE Land Classification.