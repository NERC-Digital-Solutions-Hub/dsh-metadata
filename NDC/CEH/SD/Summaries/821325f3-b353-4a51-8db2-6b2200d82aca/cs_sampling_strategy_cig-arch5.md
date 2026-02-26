# The Sampling Strategy for Countryside Survey (up to 2007) Revised and Updated from: 'The Sampling Strategy for Countryside Survey', C.J. Barr, September 1998. DETR CONTRACT No. CR0212 Revised by C.M.Wood CEH Lancaster, Library Avenue, Bailrigg, Lancaster. LA1 4AP September 2011

## Overview and aim
- Describes the field survey sampling framework used in Countryside Survey up to 2007.
- Chronicles the evolution of the ITE Land Classification and its role as the stratification system for GB-wide ecological sampling.
- Explains how national, regional, and country-specific estimates are derived, including Wales and Scotland adaptations and upland modules.
- Emphasises continuity with prior surveys while detailing changes needed for country-specific reporting and improved statistical accuracy.

## Core concepts: stratified sampling and land classification
- Objective stratification is used to ensure samples are representative across GB land types.
- Stratification is built on the ITE Land Classification, which groups land based on environmental attributes (altitude, geology, climate, etc.).
- The Land Classification evolved from an initial 32 classes (1978) to more refined frameworks over time to support country-specific reporting.

## Evolution of the ITE Land Classification and Countryside Survey (CS) surveys

- The Beginning (1978)
  - Indicator Species Analysis (ISA) used to classify 1 km squares into 32 land classes from environmental attributes.
  - A main sampling unit of 1 km squares; eight samples per class (total 256) were selected randomly for the national survey.
  - Early national estimates of habitat area were derived by combining class area with mean habitat area per square within each class.

- The Second Survey (1984)
  - Sampling extended to 12 squares per land class (total 384) to improve precision; eight squares from the 1978 set were revisited.
  - National estimates updated using the 1978 Land Classification framework.

- All Squares Land Classification and Countryside Survey 1990 (CS1990)
  - Land Classification revised to incorporate data from all GB 1 km squares; a conservative revision preserved comparability.
  - 508 squares surveyed; additional habitat recording and quadrat replication conducted.
  - Linked to the first Land Cover Map of GB (satellite-derived) for broader interpretation.
  - Results published in CS1990 main report (1993).

- Developments for CS1990 and CS1990 onward
  - Realization that GB-wide estimates required broader classification coverage; attempted to classify every GB square.
  - Computational constraints led to using surrogates for full classification; new classifications still largely preserved class characteristics, though some reallocation occurred.

- Developments for CS2000
  - Reassessment of sample numbers and the need for separate country estimates (England & Wales vs. Scotland).
  - Land Classification extended to enable country-specific reporting; 40 strata created through subdivision and aggregation of classes; additional squares added to ensure representation of new classes.
  - An upland habitat module was added to improve precision for upland estimates in England and Wales.

- Welsh-only Estimates and adjustments (CS2007)
  - Devolution created demand for Wales-only reporting; Wales gained additional Welsh-class subdivisions (creating new Welsh-specific classes: 5w, 6w, 7w, 15w, 18w).
  - Total strata increased to 45; additional Welsh squares (minimum 6 per Welsh class) implemented; adjustments to England sampling to maintain balance.
  - Wales received enhanced representation for Wales-only reporting; England retained adequate precision for several classes despite some classes with fewer squares.

## Sampling framework and data structure

- Sample units and coverage
  - Core sampling unit remains 1 km squares (centres of a 15 x 15 km grid initially used, later refined).
  - Squares are allocated to Land Classes; sampling within each class provides national and country-level estimates.

- Sample sizes and allocation
  - 1978: 8 squares per class; total of 256 squares nationwide.
  - 1984: 12 squares per class; total of 384 squares; older class allocations retained for consistency with 1984 results.
  - 1990: 508 squares surveyed; all GB squares reclassified under the All Squares framework.
  - 2000: Expanded to accommodate country-level reporting; 40 strata; additional squares (including upland module) to strengthen estimates.
  - 2007: Wales-focused adjustments; 45 strata; Welsh-specific sampling increased; some English classes reduced in sample count but deemed acceptably precise.

