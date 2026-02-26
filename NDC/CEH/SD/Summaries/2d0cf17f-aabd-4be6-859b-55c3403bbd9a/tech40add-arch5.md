# CORINE land cover technical guide - Addendum 2000

## Overview and purpose
- Addendum to the CORINE Land Cover (CLC) Technical Guide (1994) to support ongoing land cover monitoring by the European Environment Agency.
- Provides new methodological guidance, especially softcopy interpretation, semi-automated conversions, and enhanced nomenclature descriptions.
- Extends guidance for Central and Eastern Europe, adds generalisation rules for mapping at 1:100,000, and clarifies landscape content understanding.

## Production methods and data workflow

- Evolution from hardcopy inventory (printouts and transparencies) to softcopy, GIS-enabled production.
- Hardcopy inventory:
  - Computer-assisted photo-interpretation of satellite images with overlaid transparencies.
  - Use of ancillary data to confirm land cover features.
- Softcopy inventory:
  - Integrated GIS approaches enabling simultaneous handling of raster and vector data.
  - Emphasis on on-screen interpretation, flexibility, and efficiency.
- GIS and software considerations:
  - Integrated systems (vector/raster) with multi-window support, broad import/export formats (e.g., raster: BSQ/BIL/BIP, TIFF/geoTIFF; vector: Arc/Info formats, DXF).
  - Text, images, and icons linked to geographic objects; editable attribute and text data.
- System customization:
  - Consider modular architectures, user interface customization, and porting to different environments (ANSI/OS standards).
- Co-pilot software:
  - JRC’s Co-pilot provides an integrated GIS for CLC maintenance and updating, managing data "at continuum" across map editions, stored in ASCII structures and catalogues.
- Data management implications:
  - Emphasis on long-lived data governance: versioning, interoperability, and enabling updates across time.

## Conversion and generalisation of classifications

- Conversion approaches acknowledge limitations of automatic classification due to image quality, ground truth, and the gap between pixel-based classifications and holistic human interpretation.
- Methodological aspects:
  - Spatial generalisation reduces data complexity but increases certain errors; three main procedure types:
    - No spatial contiguity considered
    - Spatial contiguity considered
    - Time-varying attributes
  - Common user-driven methods:
    - Reclassification (hierarchical relabelling within the 44 CLC classes)
    - Aggregation (merging adjacent units)
    - Amalgamation (joining/merging or dividing contiguous features)
    - Smoothing (boundary adjustments)
    - Simplification (reducing boundary complexity)
- Conversion quality issues:
  - Land cover is a categorical variable with polygon and raster representations; pixel size must be small relative to minimum mapping units; conversion errors arise from spectral confusion, mixed pixels, and system/conceptual errors.
- Generalisation effects on data quality:
  - Generalisation adds simplicity and legibility at the cost of location and attribute precision; quality assessment must consider both inherent data error and generalisation-induced error.

## Validation and accuracy assessment

- Validation aims to evaluate inventory reliability for CORINE methodology, not to reassess data collection methods.
- Random sampling with potential stratification:
  - Stratified random sampling across land cover items and/or geographic regions.
  - Points are used to build confusion matrices to assess omission and commission errors.
- Sampling details:
  - Determine the number of points per stratum based on estimated error rate and acceptable standard error.
  - Points are area-proportionally allocated; multiple sampling within units is used to estimate error rates.
  - Validation includes on-screen interpretation, with strict adherence to minimum mapping size and overlaid GIS comparisons.
- Interpretation and verification:
  - Validation interpreters work with contemporary digital imagery at a fixed scale (not exceeding 1/40,000) and assess land cover at multiple hierarchical levels.
  - Verification includes topology checks, error plots, and documentation of errors for transparency.
- The raising:
  - After validation, results yield a confusion matrix and area estimates with associated standard errors, aggregated across strata and nomenclature levels.

## Data quality and statistical considerations

- Statistical properties:
  - Phase-space modeling and non-parametric approaches preferred due to discrete, nominal class structure.
- Generalisation quality considerations:
  - Quantitative measures for generalisation are limited; overlay and visual checks are essential.
  - The impact of scale change on accuracy is central to assessing generalisation outcomes.

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

- Introduction and purpose:
  - Refines class definitions without altering core content; adds clarifications to exclude confusions and improve interpretation across Europe.
- Methodology:
  - Emphasizes landscape object–image manifestation analysis; builds a visual catalog of class characteristics to aid interpreters.
- Content scope:
  - Adds texture, pattern, representative photographs, and class particularities for each CORINE class, including urban fabric (1.x), agricultural (2.x), forest (3.x), and other land cover categories (4.x, 5.x).
- Notable refinements:
  - Specific thresholds and generalisation patterns (e.g., urban fabric density, density cut-offs, and patterns for class boundaries).
  - Representative examples and guidance aimed at Phare countries and broader Europe.
- Practical outcome:
  - Enhanced guidance for consistent interpretation and mapping across different national contexts.

## Practical data governance considerations for Data Stewards

- Data model and interoperability:
  - Maintain clear documentation of polygon vs raster representations and their conversion pathways.
  - Ensure compatibility with standard formats (geoTIFF for rasters, Arc/Info–DXF for vectors) and robust metadata describing provenance.
- Metadata and lineage:
  - Capture version history, methodology choices (hardcopy vs softcopy, Co-pilot usage), calibration decisions, and validation procedures.
- Data quality and validation:
  - Implement and document validation workflows, sampling strategies, and error estimates (confusion matrices, stratum-specific and aggregated accuracy).
  - Track generalisation effects and maintain transparency about scale-dependent limitations.
- Update and governance:
  - Establish update protocols for datasets across time, including embargoes, data availability, and compatibility with national updates.
- Documentation and accessibility:
  - Provide clear user guidance on data standards, interpretation rules, and class definitions (Part I and Part II guidance).
  - Ensure data and supporting materials (methodologies, patterns, textures, and examples) are accessible to data users and curators.
- Cross-border and regional consistency:
  - Apply generalized mapping rules and class definitions consistently across Europe, accounting for regional particularities (as detailed in Part II).

## References
- Core methodological references for CORINE Land Cover, validation, generalisation, and related technical guidance (CEC, 1994; DIN 1994; Perdigao et al., 1997; Feranec et al., 1995/1996; Jaakolla, 1997; etc.).