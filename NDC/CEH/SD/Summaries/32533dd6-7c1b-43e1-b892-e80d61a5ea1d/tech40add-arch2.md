# CORINE land cover technical guide - Addendum 2000

## Aim

- Provide additional information for those collecting and updating CORINE Land Cover (CLC) data.
- Describe methodological developments, especially softcopy interpretation, and (semi-) automated conversions to CLC nomenclature.
- Extend and refine the CLC nomenclature (notably for Central and Eastern Europe).
- Improve understanding of landscape characteristics and map generalisation rules at 1:100 000 scale.
- Facilitate monitoring and consistent data interpretation over time.

## Overview

- The addendum accompanies the CORINE Land Cover Technical Guide (CEC, 1994) and supports EEA monitoring activities.
- Highlights methodological evolution from hardcopy photo-interpretation to softcopy/GIS-based production, including Co-pilot software.
- Emphasises data quality, validation, generalisation rules, and broader accessibility of underlying data.
- Extends the nomenclature with clarifications, patterns, textures, representative photos, and country-specific particularities.

## Production methods: state-of-play

- Hardcopy inventory
  - Original CORINE method: computer-aided photo-interpretation using transparencies over 1:100,000 hardcopy satellite prints, aided by ancillary data.
  - Pros: proven approach; straightforward for mid-1980s capabilities.
  - Cons: digitisation errors, border matching issues, need for multiple intermediate products, reliance on prints.

- Softcopy inventory
  - Advances enable interpretation and digitisation in a single pass via computer tools.
  - GIS integration is central; supports viewing multiple rasters/vectors in linked windows and different color legends.
  - Emphasis on integrated systems that handle various data types, metadata, and geo-referencing.

## Key components of softcopy environments

- GIS integration
  - Vector-raster integration with broad file-format support (e.g., BSQ, BIL, BIP, TIFF, geoTIFF) and (where applicable) Arc/Info exports.
  - Considers cross-compatibility and exchange formats to improve data portability.

- Text, images, and icons
  - Linking alphanumeric attributes, images, and icons to geographic objects; editable associated texts.

- System customisation
  - Flexible architecture allowing customised user interfaces, simple applications, or advanced programming (preferably aligned with standards such as ANSI for portability).

- Required functionalities (minimal set)
  - Basic: interactive display/editing of geometry, attributes, and relations.
  - Image management: import/export, integrated raster/vector display, image enhancement.
  - Queries: geographic, arithmetic, Boolean.
  - Database management: customizable structure and spatial indexing.
  - Import/export: cross-platform data exchange.
  - Documentation: metadata headers.
  - Geo-referencing: image-to-image and GCP-based transforms.
  - Statistical tools: PCA, spectral classifications.

- Co-pilot software
  - JRC-developed integrated GIS for softcopy production, maintenance, and updating.
  - Data are managed continuously across time (no breaks).
  - Objects can be points, lines, or surfaces; highly configurable via Catalogue, Typelook, and GraphicSet structures.
  - Co-pilot is available to national CLC teams for production workflows.

## Conversion of (semi-) automated classifications

- Warnings about automated conversion limits
  - Automated per-pixel classifications are limited by image quality, atmospheric conditions, relief, and the distinction between land cover versus land use.
  - Pixel-based classifications differ from human holistic interpretation; spatial patterns and objects matter for CLC classes.
  - Conversion can succeed for positional accuracy; attribute accuracy and generalisation require careful human input.

- Methodological aspects of conversion (spatial generalisation)
  - Generalisation reduces data complexity but adds errors; map accuracy deteriorates for simplicity.
  - Types of spatial generalisation procedures:
    - Non-contiguity based
    - Contiguity-aware
    - Time-varying attribute methods
  - Common user-driven methods:
    - Reclassification (hierarchical labelling from lower to upper levels)
    - Aggregation (merging nearby features)
    - Amalgamation (joining contiguous features; attribute or spatial)
    - Smoothing (boundary relocation)
    - Simplification (reducing boundary complexity)
  - Conversion quality is influenced by per-pixel accuracy, generalisation efficiency, interpretation accuracy, and manual generalisation efficiency.
  - Major limitation: quality of automatic per-pixel classification.

- Specific conversion quality issues
  - Data models: polygon (homogeneous zones, map boundaries) vs raster (dominant class per cell).
  - Both models can be acceptable if pixel size is well below the minimum mapping unit.
  - Error sources in multispectral classification: spectral confusion, mixed pixels, system errors, conceptual misalignments.
  - Statistical properties: phase-space models aid understanding of how taxonomic definitions affect derived accuracy; many traditional statistics are not suitable due to nominal, discrete, and spatially differentiated data.
  - Generalisation properties: current quality measures often miss the added error due to generalisation; assessments should consider scale changes and the balance between simplicity and accuracy.

