# The Sampling Strategy for Countryside Survey (up to 2007)

## Overview
- Traces the evolution of the ITE Land Classification and the sampling framework used for Countryside Survey from 1978 to 2007.
- Describes how stratified, random sampling of 1 km squares underpins time-series habitat and landscape estimates for Great Britain, including country-specific (England, Wales, Scotland) reporting and upland modules.
- Emphasizes the link between classification, sampling, and spatial data products (maps and tables) used to quantify habitat areas and changes.

## Core concepts and methodology
- Stratified random sampling to ensure representative coverage of ecological variation.
- ITE Land Classification as the stratification framework, built from environmental attributes (altitude, geology, climate, etc.) to define land classes.
- Sampling units: 1 km squares (center squares of grid cells, with surrounding squares linked to each center).
- Indicator Species Analysis (ISA) and related multivariate approaches used historically to derive land classes.
- Field surveys progressed across multiple decades, with each cycle refining data collection and classification to better reflect UK-wide and regional variation.
- Land Class maps underpin calculations of national habitat estimates by combining class-area with per-square habitat means.

## Timeline of key developments

### 1978 – Initial Land Classification (CS1978)
- ISA-based classification into 32 land classes from environmental data for 1228 center 1 km squares (plus surrounding squares).
- 256 squares surveyed (8 per class) across GB; habitat area estimates derived per class.
- National estimates computed as mean habitat per square in each class multiplied by the class area.

### 1984 – Second Field Survey (CS1984)
- Increased sampling within classes: 12 squares per class (384 total); eight previously visited squares retained.
- Used the 1978 classification for national estimates; data aimed at landscape changes.

### 1990 – All Squares Land Classification (CS1990)
- Land Classification revised to classify every GB square; larger-scale surrogates used due to data and computing limits.
- 508 squares surveyed; repeated vegetation quadrats and habitat mapping; linked to first Land Cover Map of GB.
- Results published with the 1990 classification; recognition that some squares changed class.

### 1998–2000 – Developments for CS2000
- Necessity to classify every GB square with a more consistent framework; 40 land classes introduced.
- Separate country estimates implemented to provide England & Wales and Scotland-specific reporting.
- Sub-division and aggregation of classes to ensure adequate country representation; additional 19–30+ squares allocated to balance representation.
- Wales-specific refinements (e.g., Land Class 17 sub-division) to improve Wales reporting accuracy.
- Upland habitat module introduced to improve statistical precision for upland estimates.

### 2007 – Developments for CS2007 (Welsh-focused reporting)
- Wales-only reporting requirements prompted further class sub-division into country-unit versions (five new Welsh classes: 5w, 6w, 7w, 15w, 18w).
- Strata increased to 45; 43 additional Welsh squares added to ensure representation of new Welsh classes.
- England adjustments: two English classes (5e, 15e) left with 4 squares per class; precision deemed acceptable per scoping study.
- Revised land-class maps and sample square distributions published for England, Wales, and Scotland.

## Separate country estimates and upland module
- Country-unit approach enables reporting for England with Wales and for Scotland, using country-specific sets of squares.
- Upland module adds targeted sampling (about 30 extra squares) in upland/marginal upland areas to boost precision for those habitats in England and Wales.

## Outputs, comparability, and data products
- National estimates are derived from class-level means and the known area of each Land Class; changes in classification over time affect cross-survey comparability.
- The report notes that switching between classifications (e.g., original 1990 vs later 2000/2007 schemes) impacts consistency; for intra-survey consistency, the latest classification is preferred.
- Table and map outputs document the distribution of survey squares by class and country, enabling GIS users to assemble time-series habitat stocks and changes.
- Table 4 (in the document) provides historical square counts under the original 1990 Land Classification to aid cross-year comparisons.

## GIS implications for map-based data products
- Land Class maps at each survey stage underpin habitat-area estimates and change detection.
- Time-series analyses require careful alignment of classifications across years (e.g., Welsh subdivisions, upland modules).
- Documentation of class definitions, sub-divisions, and sampling rates is essential for accurate GIS analyses and reproducibility.
- The evolving geography of classes (e.g., creation of Welsh-specific classes) necessitates harmonized GIS workflows when aggregating across years or countries.

## Notes on further reading and history
- The document includes extensive references, figures, and tables detailing class descriptions, sample distributions, and methodological rationales behind each survey iteration.
- Acknowledgements and bibliographic references provide additional context for the development and application of the ITE Land Classification in Countryside Survey.