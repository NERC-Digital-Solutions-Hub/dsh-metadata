# The Sampling Strategy for Countryside Survey (up to 2007)

## Overview
- Describes the evolution of the ITE Land Classification and the Sampling Strategy used for Countryside Survey field work up to 2007.
- Emphasizes stratified sampling, the use of an environmental land classification to shape GB-wide surveys, and the linking of field data to map-based outputs.
- Highlights the continuity with prior surveys while detailing adaptations for country-specific reporting (England, Wales, Scotland) and upland habitat estimation.

## Core concept: ITE Land Classification and Stratified Sampling
- Stratified, random sampling to ensure representative coverage across ecological variation (strata built from land classifications).
- Original approach used a 1 km square sampling unit, with centre squares classified and surrounding squares included to propagate class labels.
- Classification served as the framework for both site selection and national/habitat estimates.

## Development timeline and key changes

- The Beginning (early 1970s)
  - Idea of national ecological sampling using stratified sampling to capture variability.
  - Basis for the ITE Land Classification to stratify GB land into meaningful ecological types.

- 1978: First version of the ITE Land Classification
  - ISA (Indicator Species Analysis) used on environmental attributes to define 32 land classes.
  - Classification applied to centre 1 km squares (1228 centres) with four surrounding squares allocated to classes.
  - Final set encompassed 6039 km squares; 256 field samples (8 per class) for national estimates.

- 1984: Land use survey of GB (second field survey)
  - Framework retained; sample size increased (12 squares per class; 384 total).
  - Aimed to map land use/land cover and habitat features, with results published later.

- 1990: Countryside Survey 1990 (CS1990) and “All Squares” Land Classification
  - Land Classification updated to classify every GB square (broad, conservative revision).
  - 508 squares surveyed; repeated vegetation quadrats recorded; introduction of the first Land Cover Map linked to the program.

- Post-1990: Expanded classification and surrogates
  - Efforts to classify all GB squares using major climatic, geological, and physiographic surrogates.
  - Various multivariate classifications tested; best match to original had 62% correspondence, but non-matching squares fell into neighboring classes, preserving overall class characteristics.
  - Result: a revised, scalable framework for regional/local estimates; implications for mapping and data interpretation.

- 2000: Countryside Survey 2000 (CS2000) and country-unit estimates
  - Recognized need for separate England & Wales and Scotland estimates.
  - Land Classes subdivided into country-unit variants; total strata increased to 40.
  - Additional squares added to ensure adequate representation of new/subdivided classes; upland habitats module introduced to improve upland estimates for England and Wales.
  - Wales received focused sampling enhancements (including new Welsh-class sub-divisions).

- 2007: Countryside Survey 2007 (CS2007) and Wales-focused reporting
  - Wales-only reporting requirements driven by devolved policy needs.
  - Introduced five Welsh country-unit sub-classes (5w, 6w, 7w, 15w, 18w); total strata increased to 45.
  - Additional Wales squares (43) to maintain representation; some English classes experienced reduced per-class sample counts (still deemed adequate for reporting).
  - England/Scotland maps and samples adjusted accordingly to maintain overall balance.

## Sampling framework and data structure

- CS2000 framework
  - Sub-division of Land Classes into country-unit versions; aggregation where necessary to ensure representation within each country.
  - Additional sample squares allocated to preserve minimum representation per new/subdivided class.
  - Upland habitat module added for improved country-specific upland estimates.

- CS2007 framework
  - Wales-specific refinements to capture country-specific habitat status changes.
  - Wales receives dedicated sub-classes and increased Welsh-class representation; overall strata expanded to support Wales-only outputs.
  - England retains fewer squares in some broad classes but overall precision remains acceptable for reporting.

- Summary of outputs and usage
  - The sampling framework defines the basis for national habitat estimates by class area and per-square measurements.
  - National estimates can be derived from mean habitat area per square within each class, multiplied by class total area.
  - Cross-year comparability is impacted by changes in classification; CS1990, CS2000, and CS2007 use versions of the Land Classification tailored to country-specific reporting.

## Implications for GIS and data users

- Map-based data products
  - Land Classification maps underpin GIS outputs and enable spatial interpretation of habitat types, land use, and changes over time.
  - Versioning is critical: CS1978/1984 used the original 32-class system; CS1990 introduced a GB-wide refinement; CS2000 and CS2007 added country-unit splits and more classes for Wales and the uplands.

- Multiscale and multi-year integration
  - Data linked to 1 km square units allow scaling analyses from local to national levels.
  - Time-series analysis requires careful alignment of classification versions to maintain consistency across surveys.
  - Wales and Scotland (and England) require distinct handling for country-specific outputs, yet harmonized in the overall UK framework.

- Data quality and packaging challenges
  - Data are distributed across surveys and class versions, necessitating careful data management when building GIS products.
  - The evolution of classifications aims to improve accuracy for country-specific reporting, but introduces cross-year classification shifts that must be reconciled for longitudinal analyses.

## End notes

- The Sampling Strategy for Countryside Survey provides a historical and methodological thread linking decades of GB ecological sampling through the ITE Land Classification to contemporary country-specific environmental reporting.
- It emphasizes the balance between representative sampling, evolving land classifications, and the need for robust, map-based ecological information across the UK.