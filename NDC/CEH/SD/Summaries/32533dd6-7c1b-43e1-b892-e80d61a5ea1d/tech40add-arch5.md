# CORINE land cover technical guide - Addendum 2000

- Aimed to support updating CORINE Land Cover (CLC) data with additional information not in the 1994 guide.
- Describes new methodological developments for producing the CLC database, especially softcopy (on-screen) interpretation and (semi-) automated pixel-to-class conversion.
- Extends the CLC nomenclature for Central and Eastern Europe and provides generalisation rules for mapping at 1:100 000 scale.
- Improves understanding of landscape characteristics and class contents to aid interpretation and data governance.

## For Data Stewards: Purpose, scope, and governance implications

- Clarifies data collection and update processes to ensure consistent governance, accuracy, and metadata.
- Emphasises transparency about data production methods, scale, and generalisation rules to support discoverability and reuse.
- Provides validation and accuracy assessment procedures to inform data quality expectations for users.

## Part I: State-of-play and production methods

- Hardcopy inventory
  - Early CORINE method: computer-assisted photo-interpretation using 1:100,000 hardcopy satellite image prints with transparencies and ancillary data.
  - Strengths: simple and robust; weaknesses include potential digitisation errors and border-matching challenges.
- Softcopy inventory
  - Advances to softcopy interpretation using computer tools, GIS, and on-screen digitising.
  - Acknowledges limitations of fully automated approaches due to class heterogeneity and spatial patterns; human interpretation remains essential.
- Softcopy and GIS considerations
  - Integrated GIS systems manage raster and vector data, support multiple datasets, and enable overlay and legend management.
  - Emphasis on interoperability: need for data formats like geoTIFF, BSQ/BIL/BIP, Arc/Info exports, and evolving standard exchange formats.
  - Association of geographic objects with alphanumeric attributes, images, icons, and text; supports metadata and documentation linkage.
- System customisation and functionalities
  - Recommends modular, standards-friendly architectures to enable enhanced user interfaces and future upgrades.
  - Defines a minimal functional baseline: interactive geometry/attribute editing, image management, querying, customisable databases, import/export, georeferencing, and basic statistics.
- Co-pilot software
  - JRC’s Co-pilot provides an integrated GIS for softcopy CLC production, maintenance, and updating (MS Windows). 
  - Data managed “at continuum” across time, with object-centric data structures (points/lines/surfaces) and ASCII-driven configuration files.
  - Available to national CLC teams to support production workflows.

## Part I: Conversion of (semi-)automated classifications

- Cautions about automated conversions
  - Pixel-based classifications face variability in image quality, atmospheric effects, relief, and differences between land cover vs. land use.
  - Human interpretation remains essential to account for spatial patterns and object-level context.
- Generalisation and quality trade-offs
  - Spatial generalisation reduces data complexity but introduces location/attribute errors; quality assessment must reflect this trade-off.
  - Three broad spatial generalisation types: no contiguity, contiguity-aware, and time-varying attributes.
- Generalisation techniques
  - Reclassification, aggregation, amalgamation (attribute and spatial), smoothing, and simplification.
  - Emphasises that automated per-pixel accuracy and subsequent generalisation performance jointly determine final quality.
- Conversion quality issues
  - Distinguishes polygon (map boundaries) vs. raster (dominant class per cell) data models; pixel size should be well below the minimum mapping unit to keep boundaries intact.
  - Identifies sources of error in multispectral classification: spectral confusion, mixed pixels, system errors, and conceptual mismatches.
- Statistical properties and quality assessment
  - Land cover data are nominal/categorical; non-parametric or distribution-free methods are preferred for quality assessment.
  - Standard quality measures may not capture generalisation-induced errors; overlay and visual checks are important.

## Part I: Validation methodology

- Purpose
  - Validate the CORINE inventory without redefining its data model or data collection method.
  - Provide users with reliability information through a repeatable, random sampling approach.
