# The Sampling Strategy for Countryside Survey (up to 2007)

- Overview
  - Historical account of the ITE Land Classification and the evolving sampling framework for Countryside Survey (CS) GB field surveys from 1978 to 2007.
  - Describes how stratification, classification, and sampling design have been refined to support national and country-specific habitat estimates.
  - Emphasises the link between previous time-series data and current methodology, and the implications for GIS-based data products and change analysis.

- Core concepts for GIS practice
  - ITE Land Classification: environmental-attribute-based stratification used to divide GB into land classes for sampling.
  - Stratified, random sampling: aims to ensure representative coverage across diverse landscapes and reduce bias.
  - Indicator Species Analysis (ISA): multivariate approach used to form initial land classes from environmental data.
  - Sample unit and frame: primary sampling unit is a 1 km square; initial approach used the centre square of a 15 x 15 km grid, with surrounding squares also classified.
  - Temporal consistency vs. evolution: changes in classification and country-specific breakdown affect comparability across CS surveys.

- Timeline and evolution of the sampling framework
  - 1978 (Initial Land Classification and field survey)
    - ISA used to create 32 land classes from environmental data of 1228 centre 1 km squares; 4 surrounding squares per centre were added (total 6039 km squares).
    - Field survey: 8 squares per land class (256 total); national habitat estimates calculated from mean habitat area per square within each land class.
  - 1984 (Second land-use survey)
    - Sampling expanded to 12 squares per land class (384 total), retaining the 1978 framework; eight squares remained from 1978.
  - 1990 (All Squares Land Classification and third survey)
    - Land Classification revised to cover every GB square; results linked to the first full GB Land Cover Map.
    - CS1990: 508 squares surveyed; added land-use and habitat mapping elements; repeat of some vegetation quadrats.
    - Classification adjustments were conservative but caused some shifts in square-class assignments.
  - 1998–2000 (Developments toward the CS2000 framework)
    - New approach to classify every GB square using surrogates (climate, geology, physiography) with multiple classification attempts; best match achieved with 62% correspondence to the original 1990 classes.
    - Resulted in distortions in class representation; planning adjusted to restore representation in the sampling frame.
    - CS2000 established separate country estimates by subdividing land classes into England-with-Wales and Scotland versions and increasing the overall strata to 40; added 19 extra squares (plus 11 for balancing England vs Wales) and introduced upland habitat sampling.
  - 2007 (CS2007 adjustments for Wales and overall frame)
    - Wales-only reporting requirement led to further Wales-specific class subdivisions (5 new Welsh sub-classes: 5w, 6w, 7w, 15w, 18w) and an expanded 45 strata.
    - Additional Wales squares (43) to ensure adequate representation; England classes 5e and 15e retained only 4 squares each due to precision considerations.
    - Revised class maps for England-with-Wales and Scotland; results summarized in CS2007 tables/figures.

- Country-specific sampling and upland module
  - Separate country estimates
    - From CS2000 onward, countries (England & Wales, Scotland) are estimated separately using country-specific class subdivisions and allocations.
    - Adjustments include class subdivision, aggregation, and targeted additional squares to ensure adequate representation in each country unit.
  - Wales-focused adjustments (CS2007)
    - Additional Welsh subdivisions and Wales-specific sampling to improve precision for Wales-only reporting.
  - Upland module (CS2000)
    - Extra survey effort (30 squares) in upland/marginal upland classes to improve habitat estimates in upland areas of England and Wales.

- Data products and national estimates
  - National estimates can be produced using the latest classification or the original 1990 Land Classification; the 2006 scoping study notes that changing classifications affects consistency of national stock estimates.
  - Table and map references illustrate changes in numbers of squares, strata, and sampling rates across surveys; CS1990, CS2000, and CS2007 reflect progressively refined country-specific sampling.

- Practical implications for GIS and data work
  - Be aware of the classification version used for any CS estimate or map layer, as shifts in land classes alter boundaries and representativeness.
  - When integrating across survey years, track land-class definitions (including country-unit subdivisions) to maintain comparability.
  - For Wales-specific or England-with-Wales analyses, use the corresponding country-unit classifications and sampling frames from CS2000 onward.
  - Upland modules introduce additional samples in targeted strata—these may affect regional estimates and uncertainty in GIS analyses.

- Acknowledgements and references
  - Acknowledges contributions from project staff and statistical guidance; includes extensive further reading and historical documentation on the ITE Land Classification and Countryside Survey methodology.

- Endnotes and further reading
  - Includes notes on national-estimate consistency and a detailed set of references documenting the development and application of the ITE Land Classification across CS surveys.