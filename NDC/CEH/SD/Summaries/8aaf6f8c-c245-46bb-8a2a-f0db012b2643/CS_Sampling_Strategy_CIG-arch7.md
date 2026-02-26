# The Sampling Strategy for Countryside Survey

- The document outlines the evolution of the sampling framework and the ITE Land Classification used to stratify field surveys for Countryside Survey GB up to 2007.
- It situates current methodology within 30 years of development, showing how sampling and classification decisions affect spatial data products and national estimates.

## Key concepts for GIS workflows

- ITE Land Classification as the stratification framework for GB ecological sampling.
- Use of 1 km squares as sampling units, with the centre square classified (plus surrounding squares for context in early years).
- Stratified, random sampling to ensure representative coverage of land types and ecological variation.
- Outputs used to estimate national habitat areas by combining class area with mean habitat extent per class.

## Evolution of the sampling framework (timeline)

- 1978 (Initial version)
  - ISA-based land classification produced 32 classes.
  - Centre 1 km squares classified; plus four surrounding squares classified (total 6039 km2 represented).
  - 8 squares per class sampled (total 256), enabling national estimates by class means multiplied by class area.
- 1984 (Second field survey)
  - Sampling increased by 50%: 12 squares per class (total 384).
  - Eight previously visited squares retained.
- 1990 (CS1990; All Squares Land Classification)
  - All GB squares classified; 508 squares surveyed.
  - Land Cover Map linked; some squares reclassified; results published for CS1990.
- 2000 (CS2000)
  - Land Classification expanded to cover every GB square using surrogates for climate/geology/physiography.
  - Separate country estimates introduced (England with Wales, Scotland, and later Wales).
  - Class subdivisions and aggregations created 40 strata; 19 additional squares added; upland habitat module added (30 squares) to boost upland estimates.
- 2007 (CS2007)
  - Wales-only reporting requirements led to further adjustments.
  - Creation of country-unit classes (5 new Wales/England versions: 5w, 6w, 7w, 15w, 18w) increasing strata to 45.
  - Wales received 43 additional squares; some English classes reduced to 4 squares per class but deemed acceptable for precision.
  - England/Wales/Scotland revised class maps and sampling framework implemented.

## Country-level reporting and sampling adjustments

- Separate country estimates introduced to improve reporting accuracy for England with Wales, Scotland, and Wales-alone targets.
- Land Classes subdivided by country unit; where necessary, classes aggregated within a country to maintain representation.
- Wales-specific sampling increased to ensure adequate representation of Welsh classes (minimum 6 squares per new Welsh class).
- Upland habitat module expanded sampling in England and Wales to improve statistics for upland habitats.

## Outputs and estimation methods

- National estimates calculation
  - For GB: mean habitat extent per square within each Land Class × total area of that Land Class.
- Country-level estimates
  - Use country-specific subdivisions/aggregations of Land Classes.
  - Additional sampling modules (e.g., upland) to strengthen country-specific precision.
- Data products include land-class maps and spatial locations of sampled squares across surveys, enabling time-series analyses with harmonized classification schemes.

## Practical implications for GIS practitioners

- Data consistency over time
  - Changing Land Classification schemes (32 → 40 → 45 classes) and country-unit subdivisions require careful harmonization for time-series analyses.
- Spatial data layering
  - Land Class maps at each survey year; country-unit layers (England with Wales, Scotland, Wales-only) for targeted analyses.
- Sampling design awareness
  - Knowledge of how many squares per class and per country influences error terms and uncertainty in derived spatial statistics.
- Upstream data preparation
  - When combining multiple CS datasets, align classifications and class boundaries to ensure comparability; account for upland and Wales-specific modules where relevant.

## Endnotes and references

- The document provides a historical appendix and references detailing foundational works on the ITE Land Classification and Countryside Survey publications through 2007 (including 1990, 1993, 2000, and 2007 reports).