- Sampling methodology
  - Stratified random sampling across strata (land cover items and/or geographic regions).
  - Random sampling informed by digital land cover maps; allocation of sampling points per stratum to minimise standard error.
- Determining the number of sampling points
  - n_h = p_h(1 - p_h) / s_h^2 (approx.), where p_h is an estimated error rate and s_h is the accepted absolute standard error for stratum h.
  - Practical considerations include maximum points per unit area (e.g., cap at 2 points per km^2) to balance precision and practicality.
- Random sampling steps
  - Step 1: area-proportional, systematic selection of land cover units within each stratum; ensures representative coverage.
  - Step 2: placement of sampling points within each unit using local random or systematic methods depending on the required number of points.
  - Methods accommodate cases with many or few points per unit; grid-based approaches used when five or more points are needed.
- Interpretation and validation
  - Interpretation performed on-screen using digital imagery; circles of 1 km radius used around sampling points to account for minimum mapping size.
  - Validation interpreters are independent and use original data sources to assess land cover at a broader area around the point.
- Verification and documentation
  - GIS checks for topology and consistency; documentation includes plots, error tables, and a confusion matrix.
  - Validation results feed into accuracy estimation for strata and aggregated levels of the nomenclature.
- The raising (accuracy estimation)
  - Construction of confusion matrices to quantify omission and commission errors.
  - Accuracies can be estimated for each stratum and aggregated across strata, with standard errors derived from binomial variances.
  - Procedures support accuracy assessments at different nomenclature levels and across regions.

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

- Purpose
  - Refines and extends class definitions to reduce confusions, without altering core content.
  - Provides clarified contents, typical patterns, texture descriptions, representative photographs, and country-specific particularities (notably Phare countries).
- Methodology
  - Builds on visual interpretation experience from Landsat and SPOT imagery.
  - Emphasises the relationship between landscape objects and their satellite-image manifestations for interpretation.
- Structure and content
  - For each class, presents refined descriptions, dominant object types, typical arrangement/patterns, representative textures, and example photos.
  - Classifications are organised by major groups: 1.x Urban fabric, 2.x Agricultural land, 3.x Forests, 4.x Wetlands, 5.x Water.
- Practical guidance for interpreters
  - Includes threshold guidelines (e.g., urban fabric density, minimum mapping sizes, dominance rules) and generalisation patterns to aid consistent mapping across countries.
  - Addresses cross-country heterogeneity and extension to phares regions with country-specific particularities.

## Practical implications for Data Stewards

- Documentation and metadata
  - Maintain clear records of production methods (hardcopy vs softcopy), software used (including Co-pilot), and data formats.
  - Document generalisation rules, threshold decisions, and validation approaches to support reproducibility and governance.
- Data quality and usability
  - Use validation results to set user expectations on accuracy; provide per-stratum and aggregated accuracy metrics with standard errors.
  - Communicate limitations of automated conversions and the continued need for expert interpretation.
- Interoperability and formats
  - Align data products with common raster/vector formats (e.g., geoTIFF, standard GIS formats) to facilitate sharing and reuse.
  - Ensure system architecture supports multi-dataset overlays, consistent legends, and metadata exchange.
- Updates and sustainability
  - Adopt the “continuum” data management approach to track changes over time; support re-updating and incremental improvements.
  - Plan for regional extensions (e.g., Central/Eastern Europe) through Part II nomenclature refinements and region-specific interpretations.

## Summary of key takeaways

- The Addendum advances CORINE through softcopy methods, semi-automated conversions, and enhanced nomenclature guidance to improve data quality, interoperability, and scalability.
- It provides a robust validation framework (stratified random sampling, confusion matrices, and accuracy estimation) to quantify reliability and guide improvements.
- The Part II nomenclature addendum offers detailed refinements for class definitions, patterns, and textures to aid consistent image interpretation and regional applicability.
- For Data Stewards, the document underscores the importance of clear governance around data production methods, metadata, validation, and communication of data quality to users.