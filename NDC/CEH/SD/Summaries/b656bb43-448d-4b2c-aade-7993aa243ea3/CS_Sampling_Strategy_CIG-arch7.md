# The Sampling Strategy for Countryside Survey (up to 2007)

- Purpose: Document the sampling framework and land classification used for Countryside Survey fieldwork up to 2007, illustrating how GIS-ready land classes and stratified sampling underpin national and country-level habitat estimates and time-series analysis.
- Core idea: Use an environmental stratification (ITE Land Classification) to create representative samples of Great Britain that can be mapped, compared over time, and used to derive area estimates for habitat features.

## Key concepts for GIS and data products

- Stratified random sampling to ensure representative coverage across ecological variation.
- Land Classification (ITE Land Classification) as the spatial stratification basis for GB, later adapted for country-specific reporting.
- Sampling units: 1 km squares; original approach used a center square plus surrounding squares to capture local heterogeneity.
- Time-series linkage: successive surveys map changes in habitat areas over decades; classifications and sample locations are updated but anchored to prior frames for comparability.
- Data outputs: maps of land classes, sample locations, and national/country estimates of habitat areas.

## Land Classification and sampling framework

- ITE Land Classification: environmental attributes (altitude, geology, climate, etc.) used to classify GB land into discrete land classes.
- Purpose of classification: to stratify the population of GB land so that samples reflect the environmental heterogeneity of the countryside.
- Initial deployment (1978): 32 land classes derived from 1 km squares (center squares of a 15 x 15 km grid), with 4 surrounding squares per center; total of 6039 km squares classified; eight 1 km squares per class surveyed (256 total).
- National estimates: habitat areas estimated by multiplying the mean habitat area per square by the land-class area, then aggregating across classes.
- 1984 (2nd survey): sampling increased to 12 squares per class (384 total); used the 1978 Land Classification again for estimation.
- 1990 (CS1990): all GB squares classified via an updated Land Classification; 508 squares surveyed; added Land Cover Map linkage; repeat vegetation quadrats; urban/sea corrections incorporated.
- 1998 (CS1990 refinement): Land Classification expanded to 40 classes to support regional and Scotland-wide reporting.
- 2000 (CS2000): formal separation of country estimates (England with Wales, and Scotland); land classes subdivided into country-specific versions; 40 strata expanded to 40+; added samples to ensure representation of new classes; uplands module introduced to improve upland habitat estimates.
- 2007 (CS2007): Wales-only reporting driven by devolved policy needs; five new Welsh country-unit classes (5w, 6w, 7w, 15w, 18w) created; total 45 strata; added Welsh squares (43 in Wales) to ensure adequate representation; some English classes had reduced sampling but deemed acceptable for precision; Wales-focused maps produced.

## Chronology of surveys and classifications

- 1978 - Initial Land Classification and 1st Field Survey
  - ISA-based 32 land classes from center 1 km squares; 4 surrounding squares classified; 6039 km squares total; 8 squares per class (256 total).
  - National habitat estimates computed from mean habitat per square by land-class area.
- 1984 - 2nd Field Survey
  - 12 squares per land class (384 total); continued use of 1978 Land Classification for estimates.
- 1990 - All Squares Land Classification and 3rd Field Survey
  - Classification updated to include all 1 km squares; 508 squares surveyed; repeat of 1978 quadrats; integrates Land Cover Map GB.
- 1998 - Revised Land Classification for CS1990
  - Land Classification expanded to 40 classes to enable regional and Scottish reporting.
- 2000 - Developments for CS2000
  - Separate country estimates introduced; Land Classes subdivided into England-with-Wales and Scotland country-units; 40 strata; additional squares added for representation; upland habitat module added.
- 2007 - Developments for CS2007
  - Welsh-only reporting drive; five Welsh country-unit classes added; total 45 strata; 43 additional Welsh squares; some English classes with fewer squares (deemed acceptable per scoping study); Wales and England maps updated accordingly.

## Separate country estimates and uplands module

- Country-unit framework
  - England with Wales and Scotland estimated separately using country-only squares.
  - Land Classes subdivided into country-unit versions; aggregates created where necessary to maintain representation.
- Uplands module (CS2000)
  - Added sampling in upland and marginal upland classes to improve habitat estimates in higher elevation areas.

## National estimation approach

- Core formula: For each land class, estimate habitat area as:
  - mean habitat per square within the class × total area of that land class
  - Sum across all land classes to obtain national or country-level estimates.
- Data consistency consideration
  - Note: Changing the basis of national estimates (latest classification vs original) affects comparability; 2006 scoping study recommends using the latest for internal consistency, but cross-survey comparability may favor the original classification in some contexts.

## Implications for GIS and data users

- Rich time-series mapping: enables visualization of habitat change over decades across GB and its countries.
- Classified land maps serve as a robust stratification layer for GIS analyses and future data integration.
- Sampling and classification changes (e.g., introduction of Welsh classes, upland module) improve country-specific reporting but require careful handling when aggregating across surveys.
- Users should account for classification updates when performing cross-survey comparisons or compiling historical time series.

## Additional notes

- Documentation includes detailed histories of the ITE Land Classification development, methodological justifications, and appendices detailing classification evolution and early history.
- The approach emphasizes representativeness, transparency in sampling design, and alignment with policy-relevant country reporting (England, Scotland, Wales).