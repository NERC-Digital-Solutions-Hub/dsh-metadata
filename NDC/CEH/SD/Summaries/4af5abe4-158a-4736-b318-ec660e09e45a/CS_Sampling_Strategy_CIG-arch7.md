# The Sampling Strategy for Countryside Survey (up to 2007)

- A long-running national ecological survey framework that uses an ITE Land Classification-based stratification to select representative field survey squares across Great Britain, enabling time-series habitat and land-use estimates.

## Core concepts and methodology

- ITE Land Classification: a stratified system classifying land into discrete classes based on environmental attributes (e.g., altitude, geology, climate) to ensure representative sampling.
- Sampling units: 1 km² squares as the primary spatial unit; a centre 1 km square plus four surrounding squares were classified to define each sampling unit.
- Stratified random sampling: minimizes bias by ensuring all parts of the landscape are represented through strata (land classes).
- Indicator Species Analysis (ISA): multivariate method used to group quadrats into land classes during early developments; later classifications built from surrogates and environmental data.
- Time-series linkage: the sampling framework is designed to be compatible across survey cycles, enabling change detection over decades.

## Evolution of the ITE Land Classification and sampling (by survey year)

- 1978 (Initial Land Classification and Field Survey)
  - 32 land classes derived from 1228 center squares within a 15 x 15 km grid; 4 surrounding squares added per center.
  - 8 samples per class, total 256 squares surveyed.
  - National habitat area estimates computed from class proportions and per-square means.

- 1984 (Second Field Survey)
  - Sampling expanded to 12 squares per land class (total 384).
  - Continued use of the 32-class framework.

- 1990 (All Squares Land Classification and Third Field Survey)
  - Land Classification extended to classify all GB squares (not just a sample); urban/sea corrections incorporated.
  - 508 squares surveyed; additional features recorded; repeat vegetation quadrats.
  - National estimates still tied to the 1990 classification; progress toward regional and national estimates.

- 1998 (Revised Land Classification and Fourth Field Survey)
  - Land Classification updated to enable separate Scottish reporting; number of classes increased to 40.
  - Results published and used for regional estimates.

- 2000 (Developments for Countryside Survey 2000)
  - Addressed policy-driven needs for separate England & Wales vs. Scotland estimates.
  - Class sub-division into country-unit versions, class aggregation where needed, and 19 additional squares to strengthen representation (minimum 6 squares per new class).
  - Upland habitat module added to improve upland estimates in England/Wales.

- 2007 (Developments for Countryside Survey 2007)
  - Welsh-only reporting requirements prompted further Wales-specific adjustments.
  - New Welsh country-unit classes introduced (5w, 6w, 7w, 15w, 18w) increasing strata to 45.
  - 43 additional Welsh squares added; England adjusted due to removal of Welsh squares.
  - Wales became the most densely sampled country unit; updated maps and tables reflect England, Wales, and Scotland distribution.

## Data products and GIS implications

- Spatial outputs: land-class maps and stratified sample locations (1 km² grids) across GB, including country-unit splits (England & Wales, Scotland) and Wales-only refinements.
- Time-series considerations: changes in land-class schemes over time require careful mapping across years to maintain comparability; 1990 Land Classification vs. 2000/2007 country-unit revisions affect cross-year consistency.
- Complementary data: links to the 1990 Land Cover Map and other environmental datasets for richer GIS analyses and model inputs.
- Data resolution: primarily 1 km², with broader country-level aggregations and habitat/change estimates derived from class-level statistics.

## Challenges highlighted for GIS practitioners

- Data held in multiple locations and across different classification schemes; integrating across years requires careful class mapping.
- Variability in class representation across years and countries necessitates attention when building time-series analyses.
- Need to reconcile Wales-specific and Scotland-specific estimates with England/Wales national estimates; differing numbers of squares per class by year.
- Data cleaning and transformation steps are essential to ensure accurate aggregation and interpretation in map-based products.

## Summary of end-state and purpose

- The Sampling Strategy for Countryside Survey documents the historical progression of the ITE Land Classification and its use as a framework for nationally representative, map-based ecological surveys.
- It explains how sampling frames evolved to support country-specific reporting (England, Wales, Scotland) and upland habitat estimation, culminating in the 2007 adjustments that enhanced Wales reporting and Wales-specific strata.
- The resulting GIS-ready outputs support policy, planning, and public-facing data products by providing stratified, spatially explicit habitat and land-use information across Great Britain.