# The Sampling Strategy for Countryside Survey (up to 2007)

## Overview and purpose
- Describes the sampling framework for the Countryside Survey field element, tying to the iterative development of the ITE Land Classification used since 1978.
- Aims to produce representative, map-based data products by stratifying GB land using an environmental Land Classification, then selecting a stratified random sample of 1 km squares for field survey.
- Emphasizes the need to understand historical changes in the sampling framework to interpret time-series results correctly.

## Evolution of the ITE Land Classification
- Early approach (1970s): classify land using environmental attributes (altitude, geology, climate) via a multivariate method (Indicator Species Analysis) applied to 1 km squares.
- Original Land Classification (circa 1978): 32 classes derived from a center 1 km square plus surrounding squares, forming a grid-wide stratification for sampling.
- 1984 upgrade: sampling expanded within each class (12 km squares per class), increasing total coverage for the second GB survey.
- 1990 revision: extend classification to every GB square using surrogates for climatic/geophysical factors; some squares reclassified; linked to the first Land Cover Map from satellites; results published for CS1990.
- 1998–2000 refinements: attempts to classify every GB square with improved surrogates; preparation for separate Scotland reporting; the number of Land Classes increased to around 40.
- 2007 adjustments: to support Wales-only reporting, Wales-specific sub-classes introduced (creating five new country-unit classes), and a larger Wales sample added; England classes adjusted to maintain representation; total strata increased to 45.

## Survey timeline and sampling details
- CS1978 (Initial survey): 8 samples per Land Class, total 256 squares; 32 classes; 1 km squares as the sampling unit.
- CS1984 (Second GB survey): 12 km squares per Land Class, total 384; continued use of the Land Classification as framework.
- CS1990 (All Squares classification): classification expanded to cover all GB squares; field survey of 508 squares; results linked to Land Cover mapping and ECOLUC program.
- CS2000 (Revised classification): address regional/local estimation needs; separate country estimates introduced (England & Wales, Scotland); added Wales upland sampling module; increased representation across classes; overall 40 strata became 40+ with country subdivisions.
- CS2007 (Welsh adjustments): further subdivided land classes into country-unit versions; added 43 extra Welsh squares to ensure Welsh classes are adequately represented; some English classes reduced to maintain precision, resulting in 45 strata across the region.

## Land Classes and class representation
- ITE Land Classes are environmental stratifications used to assign GB land into distinct categories (originally 32, later expanded to about 40–45 with country-specific subdivisions).
- Sub-divisions created to reflect country-level reporting needs (England with Wales, Scotland) and to improve precision for Wales and upland areas.
- Class maps and distributions are used to derive national estimates and to compare across survey years.

## Country-specific adjustments and Wales uplift
- Wales-specific needs drove:
  - Introduction of country-unit class sub-divisions (e.g., 5w, 6w, 7w, 15w, 18w) for Wales.
  - Increased number of Welsh sample squares to ensure at least 6 squares per Welsh class.
  - Reallocation and aggregation of classes across countries to maintain balanced representation.
- England and Wales samples adjusted to preserve overall precision; Isle of Man samples removed from country-unit estimates and replaced.

## Upland habitat module
- CS2000 added an upland-focused module (about 30 squares) to improve the accuracy of upland habitat estimates in England and Wales.
- This addressed under-sampling in upland/marginal areas when producing country-specific estimates.

## Data use and national estimates
- National estimates are derived by: mean habitat area per square in each Land Class × land area of the class.
- Changing classifications across surveys affects comparability; two main approaches exist:
  - Use the latest classification (preferred for survey consistency, especially for country-level estimates).
  - Use the original 1990 Land Classification for cross-survey consistency (more consistent across surveys but less aligned with current structuring).
- Table 4 (not reproduced here) shows how sample sizes per class evolved under the original classification versus updated schemes.

## Practical implications for GIS workflows
- Time-series GIS must accommodate changing Land Class schemes and country-unit subdivisions.
- Crosswalks between classifications are essential to compare habitat estimates across CS years.
- Spatial data products should include:
  - Land Class maps (original and updated versions) and country-unit classifications.
  - Sample square locations with class assignments for each survey year.
  - Upland module results for 2000 onward to support Wales/England upland analyses.
- When delivering Wales- or England-and-Wales-specific outputs, ensure correct application of country-unit classes and additional Welsh squares to maintain precision.
- Documentation should clearly note the classification version used for any national or country-specific estimates to prevent misinterpretation.

## Endnotes and references
- The document includes acknowledgements, further reading, and detailed tables/maps (not reproduced here) that provide the exact counts of squares per class per survey and the geographic distribution of sample squares.