# The Sampling Strategy for Countryside Survey (up to 2007)

- Overview
  - A historical and methodological account of how Countryside Survey sampling frames and land classifications were developed from the 1970s to 2007.
  - Emphasises how the ITE Land Classification is used as the sampling framework to create representative, stratified samples across Great Britain, with later adaptations for country-specific reporting (England, Scotland, Wales) and upland habitats.
  - Describes how data from field surveys are stratified, collected, and used to produce national estimates of habitat features.

- Core concepts for GIS context
  - Stratified, random sampling to ensure representative coverage of diverse land types.
  - Land Classification (ITE Land Classification) as a spatial framework: assigns GB 1 km squares to environmental classes based on key attributes; classes described and mapped.
  - Use of environmental surrogates (altitude, geology, climate, etc.) to classify all squares when full data collection is infeasible.
  - National estimates derived by combining class-level statistics with the land area occupied by each class.

- The ITE Land Classification and stratification
  - Origin: 32 Land Classes developed in the 1970s using indicators from environmental attributes; a 15x15 km grid centre square approach classified the majority of GB squares, with surrounding squares also allocated to classes.
  - Purpose: Provides an objective, stratified framework to sample representative habitat areas across diverse landscapes.
  - Outputs: Maps and tables describing Land Classes and their characteristics; used to estimate the area of habitats by class.

- Survey eras and their frameworks
  - 1978 (Initial Land Classification & Field Survey)
    - ISA-based grouping into 32 Land Classes from 1 km squares; eight samples per class (total 256 squares) surveyed.
    - National habitat estimates calculated as the mean habitat area per square within a class, multiplied by the land area of that class.
  - 1984 (Second GB Survey: Land Use Focus)
    - Sampling increased by 50%: 12 squares per class (total 384).
    - Built on the 1978 framework but expanded to emphasize land use and habitat mapping.
  - 1990 (CS1990: All Squares Land Classification)
    - Land Classification revised to classify every GB square using environmental surrogates; 508 squares surveyed.
    - Linked with the first Land Cover Map of GB (from satellite data); repeated vegetation quadrats from 1978.
    - Results published as Countryside Survey 1990 main report.
  - 1990s Developments (CS1990 to CS2000)
    - The classification was extended to classify all squares, driven by regional/local estimation needs.
    - A 62% correspondence found when mapping the old 1990-classified squares to a new, expanded framework; non-matching squares generally fell into neighboring classes, preserving class-level characteristics.
    - National estimates for subregions required rethinking sampling distribution due to classification changes.
  - 2000 (CS2000: Separate Country Estimates)
    - Emphasis on England & Wales vs Scotland reporting; proposals to report country-unit estimates.
    - Land Classes subdivided by country units, with aggregation where few squares remained in a country.
    - 40 strata (vs 32 previously) and additional squares to ensure adequate representation; Wales received particular attention to support Wales-only reporting.
    - 19 additional squares introduced to ensure all new classes were represented; extra allocation to England/Wales balance.
    - An uplands module added to improve habitat estimates for upland areas.
  - 2007 (CS2007: Wales-focused reporting and refinements)
    - Wales-only reporting further refined; Wales had previously been the most intensively sampled country, but needed more squares for Wales-only estimates.
    - Country-unit sub-divisions created for Land Classes (5 new Welsh-specific classes: 5w, 6w, 7w, 15w, 18w); total strata increased to 45.
    - 43 additional Welsh squares added; two English classes (5e, 15e) constrained to 4 squares each.
    - Revised Land Class maps for England with Wales and Scotland; detailed maps of sample squares available.

- Country units and Welsh upland emphasis
  - England, Wales, Scotland treated as separate units for reporting; adjustments made to ensure reliable country-specific estimates.
  - Wales required more targeted sampling due to policy and reporting needs; a Wales-specific sub-division of several Land Classes was implemented.
  - Isle of Man samples removed from country-unit estimates and replaced with new England samples for Wales reporting consistency.

- Uplands module
  - An additional module (CS2000) placed 30 squares in upland and marginal upland Land Classes to improve statistical precision for upland habitat estimates in England and Wales.

- Data products and outputs
  - Land Classification maps (illustrating revised England-with-Wales and Scotland classifications; revised England-with-Wales maps for 2000; Wales-specific maps for 2007).
  - Tables detailing the number of squares surveyed by class and year, and the sampling rates (e.g., 1:x) by class and country.
  - Acknowledgements and references detailing methodological foundations and related publications.

- National estimates: key notes
  - Changing the classification system used for national estimates affects consistency of stock estimates (GB versus country-specific reporting).
  - For CS, it is preferred to use the latest, country-specific classification framework.
  - The document provides comparative tables showing sample sizes across the original 1990 classification and the later CS2007 framework.

- Practical implications for GIS specialists
  - The ITE Land Classification provides a reproducible, multivariate stratification framework for spatial sampling and habitat estimation.
  - The approach supports country-specific (England, Scotland, Wales) reporting and enables focusing on upland and coastal/marginal habitats via additional modules.
  - Upgrading classifications can change the distribution of squares among classes; re-aggregation or subdivision may be required to maintain balanced representation.
  - The linkage between Land Classification, Land Cover mapping, and field survey data enables GIS-enabled analysis of habitat extent and change over time.
  - Detailed class maps and tabular summaries are essential for understanding sampling coverage and for producing national and regional estimates.