## Validation methodology

- Purpose: evaluate CORINE inventory reliability for unit identification and delineation, not to reassess data collection methods.
- Process: repeat data collection using random sampling with identical data sources; interpret national areas again and compare to original interpretations.
- Output: confusion matrices to identify omission/commission errors; results can be presented for specific nomenclature levels or regions.
- Stratified random sampling
  - Strata can be defined by land cover items or by geographic regions.
  - Points are drawn so every point represents equal area within its stratum.
  - Enables error rate estimation by stratum and overall accuracy via area-weighted aggregation.

- Sampling design and point allocation
  - Number of sampling points per stratum calculated using a binomial-based formula considering estimated error rate and accepted standard error.
  - Practical considerations: cap (e.g., 2 points per km²) to avoid unrealistic sampling densities in small strata.
  - Random vs systematic placement within strata; sampling within land cover units is area-proportionate.

- Stepwise sampling process
  - Step 1: select strata and determine points per stratum.
  - Step 2: draw sampling points within each stratum and land cover unit, with area-proportionate allocation.

- Interpretation and validation
  - Validation uses on-screen interpretation within a fixed scale (not exceeding 1:40,000) to preserve geometric accuracy.
  - Validation includes evaluating minimum mapping units and border effects; field surveys may be impractical, so documentation and metadata are crucial.
  - Validation output includes a plot and a summary table; topology checks are performed.

- Raising (estimation of accuracy)
  - Builds a confusion matrix from validation results; estimates correctly classified area per stratum and overall.
  - Aggregation across strata follows area-weighted schemes; standard errors are calculated via binomial variance conventions.

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

- Introduction
  - Over a decade of CORINE inventory experience prompted refinements to class definitions to reduce confusion without altering core content.
  - The addendum enhances the 1994 definitions with clarifications, contents, patterns, textures, representative photographs, and country-specific particularities.
  - Aims to improve interpretation and consistency across Europe, with emphasis on scale, patterns, and typical landscape objects.

- Methodology
  - Visual interpretation remains the basis for object identification in satellite imagery.
  - Adds detailed descriptors of landscape objects and their manifestation in imagery to aid interpreters.
  - Provides graphic and textual presentations of class characteristics, representative photographs, and patterns.

- Examples of refinements by class groups
  - Class 1.x Urban fabric (containing 111 Continuous urban fabric, 112 Discontinuous urban fabric, 121 Industrial/commercial units, 122 Road and rail networks, etc.)
  - Class 2.x Agricultural land (including 211 Non-irrigated arable land, 212 Permanently irrigated land, 221 Vineyards, 222 Fruit trees and berry plantations, 231 Pastures, 242 Complex cultivation patterns with scattered houses, 243 Land with mixed cultivation patterns, etc.)
  - Class 3.x Forests (3.1 Forests, 3.2 Shrubs/herbaceous vegetation associations, 3.3 Open spaces with little or no vegetation, 3.4 etc.; including detailed notes on crown cover thresholds and patterns)
  - Class 4.x Inland/coastal wetlands (4.1 Inland wetlands, 4.2 Coastal wetlands; definitions and typical vegetation types)
  - Class 5.x Inland and Marine waters (5.1 Inland waters, 5.2 Marine waters; guidance on water bodies, estuaries, lagoons, and related features)
- Generalisation patterns and thresholds
  - Urban fabric density thresholds (e.g., continuous urban fabric defined by high impermeable surface coverage; discontinous urban fabric defined by 30–80% impermeable coverage with specific patterns)
  - Minimum mapping sizes, buffer zones, and area-based rules for combining features (e.g., amassing small units to reach thresholds, or preserving certain features within buffers)
  - Specific notes on vegetation textures, patterns, and dominant cover for reliable class assignment

## Implications for Analysts Monitoring the Environment

- Standardisation and comparability
  - The addendum consolidates a harmonised approach for data collection, interpretation, and class assignment across Europe, enabling consistent temporal and cross-country analyses.

- Data quality and transparency
  - Emphasises robust validation (random stratified sampling, confusion matrices, area-weighted accuracy) and clear documentation of methodologies and metadata.

- Accessibility and reuse
  - Describes Co-pilot and softcopy GIS workflows that support storage, updating, and sharing of CORINE data; encourages access to underlying datasets and transparency of processing steps.

- Practical scale and applicability
  - Aligns class definitions and generalisation rules for mapping at 1:100 000, with explicit guidance on handling edge cases, borders, and small-scale generalisation challenges.

- Extended coverage and relevance
  - Extends nomenclature with Central and Eastern European country particularities, facilitating broader regional applicability and comparability.

## Note on Scope

- The document provides both methodological guidance (production, validation, generalisation) and practical class-level clarifications (Part II) to support consistent, repeatable CORINE land cover mapping and monitoring across Europe.