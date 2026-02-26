# The Sampling Strategy for Countryside Survey

## Overview
- Documents the development and application of the ITE Land Classification as the sampling framework for Countryside Survey field work from 1978 through 2007 (updated 2011).
- Emphasises stratified, random sampling to ensure representative national estimates of habitat land use and related features across Great Britain.
- Describes how the Land Classification evolved, the sampling allocations per survey, and how country-specific estimates (England, Wales, Scotland) were created and updated over time.
- Highlights data governance considerations important for long-running time-series datasets, including classification versioning, comparability across surveys, and transparency about updates and limitations.

## Land Classification: Evolution
- The ITE Land Classification originated in the 1970s to stratify large ecological surveys and enable representative sampling.
- 1978 (CS1978): 32 land classes defined from environmental attributes; used a stratified random framework with 8 samples per class (256 total).
- 1984 (CS1984): sampling increased to 12 km squares per class (384 total) to broaden coverage.
- 1990 (CS1990): all GB 1 km squares classified; major revision to allow nationwide estimates; urban and sea corrections incorporated; number of classes expanded to 40.
- 1998–2000 (CS2000): further refinement to support Scotland- and England/Wales-specific reporting; introduced country-unit subdivisions and increased strata to 40; added 19–43 extra squares to improve representation, with Isle of Man replacement for country-unit estimates.
- 2007 (CS2007): additional Wales-specific adjustments (devolution context) requiring Wales-only reporting; introduced five new Welsh classes (5w, 6w, 7w, 15w, 18w); strata increased to 45; added 43 more Welsh squares and adjustments to maintain representation across countries.
- Throughout, practical adaptations addressed computational limits, regional representativeness, and the need for country-specific estimates.

## Sampling Framework by Survey Year
- 1978 CS1978:
  - 32 Land Classes; 8 sample squares per class; total 256 squares.
  - Sampling based on centre squares of a 15 x 15 km grid; ISA-based classification to form Land Classes.
- 1984 CS1984:
  - 32 classes; 12 squares per class; total 384.
  - Sampling expanded within the same framework to strengthen estimates.
- 1990 CS1990:
  - All GB 1 km squares reclassified under a unified Land Classification; 508 squares surveyed.
  - Retained previous features, with repeat vegetation quadrats; introduced Land Cover Map linkage.
- 2000 CS2000:
  - Major revision to support separate country estimates (England with Wales; Scotland); added country-unit subdivisions and 40 strata.
  - England & Wales: 28–30 squares per class in aggregate across 40 strata; Scotland: distribution adjusted to reflect country needs.
  - Uplands module included: an additional 30 squares targeting upland/marginal habitats to improve country-specific estimates.
  - Wales-specific expansion: Wales sampling expanded from 64 squares (CS1990/CS2000 baseline) toward 107 squares for CS2007.
- 2007 CS2007:
  - Wales-focused adjustments to meet Wales-only reporting needs; introduced five new Wales-specific classes (5w, 6w, 7w, 15w, 18w).
  - Total strata increased to 45; supplementary Welsh squares added to ensure representation of new classes; England had reduced squares for two classes (4 per class in some cases) with minimal precision impact.
  - Final distribution supports both UK-wide and country-specific habitat change reporting.

## Country-specific Estimates and Wales/Uplands
- Separate country estimates:
  - Framework subdivided Land Classes into country units (England & Wales; Scotland) to enable country-specific reporting.
  - Aggregation applied where a country had too few squares in a given class to maintain statistical reliability.
  - Isle of Man samples removed from country-unit estimates; replaced with additional squares in England.
- Wales:
  - Wales became the most intensively sampled country in CS2007 to support Wales-only environmental policy/reporting needs.
  - Welsh-class subdivisions created (5w, 6w, 7w, 15w, 18w) and ensured a minimum of 6 squares per new Welsh class.
  - Wales sample squares increased from 64 (CS1990/2000 baseline) to a higher count by 2007 (107).
- England and uplands:
  - England required adjustments to align with Wales and Scotland reporting standards; uplands module added to bolster habitat estimates in upland areas of England and Wales.

## Data Governance and National Estimates
- Note on national estimates:
  - Changing the core Land Classification affects consistency of stock/area estimates across surveys.
  - For cross-survey consistency, the latest Land Classification is preferred for GB-wide estimates, while the original (1990) classification may be used for cross-survey comparability.
  - Tables and figures document how sample sizes and strata have evolved, and how estimates should be interpreted given classification changes.
- Documentation and provenance:
  - Detailed historical record of classifications, sampling allocations, and country-specific adaptations provide necessary provenance for time-series analyses.
  - Appendices and references document methodological foundations, scope for Wales/Scotland reporting, and related methodological literature.

## Practical Data Stewardship Implications
- Versioning and provenance:
  - Maintain explicit versioning of the Land Classification and sampling frames used for each survey year (1978, 1984, 1990, 2000, 2007).
  - Capture country-unit definitions (England & Wales; Scotland) and any sub-divisions (Welsh classes) to support reproducible country-specific estimates.
- metadata and interoperability:
  - Record the number of squares per class per survey, geographic coverage, and any changes in class definitions or country boundaries.
  - Link field survey data to the Land Classification version and year to enable correct interpretation and comparability.
- data quality and limitations:
  - Be transparent about precision implications when class counts per country are small (e.g., some English classes in CS2007 with only four squares).
  - Document upland and marginal habitat sampling as a distinct module with targeted squares to improve estimates for specific regions.
- governance for long-term datasets:
  - Ensure clear documentation of changes in sampling strategy, class definitions, and country-unit reporting to support robust, auditable time-series analyses.
  - Provide guidance for researchers on when to apply latest classifications versus historical classifications for GB-wide versus country-specific estimates.

## Appendices and Further Reading (Context)
- Includes brief history of the ITE Land Classification and references detailing methodological developments, comparisons, and applications to policy-relevant reporting.
- Acknowledgements highlight contributors and statistical guidance that supported the sampling strategy evolution.