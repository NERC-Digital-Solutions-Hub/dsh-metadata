# CORINE land cover technical guide - Addendum 2000

## Overview
- An addendum to the CORINE Land Cover Technical Guide (CEC, 1994) to support land cover monitoring by the EEA.
- Provides extra methodological information, enhancements to the nomenclature, and mapping generalisations at 1:100 000.
- Extends guidance for softcopy (on-screen) interpretation, data integration with GIS, and central/eastern Europe adaptations.
- Adds generalisation rules, data quality considerations, and validation approaches to improve usability and consistency across European implementations.

## Part I: State-of-play production methods of the CORINE land cover database

### Introduction
- Documents the evolution from hardcopy inventory (photo-interpretation on printed transparencies) to softcopy, computer-assisted methods.
- Highlights that automated or semi-automated classifications require substantial human interpretation due to the CORINE 44-class hierarchy and landscape complexity.
- Notes that both analogue and digital approaches remain valid and can be combined.

### Hardcopy inventory
- Original method relied on computer-aided photo-interpretation using transparencies over 1:100 000 hardcopy satellite prints and ancillary data.
- Emphasises key features of CORINE units (homogeneous zones, significant surface coverage at the mapping scale, clear delimitation from surroundings).
- Digital tools were sometimes used to assess geometry and content after digitisation.

### Softcopy inventory
- Describes on-screen interpretation and digitisation using integrated GIS environments.
- Emphasises the importance of working with multiple data types (raster and vector) and flexible viewing windows, linked to different image sets.
- Underlines the need for interoperable data formats and references emerging standard exchange formats (geoTIFF for rasters; evolving vector formats).

### GIS
- Recommends integrated GIS systems capable of handling multiple data sets within the same frame of reference.
- Stresses raster-vector interoperability, broad import/export capabilities (BSQ, BIL, BIP, TIFF, geoTIFF; vector formats like DXF, Arc/Info), and data exchange standards.

### Text, images and icon information
- Supports linking non-spatial assets (texts, icons, image documents) to geographic objects with interactive display and editing capabilities.

### System customisation
- Advises evaluating software architecture, modularity, and development kits to enable advanced user interfaces or extra functionality.
- Highlights varying levels of customization, from custom interfaces to advanced applications, and recommends aiming for standards compatibility to ease porting.

### Required functionalities
- Identifies a minimal functional set:
  - Basic: display/edit geometry, attributes, and relations.
  - Image: raster/vector display, import/export, image enhancement.
  - Query: geometric, attribute, and topological queries.
  - Database management: geographic indexing and structure customization.
  - Import/export: cross-platform data exchange.
  - Documentation: file structure metadata.
  - Georeferencing: image-to-image and GCP-based transforms.
  - Statistical tools: components like principal components and spectral classifications.
- Suggests overlaying legends across data types for user-friendliness.

### Co-pilot software
- Describes the JRC Co-pilot system for softcopy CORINE data maintenance (MS Windows 3.1/95).
- Data are managed in a continuum GIS database, with geographic objects as basic units (points, lines, surfaces) defined by user Catalogues, Typelook, and GraphicSet structures.
- Notes availability of Co-pilot from JRC for national CORINE teams.

### Conversion of (semi-) automated classifications
- Warns about limitations of automated classification: image quality variability, difference between land cover vs. land use, and the gap between pixel-based classifications and human holistic interpretation.
- Reports that conversions can be successful for positional accuracy but require careful handling of thematic content.
- Outlines generalisation techniques (see 4.1) and quality concerns (see 4.2).

#### 4.1. Methodological aspects of a conversion
- Spatial generalisation reduces data complexity at the cost of some accuracy.
- Outlines three procedure types:
  - No contiguity considerations
  - Contiguity-aware
  - Time-varying attributes
- Describes common user-controlled methods:
  - Reclassification (hierarchical relabelling within the 44-class system)
  - Aggregation (merging adjacent features)
  - Amalgamation (joining or dividing features; semantic vs. spatial amalgamation)
  - Smoothing (boundary relocation to reduce raster step effects)
  - Simplification (reducing boundary complexity)
- Emphasises that accuracy in automatic classifications, visual interpretation, and generalisation collectively determine final quality.

#### 4.2. Specific conversion quality issues
- Explains land cover as a nominal, discrete map across polygon and raster models.
- Details sources of error: spectral class confusion, mixed pixels, system errors, conceptual/class coherence errors.
- Discusses phase-space modelling and the relevance of per-pixel vs. contextual generalisation for quality assessment.
- Highlights generalisation quality trade-offs: scale change increases error but improves legibility; many traditional quality measures do not account for these generalisation errors.

