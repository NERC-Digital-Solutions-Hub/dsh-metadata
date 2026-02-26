# CORINE land cover technical guide - Addendum 2000

## Overview and aims
- Addendum to the CORINE Land Cover Technical Guide (1994) to support data collection and updates.
- Introduces methodological developments for softcopy interpretation, (semi-) automated conversions, and expanded nomenclature for Central and Eastern Europe.
- Extends breadth of class descriptions with generalisation rules for mapping at 1:100 000 and clarifies landscape characteristics for better interpretation and consistency.
- Provides guidance on data governance, quality, storage, and dissemination considerations to ensure datasets are discoverable and usable.

## Production methods for CORINE data

### Hardcopy inventory
- Original method: computer-aided photo-interpretation using transparencies over 1:100 000 hardcopy satellite image prints.
- Ancillary data supports identification and confirmation of land cover features.
- Pros/cons: reliable legacy approach but prone to digitisation errors and border alignment issues; requires intermediate hardcopy products.

### Softcopy inventory
- Advances include computer-assisted interpretation directly on-screen with GIS/softcopy tools.
- Emphasises integrated handling of multiple data types (raster and vector) and on-screen editing.
- Discusses requirements for GIS engines to manage multi-dataset views, import/export standards (raster: BSQ/BIL/BIP/TIFF/geoTIFF; vector: Arc/Info formats; emphasis on interoperability).

### System components
- Text, images, and icons linked to geographic objects; editable attribute/text data.
- System customisation considerations: modularity, user interface customization, and porting to different OS environments with standards (ANSI) where feasible.
- Co-pilot software (developed by JRC/Ispra) as an integrated MS-Windows GIS for CORINE data, managing data "at continuum" in a single geodatabase and exposing ASCII-based main structures.

### Required functionalities
- Core functions for interactive display/editing of geometry, attributes, and relations.
- Image management, raster/vector integration, image enhancement.
- Geospatial and arithmetic queries; customizable database structure and indexing.
- Import/export interoperability, documentation headers, and georeferencing capabilities.
- Statistical tools for advanced analysis (e.g., principal components, spectral classifications).

## Conversion of (semi-)automated classifications
- Acknowledges limitations of automated per-pixel classifications due to image quality, relief, and the gap between pixel-level data and holistic CORINE classes.
- Conversion (spatial generalisation) can improve positional accuracy and support cartographic generalisation, but introduces complexity and potential attribute changes.
- Four main spatial generalisation approaches:
  - Reclassification (grouping into CORINE classes, often hierarchical)
  - Aggregation (merging nearby features)
  - Amalgamation (joining or dividing features with attribute/spatial considerations)
  - Smoothing and simplification (boundary adjustment and boundary simplification)
- Key caveats: results depend on feature size, output scale, and the interaction of feature size with generalisation rules; automated per-pixel accuracy remains a limiting factor.

### Methodological aspects of a conversion
- Generalisation reduces data complexity but adds potential error (location, attributes, consistency, completeness).
- Types of spatial procedures: no contiguity, contiguity-aware, and time-varying attributes.
- Emphasis on hierarchical reclassification and combined attribute/spatial amalgamation, with smoothing and boundary simplification as needed.

### Specific conversion quality issues
- Land cover is a categorical (nominal) map; two data models discussed: polygon (delineated homogeneous areas) and raster (dominant class per cell).
- Errors sources: spectral class confusion, mixed pixels, system errors, and conceptual/class definitional errors.
- Statistical properties require non-parametric/description-based approaches due to discrete nominal classes.
- Generalisation quality: no single quality measure suffices; assessment must consider scale change, intentional error introduction for simplicity, and overlay comparisons.

## Validation methodology
- Validation repeats data collection using the same sources to assess reliability and identify omission/commission errors via a confusion matrix.
- Provides guidance for stratified sampling and regional/nomenclature-based stratification to estimate correctly classified area and associated errors.

### Sampling methodology
- Stratified random sampling: strata can be by land cover item or geographic region.
- Determines the number of sampling points per stratum to achieve a desired standard error.
- Points are area-proportionate within strata; stratification reduces overall sampling error.

### Determination of sampling points
- n_h = p_h(1 - p_h) / σ_h^2 (binomial formulation) for each stratum h.
- Practical considerations include limits on points per square kilometer and handling small strata.
- A step-wise process for allocating and locating points within each stratum is described to ensure area-proportional and well-distributed sampling.

### Random sampling steps
- Step 1: area-proportional unit selection within a stratum (systematic sampling with random start).
- Step 2: placement of random sampling points within land cover units using local random/systematic methods.
- Three cases for point allocation depending on the number of points required per unit.

### Interpretation of sampling points
- Identification of land cover at or around sampling points follows the CORINE interpretation methodology, ensuring adherence to minimum mapping size and applying circular areas (1 km radius) around points for context.
- Validation can be performed on-screen using digital imagery; field surveys are often not feasible due to cost.

### Conducting validation and verification
- GIS checks for topology and boundary integrity; documentation and plotting of validation results; inclusion of metadata supporting the validation process.
- Creates a confusion matrix, estimates correctly classified area per stratum, and aggregates results by strata and nomenclature levels.
- Standard error estimation formulas provided; variance calculations account for area proportions.

### The raising (final accuracy estimation)
- Post-validation overlay to derive corrected classification rates and confusion matrices.
- Overall accuracy P is computed as a weighted sum across strata, with standard errors derived from binomial variance formulas.
- Accuracy can be reported at different aggregation levels of the nomenclature; standard errors are provided accordingly.

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

### Introduction
- Over a decade of CORINE inventory experience shows that class definitions can be refined without changing core content.
- Adds refinements and extensions to class definitions, contents, dominant objects, typical patterns, textures, representative photographs, and country-specific particularities (especially Phare countries).
- Aims to improve image analysis and interpretation at 1:100 000 scale, and to support more consistent cross-country application.

### Methodology
- Visual interpretation remains the core method; emphasis on interpretation elements and landscape objects as they appear in satellite imagery.
- The addendum provides graphic and textual presentation for class characteristics, including typical patterns, textures, representative photos, and country-specific notes.

### Characteristics and general rules
- The addendum lists and elaborates on class-specific refinements, patterns, and particularities (for example, urban fabric, industrial units, roads, water bodies, wetlands, forests, and more).
- Includes guidance on thresholds and patterns used to differentiate classes (e.g., continuous vs. discontinuous urban fabric, minimum widths for networks, extension and density criteria).

### Representative examples and patterns
- Provides illustrative examples and figures for numerous classes (e.g., urban fabric densities, vegetation textures, and typical configurations for land cover types).
- Presents particularities and generalisation rules to assist interpreters in consistently applying the nomenclature across varied landscapes.

## Notable points for Data Stewards
- Emphasises data quality, documentation, and metadata to support reuse, update cycles, and transparency.
- Highlights the importance of interoperability of formats (raster and vector) and the role of Co-pilot and similar tools in maintaining a continuous CORINE dataset.
- Shows the balance between automation and human interpretation, with explicit guidance on when automated conversions are appropriate and how to validate results.
- Provides detailed, country- and context-specific refinements to improve accuracy and consistency of land cover classification across Europe, including Central and Eastern Europe.

## References
- CEC (1994) CORINE Land Cover Technical Guide; Ferancec et al. 1995–1997; DIN standards; and related methodological works cited for background and methodology.