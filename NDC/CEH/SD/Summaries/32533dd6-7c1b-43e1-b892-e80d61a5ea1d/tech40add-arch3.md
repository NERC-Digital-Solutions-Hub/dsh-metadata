# CORINE land cover technical guide - Addendum 2000

## Overview and purpose
- Addendum to the CORINE Land Cover Technical Guide (1994) to support ongoing land cover monitoring.
- Aims to provide additional information for data collection and updating, describe new softcopy methodologies, extend nomenclature for Central and Eastern Europe, add generalisation rules for 1:100 000 mapping, and improve understanding of landscape characteristics.
- Emphasises a shift from hardcopy photo-interpretation to computer-based, GIS-enabled workflows; highlights data governance, metadata, openness, and data sharing as essential but sometimes challenging.

## Part I: State-of-play, production methods and related topics

### Hardcopy inventory
- Original CORINE workflow relied on computer-aided photo-interpretation using 1:100 000 hardcopy transparencies over satellite image prints, with ancillary data.
- Strengths: proven approach; straightforward interpretation with physical overlays.
- Limitations: digitisation errors, border matching issues, duplication of intermediate outputs (transparencies, prints), and potential data handling inefficiencies.
- Ancillary data remains essential for accurate interpretation.

### Softcopy inventory
- Modern approach uses on-screen interpretation and digitisation within GIS environments.
- GIS considerations include multi-dataset management, support for raster and vector formats, and progressing toward standardized exchange formats (geoTIFF for rasters; evolving standards for vectors).
- Emphasises integration of text, images, and icons linked to geographic objects; editable associated texts; flexible data management.

### System customization and functionalities
- Software ecosystems vary (PC-based, workstation-based); advocates for modular, standards-aware design to facilitate porting and future enhancements.
- Required functionalities include: interactive geometry/attribute editing, image management and display, various query capabilities, a customizable database with geographic indexing, robust import/export, documentation, georeferencing, and statistical tools.

### Co-pilot software
- JRC’s Co-pilot provides an integrated GIS environment for CORINE Land Cover data maintenance, updating, and continuum data management (data from different times/maps in one database).
- Data model emphasizes geographic objects (points, lines, surfaces) with catalogues, typelook definitions, and ASCII-based main data structures for ease of editing.
- Available through national CLC production teams to support standardized workflows.

## Part I: Conversion of (semi-) automated classifications

### Methodological aspects
- Automated classification is valuable but limited by variable image quality, ground conditions, and the gap between pixel-based classifications and human holistic interpretation.
- Automation generally yields good positional accuracy; attribute accuracy depends on subsequent interpretation.
- Spatial generalisation (simplification of data) reduces complexity but adds error; three generalisation types:
  - No contiguity considered
  - Contiguity considered (area relationships with surroundings)
  - Temporal variation considered

### Generalisation steps used (UK/Sweden/Finland examples)
- Reclassification: regrouping into CORINE classes, often hierarchical.
- Aggregation: merging nearby small features into a single area.
- Amalgamation: joining or dividing contiguous features based on semantic proximity.
- Smoothing and simplification: boundaries adjusted to remove raster-induced jaggedness and reflect significant trends.

### Specific conversion quality issues
- Land cover is categorical; data models include polygon (homogeneous areas) and raster (dominant class per cell).
- Key error sources: spectral class confusion, mixed pixels, system errors, and conceptual differences between land cover and land use.
- Phase-space modeling helps study the relationship between land cover accuracy and measures derived from the data.
- Generalisation quality is hard to measure with standard metrics; tests, overlays, and visual checks are essential.

## Part I: Validation methodology

### Validation purpose
- Validate CORINE inventory against the same data sources used in the original collection, to inform users about reliability and item-level validity.
- Produce a confusion matrix to identify omissions and commissions and to enable level-specific accuracy assessments.

### Sampling methodology (5.1)
- Stratified random sampling across land cover items and/or geographic regions.
- Determines strata, allocates sampling points per stratum, and overlays digital maps to estimate error surfaces.
- Enables precision control: standard errors can be reduced by stratification.

