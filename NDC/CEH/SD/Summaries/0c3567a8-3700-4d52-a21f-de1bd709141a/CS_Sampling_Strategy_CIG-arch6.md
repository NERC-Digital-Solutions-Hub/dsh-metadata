# The Sampling Strategy for Countryside Survey (up to 2007)

## Overview
- Describes the sampling framework and the evolution of the ITE Land Classification used for Countryside Survey field surveys in Britain.
- Aims to provide representative, stratified samples to detect ecological and land-use change over time.
- Emphasises linking past and present methodologies to understand timeseries data and ensure comparability where possible.

## The ITE Land Classification and Stratification
- Stratified, random sampling is used to avoid bias and ensure representative coverage of diverse landscapes.
- Land Classification groups environmental attributes (altitude, geology, climate, etc.) into discrete land classes.
- Initial approach classified a subset of GB 1 km squares (center squares of a 15 x 15 km grid) into 32 classes; surrounding squares were assigned by a consistent key.
- The classification provides the framework (strata) for sampling and for deriving national habitat estimates.

## Chronology and Key Developments

- 1978 (Initial Land Classification & 1st Field Survey)
  - ISA-based classification produced 32 land classes from 1228 categorized squares; 8 squares per class (256 total) were surveyed.
  - National habitat estimates calculated as the product of mean habitat area per square within a class and the total area of that class.

- 1984 (2nd Field Survey)
  - Extended framework to 12 squares per class (384 total); eight squares previously visited were reused.
  - Focus shifted toward land use and habitat mapping.

- 1990 (All Squares Land Classification & 3rd Field Survey)
  - Land Classification revised to classify every square in GB; urban/sea corrections applied.
  - 508 squares surveyed; included repeat vegetation quadrats from 1978.
  - Linked to the first Land Cover Map of GB.

- 1998–2000 (Revised Land Classification & 4th Field Survey; Separate country estimates)
  - Expanded classification (up to 40 classes) to support Scotland reporting; later adjustments enabled England/Wales and Scotland reporting as separate country units.
  - England & Wales and Scotland-based estimates introduced; 40 strata formed via subdivision/aggregation of classes.
  - Additional squares added (19 new for country representation; 11 extra for balance) and adjustments for Land Class 17 in Wales.
  - Isle of Man squares replaced to align with country-based reporting.
  - An uplands module was added to improve habitat estimates in upland England and Wales.

- 2007 (Revised Land Classification & 5th Field Survey; Wales-focused reporting)
  - Wales-only reporting required additional Wales-specific classes (5w, 6w, 7w, 15w, 18w) bringing total to 45 strata.
  - 43 additional Welsh squares added; England had no corresponding extra additions in this update.
  - Wales class representation refined; maps updated for England with Wales and Scotland.

## Country and Regional Adaptations
- Separate country estimates introduced to enable England & Wales and Scotland-specific reporting; Wales-focused adjustments implemented for Wales-only outputs.
- Uplands module added to bolster statistical accuracy for upland habitats in England and Wales.
- Isle of Man data removed from country-level estimates and replaced with additional squares elsewhere to maintain representativeness.

## Data Outputs and Estimation Approach
- For each survey, the sampling design is documented by:
  - Number of squares, strata, and sampling rate (1:x) per land class and country.
  - Changes in the land classes and the corresponding effect on representation and estimates.
- National estimates are derived by applying per-square habitat measurements to the land-class areas; classification changes affect cross-survey comparability.
- Tables in the document summarize the distribution of sample squares across classes and years (CS1978, CS1984, CS1990, CS2000, CS2007) and by country (England & Wales, Scotland, Wales).
- Outputs include land-class maps, country-specific estimates, and habitat-change statistics over time.

## Data Quality, Comparability, and Challenges
- Changing the basic land-class framework impacts the consistency of national stock estimates across surveys.
- Within a given survey, latest classification is preferred for consistency; cross-survey comparability may require mapping between classifications used in different years.
- The framework relies on surrogate data for some variables when full-classification coverage is not feasible given computational limits.

## Practical Implications for Data Support
- Data products can include time-series dashboards showing habitat area by land class and country, with the ability to drill into uplands and Wales-specific classes.
- Mapping and legend alignment across surveys are essential to maintain comparability.
- Documentation should include mappings between older 32-class schemes and newer 40/45-class schemes, plus any country-unit subdivisions.
- Considerations for data pipelines include handling shifts in classification, reweighting samples for country-specific reporting, and preserving provenance of each survey version.

## Acknowledgements and Further Reading
- Acknowledges contributions from DETR, CEH, ITE, and other researchers for methodological development and statistical guidance.
- References and bibliographic notes provide deeper historical context and methodological details for each survey iteration.