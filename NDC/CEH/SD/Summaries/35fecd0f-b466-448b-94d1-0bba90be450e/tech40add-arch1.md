# CORINE land cover technical guide - Addendum 2000

## Aim and scope
- Addendum to the CORINE Land Cover Technical Guide (1994) to support land cover monitoring by the EEA.
- Provides additional information not in the original guide, describes methodological developments (soft copy interpretation, semi-automated conversions), enhances nomenclature (including Central and Eastern Europe), extends mapping rules to 1:100 000, and clarifies landscape characteristics.

## Part I: State-of-play and production methods

### Hardcopy inventory
- Early CORINE approach used photo-interpretation on 1:100 000 hardcopy satellite image prints overlaid with transparencies.
- Ancillary data aided interpretation; manual digitisation introduced border and boundary challenges.
- Still valuable but prone to digitisation errors; relied on intermediate hardcopy products.

### Softcopy inventory
- Modern approach uses softcopy interpretation and digitisation in a single pass, integrating with GIS.
- Emphasizes on-screen interpretation and the benefits of computer-based tools.
- Highlights the role of integrated GIS for handling multiple raster and vector datasets, and various raster/vector formats (e.g., geoTIFF, BSQ/BIL/BIP).

### GIS, data and information types
- Emphasizes linking geographic objects with alphanumeric attributes, textual information, and image/icons.
- Supports rich data connections (texts, images, icons) and editable attribute information.

### System customization and required functionalities
- Software should be modular and extensible, allowing customized user interfaces and applications.
- Minimal functional requirements include: interactive editing/display of geometry and attributes; image management; diverse query capabilities; a flexible database that supports indexing and data exchange; documentation and georeferencing tools; and statistical capabilities.

### Co-pilot software
- JRC’s Co-pilot provides an integrated GIS environment for softcopy CORINE land cover management, updating, and maintenance.
- Data are managed in a continuum across maps and time, with objects (points, lines, surfaces) and user-defined catalogues for object types and graphical lookups.
- Distributed to national CLC teams as a key toolkit.

## Part I: Conversion of (semi-)automated classifications

### Methodological aspects
- Automated conversions from per-pixel classifications face limitations due to:
  - variable image quality and ground conditions,
  - differences between land cover as a category and land use as functional intrusion,
  - the gap between pixel-level classification and human holistic interpretation.
- Conversion can yield accurate positional generalisation but may struggle with attribute accuracy; requires careful supervision.

### Quality issues
- Data models: polygon (homogeneous areas) vs raster (dominant class per pixel) have implications for conversion quality.
- Main error sources: spectral class confusion, mixed pixels, system errors, and conceptual misalignments between classes.
- Generalisation reduces data complexity but increases overall error; quality measures must account for the effects of generalisation on location and classification.

## Part I: Validation methodology

### Validation purpose
- Assess the CORINE inventory’s reliability for unit delineation and classification according to CORINE rules.
- Provide users with information on item-level validity and overall accuracy.

### Sampling and stratification
- Validation uses random sampling with stratification, allowing assessment across land cover items or geographic regions.
- Sampling plan derives from an initial digital land cover map and a target number of sampling points per stratum.

### Determination of sampling effort
- The number of sampling points per stratum depends on an estimated error rate and an accepted absolute standard error.
- A cap is suggested (e.g., no more than 2 points per km²) to balance practicality and precision.
- The approach aims to minimise standard error and enable errors to be attributed to strata or nomenclature levels.

### Random sampling steps
1) First step: area-proportionate sampling of land cover units within strata, using a step-size and a systematic-cum-random selection to allocate points to units.
2) Second step: determine sampling point locations inside units with methods ranging from pure random within unit bounds to systematic-plus-random approaches for multiple points; grid-based methods are used when many points are needed.
3) Interpretation: interpret points in a controlled, on-screen manner following CORINE methodology, typically with a circular area (1 km radius) around each point and without knowing the sampling location to avoid bias.

### Interpretation and validation execution
- Interpretation progresses from larger to smaller units, with final identification aligned to the nomenclature levels.
- Validation includes a detailed documentation process, a plotting overlay for error verification, and checks for topology and minimum mapping size.
- A confusion matrix is produced to quantify omission and commission errors per stratum and per nomenclature level.

### Raising and accuracy estimation
- After validation, coverage is overlaid with sampling points to compute correctly classified area percentages per stratum.
- Overall accuracy is weighted by stratum area; standard errors are computed for estimators using binomial formulations.
- Aggregation across strata or nomenclature levels is possible, with appropriate area-weighted summations and error propagation.

## Part I: References
- Core methodological and statistical sources (CEC 1994, DIN 1994, and multiple technical papers) cited for guiding validation and generalisation procedures.

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

### Introduction and purpose
- Builds on a decade of CORINE experience to refine class definitions without changing their core meanings.
- Adds clarifications to improve interpretation accuracy, including:
  - refined or extended class definitions,
  - lists of included/excluded cases,
  - representative patterns and textures,
  - typical photographic examples,
  - country-specific particularities (Phare countries).

### Methodology
- Visual interpretation of Landsat and SPOT imagery remains central; emphasis on interpretation elements and landscape-object relationships.
- The addendum provides graphic and text descriptions for scale 1:100 000 mapping, improving consistency across Europe.

### Specifications and sample content
- Offers detailed guidance for numerous classes (notably urban, agricultural, forest, and wetland categories).
- Includes density/extension thresholds (e.g., urban fabric thresholds, impervious surface criteria) and pattern-based generalisation rules.
- Presents representative patterns, textures, and photographs to aid interpreters.
- Addresses class particularities and generalisation rules to apply in various geographic contexts (including Phare countries).

## Implications for analysts and data users
- The Addendum documents the transition from hardcopy to softcopy GIS-enabled workflows, with an emphasis on data provenance, metadata, and reproducibility.
- Validated CORINE data rely on stratified random sampling, careful interpretation, and transparent error estimation, enabling quantified confidence in land cover outputs.
- The Part II nomenclature addendum improves cross-country consistency and interpretation, with practical rules for mapping at 1:100 000 and guidance on class patterns and textures.