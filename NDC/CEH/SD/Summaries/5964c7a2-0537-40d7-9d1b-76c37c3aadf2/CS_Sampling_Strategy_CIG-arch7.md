# The Sampling Strategy for Countryside Survey (up to 2007)

- The document describes the evolution of the Countryside Survey sampling framework and the ITE Land Classification used to stratify field sampling from 1978 to 2007.
- Grounded in GIS-friendly, map-based stratification, the approach aims to produce robust national and country-specific habitat and land-use estimates by linking sample squares to a hierarchical land classification.

## Key concepts and motivations

- Stratified random sampling is used to avoid bias and ensure representative coverage across ecological land types and regions.
- The ITE Land Classification provides the strata: environmental attributes (e.g., altitude, geology, climate) define land classes used to allocate samples.
- Sampling units are 1 km² squares; due to limited early computing power, a center square plus surrounding squares were classified to derive class properties and proportions.

## The beginnings: 1978 Countryside Survey (CS1978)

- Indicator Species Analysis (ISA) used on environmental data from 1 km squares to produce 32 Land Classes.
- Center square (the 1 km classified) plus four surrounding squares created a total of 6039 km² classified for analysis.
- Eight samples per Land Class were surveyed (256 total) to estimate national habitat areas.
- National estimates: mean habitat area per square in each class × area of that class, enabling countrywide totals.

## 1984 Countryside Survey (CS1984)

- Field survey expanded to 12 km² squares per Land Class (total 384 squares).
- Used the 1978 Land Classification for national estimates.
- Results informed landscape change assessments and policy-relevant statistics.

## 1990 Countryside Survey (CS1990) and All Squares Land Classification

- Land Classification revised to classify every square in GB (All Squares approach); urban and sea corrections added.
- Field survey included 508 squares; repeated vegetation quadrats and broader land-use data were collected.
- The classification shift required re-evaluating how national estimates were derived; still based on Land Class proportions but now using a more complete GB-wide framework.

## Developments leading to CS2000

- CS1990 highlighted issues in representation and regional/policy needs, prompting:
  - Separate country estimates (England, Scotland, Wales) to support devolved governance.
  - Reassessment of sample sizes and representation across Land Classes to ensure adequacy for upland and regional reporting.
- The new Land Classification for CS2000 sought to maintain compatibility while enabling England-with-Wales and Scotland-only reporting.

## CS2000: Separate country estimates and expanded sampling

- Land Classes were subdivided into country-unit versions (England with Wales; Scotland) to support country-specific reporting.
- Class aggregation and subdivision created more strata (40 → 45), improving representation within each country.
- Additional squares were allocated to ensure adequate representation of new classes; Wales received a notable increase to support Wales-only reporting.
- An upland module added 30 extra squares to improve habitat estimates for uplands in England and Wales.
- Isle of Man squares were adjusted to align with country-unit reporting.

## CS2007: Wales-focused reporting and further refinements

- Wales-only reporting requirements led to further adjustments:
  - Sub-divisions created five new Wales-specific classes (5w, 6w, 7w, 15w, 18w) to reflect country-unit differences.
  - Total strata increased to 45; Wales received additional squares to ensure minimum representation in each Welsh class.
  - England adjustments were made to compensate for Welsh additions, though some English classes ended with as few as four squares.
- The CS2007 sampling framework maps show the revised England-with-Wales and Scotland classifications and the country-specific sample squares.

## Summary of sampling and data implications

- CS1978: 256 samples across 32 Land Classes; foundational stratified framework.
- CS1984: 384 samples; refinement and expansion of captured landscape data.
- CS1990: All Squares Land Classification; 508 samples; broader GB-wide coverage and emergence of country reporting needs.
- CS2000: Expanded to separate country estimates; more strata (40 → 45); Wales-focused sampling increases; upland module added.
- CS2007: Wales-specific classifications (5w, 6w, 7w, 15w, 18w); more Welsh squares; targeted improvements for Wales reporting; England adjustments to maintain balanced representation.

## National estimates and classification changes

- The method of deriving national estimates has shifted with each reclassification.
- For consistency within a single survey, the latest classification is preferred; for cross-survey consistency, some analyses align with the original 1990 classification.
- The document provides tabulated comparisons of sample sizes per class across surveys to illustrate how sampling and classification changes affect national estimates.

## Acknowledgements and references

- Acknowledges statistical guidance, data synthesis, and graphics support.
- Includes a comprehensive list of further reading and historical references on the ITE Land Classification and Countryside Survey methodology.

## Practical takeaways for GIS and data products

- The sampling framework is tightly coupled to a multi-era land classification scheme; map products should be paired with the corresponding Land Class maps for the target survey year.
- When generating country-specific or Wales-specific analyses, ensure the appropriate country-unit subdivisions and class definitions are applied.
- Be mindful of potential changes in class definitions across survey years when comparing time series; align classifications or reclassify historical data as needed for accurate GIS analyses.
- The upland and Wales-focused modules highlight the value of targeted sampling to improve precision in underrepresented areas within spatial datasets.