### Validation methodology
- Validation repeats data collection with the same sources via random sampling to produce a confusion matrix.
- Allows assessment of omission/commission errors per class and at different nomenclature levels.
- Enables stratified analysis by region or nomenclature level and computes weighted accuracy estimates.
- Provides formulas for estimating sampling points per stratum, error rates, and standard errors; includes aggregation across strata to determine overall accuracy.
- Includes methods for calculating variances and standard errors, with area-based weighting for total accuracy.

### References
- CEC 1994 CORINE Land Cover Technical Guide
- DIN/Norms and related methodological/statistical references
- Earlier CORINE quality and generalisation studies

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

### Introduction
- Reflects a decade of visual interpretation experience with Landsat and SPOT imagery.
- Refines or extends definitions without altering the core content of the original class definitions.
- Aims to enhance uniform European nomenclature with country-specific particularities, patterns, textures, representative photographs, and guidance on interpretation at 1:100 000.

### Methodology used for the compilation of the addendum
- Continues to base class identification on analysis of interpretation elements and landscape objects as shown in imagery.
- Provides enhanced descriptions that include objects, their dominant patterns and textures, and representative photographs to assist interpreters.

### Class characteristics and generalisation guidance (illustrative scope)
- Presents refined or extended definitions, including:
  - Dominant objects within each class
  - Typical arrangement patterns and textures
  - Representative photographs and country-specific particularities
- Includes guidance on extending and generalising across a 1:100 000 scale framework.
- Covers major classes (examples shown in the text include):
  - 1.x Urban fabric (e.g., 111 Continuous urban fabric; 112 Discontinuous urban fabric; 121 Industrial or commercial units; 122 Road and rail networks)
  - 2.x Agricultural and arable classes (e.g., 211 Non-irrigated arable land; 212 Permanently irrigated land; 221 Vineyard-related classes; 222 Fruit trees and berry plantations)
  - 3.x Forests and natural vegetation (e.g., 311 Broad-leaved forests; 312 Coniferous forests; 321 Natural grasslands; 322 Moors and heathland; 323 Sclerophylous vegetation; 324 Forest degradation and clear-cuts)
  - 4.x Inland and coastal wetlands and waters (e.g., 411 Inland wetlands; 421 Salt marshes; 422 Salines; 431 Inland waters; 512 Inland water bodies; 523 Sea water)
- Provides classification thresholds and generalisation rules, including:
  - Density thresholds for urban fabric (e.g., 80% impermeable surface for 111; 30% to 80% impermeable for 112)
  - Area-based thresholds for consolidating units (e.g., 25 ha minimums and boundary considerations)
  - Patterns and texture descriptions to aid interpretation
  - Specific notes for complex cultivation patterns, agro-forestry, and mixed parcels
- Includes extensive visual and pattern descriptions to assist consistent interpretation across Europe, with emphasis on Central and Eastern European contexts.

### Representative examples (illustrative)
- 1.1 Urban fabric: density and texture cues for distinguishing continuous vs. discontinuous urban forms; subtypes for housing estates and road networks.
- 2.x Agricultural: differentiation of arable land, permanent crops, pastures, and mixed cultivation patterns; notes on vineyards, olive groves, hops, and irrigation contexts.
- 3.x Forests: distinctions among broad-leaved, coniferous, and mixed forests; notes on altitude-related patterns and shrub/grass undergrowth.
- 4.x Wetlands and waters: inland wetlands, coastal wetlands, salt marshes, lagoons, and water body patterns with textures and dominant vegetation.

### Purpose for GIS specialists
- Provides detailed, practical refinements to improve on-screen interpretation, class assignment accuracy, and consistency with the CORINE 1:100 000 framework.
- Supports better generalisation decisions and more reliable cross-country comparisons, including Central and Eastern Europe.
- Enhances interpretive guidance with textures, representative images, and explicit pattern descriptions.

## Practical implications for GIS Specialists
- When producing CORINE Land Cover data, balance automated classification with expert interpretation, especially given the 44-class hierarchy.
- Leverage softcopy GIS workflows and Co-pilot-like tools to manage and update the CORINE inventory efficiently.
- Apply validated sampling and robust validation (stratified random sampling, confusion matrices, area-weighted accuracy) to quantify reliability.
- Use the Part II addendum guidance to refine class definitions, update patterns and textures, and apply consistent generalisation rules at 1:100 000 scale, with attention to regional particularities.