# CORINE land cover technical guide - Addendum 2000

- Purpose and scope
  - Addendum to the CORINE Land Cover Technical Guide (1994) to support ongoing land cover monitoring and updates.
  - Introduces new methodological developments: soft copy interpretation, (semi-) automated conversions, enhanced nomenclature descriptions, and generalisation rules for 1:100,000 mapping.
  - Extends guidance to Central and Eastern Europe and improves understanding of landscape contents and class characteristics.
  - Outlines data collection, processing, and governance practices to improve data quality and openness.

## Part I: State-of-play production methods of the CORINE land cover database

- Hardcopy inventory
  - Computer-aided photo-interpretation using overlaid transparencies on 1:100,000 hardcopy satellite prints.
  - Ancillary data used to confirm content; emphasis on homogeneous zones, identifiable boundaries, and sufficient scale for interpretation.
  - Marrying analogue methods with digital tools; recognition of limitations such as border matching and potential digitisation errors.

- Softcopy inventory
  - Transition to softcopy interpretation and digitisation; on-screen work with image data and GIS tools.
  - GIS integration (3.1)
    - Requires GIS capable of handling multiple datasets, raster and vector data, and various raster/vector formats (e.g., BSQ, BIL, BIP, TIFF, geoTIFF; Arc/Info exchanges; DXF).
    - Push toward common geospatial exchange standards to facilitate data sharing.
  - Text, images and icon information (3.2)
    - Linking alphanumeric attributes, images, and icons to geographic objects; editable text for object documentation.
  - System customization (3.3)
    - Evaluation of software architecture, modularity, and extendibility; emphasis on standards-friendly design for future porting.
  - Required functionalities (3.4)
    - Core needs include interactive display/edit of geometry/attributes/relations, image management, various query types, a customizable database, import/export, documentation headers, georeferencing, and statistical tools.
  - Co-pilot software (3.5)
    - JRC’s integrated Windows-based GIS for softcopy CORINE Land Cover production; continuum data management across time; ASCII-based data structures; available to national teams.

- Conversion of (semi-)automated classifications
  - Caution about limitations of automated classifications due to image quality, land cover vs. land use, and the need for human interpretation to reflect CORINE’s structure.
  - Methodological aspects (4.1)
    - Spatial generalisation reduces data complexity but adds errors; involves reclassification, aggregation, amalgamation, smoothing, and simplification.
  - Specific conversion quality issues (4.2)
    - Data models: polygon vs raster; importance of pixel size being small relative to minimum mapping unit.
    - Sources of error in multispectral classification: spectral confusion, mixed pixels, system errors, and conceptual misalignments.
  - Statistical properties (4.2.1)
    - Phase-space modelling for understanding how taxonomic definitions relate to mapped outputs; recommends non-parametric approaches due to nominal, discrete classes.
  - Generalisation properties (4.2.2)
    - Generalisation adds error for simplicity; typical procedures include reclassification, aggregation, amalgamation, smoothing, and simplification; performance hinges on per-pixel classification quality.

- Validation methodology (5)
  - Validation repeats original data collection using random sampling; builds a confusion matrix to quantify omissions and commissions.
  - Outputs include reliability information at various nomenclature levels; enables stratified analysis by region or class level.

- Sampling methodology (5.1)
  - Stratified random sampling: strata by land cover items or geographical regions; area-proportional selection of sampling points.
  - Aims to minimize standard error; determines sampling density per stratum, with practical caps (e.g., 2 points per km²).

- Determination of the number of sampling points (5.2)
  - Uses a binomial-based formula to compute points per stratum based on estimated error rate and desired standard error.
  - Practical considerations for small strata and high point density.

- Random sampling steps (5.3)
  - Step 1: area-proportional selection of land cover units within a stratum.
  - Step 2: distribution of sampling points within units using pure random, systematic, or grid-based approaches depending on the number of points.

- Interpretation of sampling points (5.4)
  - Identification at multiple levels, from broad classes to finer levels; interpretation often conducted on-screen with access to original data sources.
  - Validation emphasizes adherence to minimum mapping size and off-center interpretation to maintain methodological integrity.

- Conduct and verification of validation (5.4.1, 5.4.2)
  - Validation maps checked for topology; meta-data and field documentation are important for reproducibility.
  - Results documented in plots and tables; final validation supports a confusion matrix and accuracy assessments.

- The raising (5.5)
  - Overlay validated data with random points to construct confusion matrices and estimate correctly classified area per stratum.
  - Aggregation across strata yields overall accuracy; standard errors are computed via binomial variance formulas.

- References (6)
  - Key sources include CORINE Technical Guide (1994), standard quality management and statistics references, and related methodological papers.

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

- Introduction (Part II, 1)
  - Experience from >10 years of CORINE interpretation led to refinements of definitions to reduce confusions without altering core class content.
  - Adds clarifications to class definitions, contents, typical patterns, textures, representative photos, and country-specific particularities (Phare countries).

- Methodology (Part II, 2)
  - Visual interpretation remains central; enhancement focuses on interpretation elements and relationships between landscape objects and their image manifestations.
  - Presents a graphic and textual presentation of class characteristics at 1:100,000 scale, including texture and pattern concepts to aid interpreters.

- Content (Part II, Part II, 3)
  - Detailed refinement and extension for numerous classes (e.g., 1.1 Urban fabric through 5.1 Inland waters; 3.1 Forests through 3.3 Open spaces with little or no vegetation; 4.1 Inland wetlands; 5.1 Inland waters, etc.).
  - For each class, provides:
    - Refined definitions and extension/dispersion notes.
    - Characteristics of typical contents (dominating objects, textures, patterns).
    - Generalisation rules and representative photographs.
    - Specific particularities and exclusions to guide consistent mapping across countries.
  - Extensive examples and patterns (figures) illustrate density, texture, and arrangement for accurate classification.

- Specifications and particularities
  - Includes explicit thresholds and extensions for distinguishing urban fabric density (e.g., continuous vs discontinuous).
  - Provides guidance for handling mixed land uses, complex cultivation patterns, and cross-cutting features (e.g., roads, ports, rail networks, water bodies).
  - Addresses regional special cases (Phare countries) and illustrative patterns for multiple classes (urban, agricultural, forest, wetlands, waters, etc.).

- References (Part II, 4)
  - Citations to supporting sources and prior CORINE documents, including European and national contributions.

Note: The document is rich in class-level detail, generalisation rules, and illustrative guidance intended to standardize interpretation across member states and Phare countries, while supporting consistent monitoring and policy-relevant reporting.