- National estimates methodology
  - Estimates are derived by multiplying the mean habitat area per square within each Land Class by the total area of that class.
  - This approach ties national totals to the distribution of Land Classes and the measured habitat in sampled squares.

- Data products and references
  - Land Classification maps and sampling maps accompany each survey (references to Figures 1–7 and maps in the report).
  - Tables summarize numbers of squares by class and survey year, and illustrate sampling rates (e.g., 1:x values).

## Country-specific reporting and upland module

- Separate country estimates
  - CS2000 introduced country units (England with Wales and Scotland) with subdivisions of Land Classes to reflect country boundaries.
  - Additional sampling ensures adequate representation of each class within each country unit; aggregation when necessary to maintain statistical viability.

- Wales and uplands emphasis (CS2007)
  - Wales required dedicated Welsh reporting; increased Welsh sampling and Welsh-specific Land Classes.
  - An upland habitat module (30 extra squares) added to boost precision for upland habitats in England and Wales.

## Data governance implications for Data Stewards

- Data lineage and versioning
  - Land Classification evolves across surveys (1978, 1984, 1990, 1998, 2000, 2007); consistent documentation of which classification was used for each CS survey is critical for temporal analyses.
  - National estimates may be calculated using different classifications depending on the survey year; notes emphasize choosing the latest for within-survey consistency or maintaining historical classifications for cross-survey comparability.

- Metadata and data standards
  - Clear metadata is needed for class definitions, boundary changes, and country-specific subdivisions.
  - Documentation of sample allocation rules (subdivision/aggregation) and rationale for adding (or removing) squares per class is essential for reproducibility.

- Data sharing, licensing, and embargoes
  - Data are produced for national and country-level reporting; governance should address sharing of Land Classification maps, sampling grids, and habitat statistics with appropriate embargoes and permissions.

- Data updates and provenance
  - Updates to Land Classification or sampling schemes should be versioned and traceable to avoid confusion in longitudinal analyses.
  - The upland module and Welsh classifications introduce additional data layers; provenance should capture which modules and year-specific rules were applied.

## Challenges and considerations

- Incomplete user needs picture and data timeliness
  - Aligning country-specific needs (e.g., Wales-only reporting) with the broader GB framework requires careful planning and data model flexibility.

- Interoperability and representativeness
  - Changes in Land Classification across years can affect comparability; cross-survey consistency requires clear mapping between old and new classes and explicit guidance on longitudinal interpretation.

- Sample size and precision
  - Wales’ high land area representation required more extensive sampling; some English classes receive fewer samples, with assessments of precision indicating acceptable, albeit nuanced, impacts on estimates.

- Handling multiple systems and formats
  - Transitioning between original 1990 Land Classification and later refined classifications demanded careful management to ensure all estimates remain interpretable and usable.

## Summary of historical progression (by year)

- 1978: Initial Land Classification with 32 classes; 256 squares surveyed nationwide.
- 1984: Second field survey; 12 squares per class; 384 squares total.
- 1990: All Squares Land Classification; 508 squares surveyed; integration with satellite-derived land cover mapping.
- 1998: Revised Land Classification to support Scotland reporting; world-class expansion to 40 classes.
- 2000: CS2000; country-unit reporting introduced; 40 strata; upland module added; broader representation across GB.
- 2007: CS2007 adjustments for Wales-only reporting; Welsh classes subdivided to create 45 strata; Wales gains enhanced sampling.

## Acknowledgements and references

- Acknowledgements for contributors and statistical guidance.
- References and bibliography detailing foundational works on the ITE Land Classification and Countryside Survey lineage.
- Appendix i: Brief history and evolution of the ITE Land Classification (detailed year-by-year development).