### Determining the number of sampling points (5.2)
- n_h (points per stratum) is derived from a binomial formulation based on estimated error rate p_h and acceptable standard error σ_h.
- Practical guidance includes caps (e.g., max 2 points per km²) to avoid impractical sample densities in small strata.
- Higher estimated error or required precision increases the number of points.

### First and second steps of random sampling (5.3)
- Step 1: Area-proportionate, systematic selection of land cover units within strata; determines how many points per unit.
- Step 2: Location of points within units via pure random sampling, systematic sampling, or grid-based approaches depending on the number of points required.

### Interpretation of sampling points (5.4)
- Interpretation proceeds level-by-level (from broad to detailed) with ancillary data evaluated in depth.
- Validation interpretation is performed on-screen against digital imagery at scales no larger than 1:40 000 to preserve context and accuracy.
- Validation should be conducted by an independent interpreter familiar with CORINE methodology, ideally without knowledge of the sampling point locations.

### The raising (accuracy estimation) (5.5)
- Builds a confusion matrix from validation results to estimate correctly classified area per stratum and overall accuracy.
- Formulas allow aggregation across strata and across nomenclature levels; standard errors are computed to reflect sampling variability.
- Stratification can align with geographic regions or nomenclature levels; aggregation across strata is weighted by area.

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

### Introduction and purpose
- Over a decade of experience shows that most CORINE classes can be refined without altering core definitions.
- Adds refinements to definitions, explicit inclusions/exclusions, generalised patterns, representative photographs, class particularities (including Phare country specifics), and guidance for interpretation at scale 1:100 000.
- Aims to improve image interpretation and landscape understanding; supports consistent cross-country mapping and time-series comparisons.

### Methodology for the addendum
- Visual interpretation remains central; emphasizes analysis of landscape objects and their image manifestations.
- Provides enhanced class characteristics (texture, pattern), dominant objects, representative patterns, and photographs to aid interpreters.
- Covers a broad range of classes (from 1.1 Urban fabric through 5.2 Marine waters), with extensive guidance on features, thresholds, and generalisation rules.

### Notable content and generalisation guidance
- The addendum includes threshold-based and pattern-based refinements for numerous classes, including:
  - Urban fabric (1.x) and its density distinctions (e.g., continuous vs discontinuous).
  - Agricultural classes (2.x) with detailed subtypes and extension criteria.
  - Forest and non-forest vegetation (3.x) with definitions for forests, moors, sclerophyllous vegetation, and related patterns.
  - Wetlands and water bodies (4.x, 5.x) with refined coastal/inland wetland interpretations and water body classifications.
- Provides guidance on how to map transitional areas, buffer zones, and complex parcel patterns, along with generalisation rules to ensure consistency across countries.
- Includes representative textures, patterns, and illustrative figures to support consistent interpretation and classification.

## Practical implications for monitoring frameworks

- Data governance and openness: Clear emphasis on metadata, data sharing, and openness; potential barriers identified (privacy, provenance, and governance).
- Data workflow modernization: Moving from hardcopy to softcopy GIS-based workflows improves accuracy, repeatability, and efficiency; need for interoperable data formats (geoTIFF, vector formats).
- Quality assurance and validation: Robust validation framework using stratified random sampling and confusion matrices; explicit methods to quantify and communicate uncertainty to policy users.
- Classification consistency: Part II provides detailed, harmonised definitions and patterns to support cross-country comparability and longitudinal monitoring.
- Scalable, adaptable monitoring: The framework supports updating CORINE data across time and space (including Central and Eastern Europe) and accommodates new data sources and generalisation needs.
- Practical implementation notes: Emphasises scale considerations (1:100 000), minimum mapping sizes, and the balance between generalisation and accuracy, which are critical for policy-relevant reporting.

## Relevance to environmental health monitoring policy
- Enables consistent, transparent assessment of land cover change, urbanisation, vegetation, wetlands, and water resources—key indicators for environmental health and policy evaluation.
- Provides a structured approach to measure accuracy and uncertainty, strengthening the reliability of health-related environmental indicators derived from land cover data.
- Supports decision-making on land-use planning, urban development, habitat protection, flood risk assessment, and ecosystem health by delivering harmonised, well-documented classification schemes and validation results.