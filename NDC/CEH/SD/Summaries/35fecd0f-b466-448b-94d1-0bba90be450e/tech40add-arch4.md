# CORINE land cover technical guide - Addendum 2000

## Overview and aims
- Addendum to the CORINE Land Cover Technical Guide (1994) to support land cover monitoring by enhancing data collection guidance.
- Introduces methodological developments for softcopy interpretation, (semi-)automated conversions, metadata/standards, and broader European extension (including Central and Eastern Europe).
- Extends the CORINE nomenclature with generalisation rules and clarifications to improve interpretation and comparability.
- Aims to improve understanding of landscape characteristics and data quality within a 1:100,000 mapping framework.

## Part I: State-of-play production methods of the CORINE land cover database

### Introduction
- Describes the shift from hardcopy inventory (photo-interpretation on printed transparencies) to softcopy, GIS-enabled workflows.
- Highlights that automated classification alone cannot fully replace human interpretation due to the CLC’s functional vs. spectral distinctions and landscape complexity.
- Notes that both analogue and digital approaches remain valid and can be combined.

### Hardcopy inventory
- Original CORINE workflow: computer-aided photo-interpretation using transparencies over 1:100,000 hardcopy satellite prints, with ancillary data.
- Emphasizes homogeneity, boundary clarity, and the need for multiple intermediate products in earlier workflows.
- Acknowledges benefits and error sources associated with manual digitisation.

### Softcopy inventory
- Advances to on-screen interpretation and digitisation, leveraging integrated GIS environments.
- Recommends GIS capabilities: multi-dataset viewing, broad raster/vector format support, and interoperability via standard formats (geoTIFF for rasters; common vector formats).
- Discusses integration of image, text, and icon data linked to geographic objects; editable attribute data; and rich metadata support.

### System customisation
- Encourages evaluating software architecture, modularity, and development kits to support custom user interfaces and new functionalities.
- Stresses openness to porting and standards compliance (e.g., ANSI/other OS standards).

### Required functionalities
- Outlines a minimal functional suite for softcopy GIS-based systems:
  - Interactive editing and display of geometry, attributes, and relations.
  - Image management, raster/vector integration, image enhancement.
  - Various query capabilities (geographic, arithmetic, Boolean).
  - Customisable database structure and geospatial indexing.
  - Import/export across formats.
  - Documentation headers and georeferencing tools.
  - Statistical analysis tools (e.g., PCA, spectral classifications).
- Highlights the need for overlaying multiple data types and legends in a single view.

### Co-pilot software
- Describes JRC’s Co-pilot as an integrated Windows-based GIS for softcopy production, maintenance, and updating of the CLC database.
- Features a continuum data model (no breaks across map versions) and an object-based data model (points, lines, surfaces) with catalogues, typelook, and ASCII-based main structures.
- Notes Co-pilot’s availability to national CLC teams.

### Conversion of (semi-)automated classifications
- Warns about limitations of automated classification due to data quality, scale, and differences between land cover vs. land use.
- Emphasises the value of hybrid approaches (automatic classification plus human interpretation) for spatial generalisation and attribute accuracy.
- Outlines that conversion quality depends on several interacting factors: feature size, output scale, user objectives, and input information.

#### Methodological aspects of a conversion
- Defines spatial generalisation as reducing data complexity at the cost of some accuracy.
- Identifies three broad types of spatial generalisation procedures (no contiguity, contiguity-aware, temporal variation).
- Summarises UK/Sweden/Finland approaches: reclassification, aggregation, amalgamation, smoothing, simplification; stresses hierarchical relabelling and the need to reflect the 44-class hierarchy.

#### Specific conversion quality issues
- Discusses data models (polygon vs raster) and their implications for quality assessment.
- Identifies four main error sources in multispectral classification: spectral confusion, mixed pixels, system errors, conceptual errors.
- Describes statistical properties of land cover data and cautions against overreliance on formal statistics due to nominal/categorical data and phase-space considerations.
- Notes limitations of generalisation quality measures and the importance of overlay/visual checks to assess map quality.

## 5. Validation methodology

### Validation purpose
- Validation evaluates CORINE Land Cover inventories for identifying and delineating CORINE units; it does not re-evaluate data collection methods themselves.
- Uses repeated data collection with random sampling to generate a confusion matrix and assess omission/commission errors.
- Enables reliability estimates at different nomenclature levels and strata.

### Sampling methodology
- Employs stratified random sampling (by land cover items and/or geographic regions).
- Details input: digital land cover map and requested sampling points per stratum.
- Phase 1: select strata and determine points per stratum; Phase 2: draw sampling points within strata, ensuring area-proportional representation.
- Output includes misclassification areas by stratum and overall accuracy estimates.

### Determination of the number of sampling points
- Provides a binomial-based formula to determine required points per stratum, incorporating expected error rate and acceptable standard error.
- Discusses practical limits (e.g., cap of 2 points per km^2) and methods to handle strata of varying sizes.
- Distinguishes several cases for point placement within land cover units and outlines robust systematic/local random sampling strategies.

### Interpretation of random sampling points
- Points are interpreted iteratively from high-level (broad) to lower-level categories, guided by ancillary data and minimum mapping size considerations.
- Emphasises on-screen interpretation with a fixed scale to preserve comparability with original data.

### Conduction and verification
- Validation is conducted with interpreters blind to exact locations to preserve objectivity.
- Uses overlays, GIS checks, and a structured verification plot to document errors and plausibility.
- Ensures consistency with original data sources and field documentation.

### The raising (estimation of accuracy)
- Builds confusion matrices to estimate correctly classified areas per stratum and overall. Includes formulas to aggregate results across strata or aggregated nomenclature levels.
- Describes variance estimation for accuracy metrics and notes that precision generally improves with stratified sampling and robust point placement.

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

### Introduction
- Provides refinements to CLC class definitions based on long-standing interpretation experience.
- Extends core class descriptions with clarifications, typical patterns, textures, representative photographs, and country-specific particularities.
- Aims to reduce confusion and improve image interpretation consistency at 1:100,000 scale.

### Methodology
- Visual interpretation framework: focuses on land-cover objects and their image manifestations.
- Emphasises interpretation elements (texture, patterns) as a basis for up-to-date class characteristics and generalisation guidance.
- Supports ongoing enhancement of class contents for European landscape types, including Phare country specifics.

### Class descriptions and generalisation themes (highlights)
- Urban fabric and related classes (e.g., 111 Continuous urban fabric; 112 Discontinuous urban fabric) with density thresholds and extension rules (e.g., 80% impermeable surface for 111; 30–80% impermeable for 112; specific handling of patches and buffers).
- Industrial, transport, and infrastructure classes (e.g., 121 Industrial or commercial units; 122 Road and rail networks; 124 Airport areas) with texture, extension rules, and exclusions.
- Agricultural classes (e.g., 211 Non-irrigated arable land; 212 Permanently irrigated land; 221 Vineyards; 231 Pastures; 242 Complex cultivation patterns) including crop-specific rules, mixed land uses, and special cases.
- Forest and semi-natural vegetation classes (e.g., 3.1 Forests; 3.2 Shrubs and/or herbaceous vegetation associations; 3.3 Open spaces with little or no vegetation; 311 Broad-leaved forests; 322 Moors and heathland; 333 Open spaces with limited vegetation) with canopy thresholds, extension criteria, and patterns for interpretation.
- Wetlands and water-related classes (e.g., 411 Inland wetlands; 412 Forested wetlands; 421 Salt marshes; 512 Inland waters) including notable generalisation rules for linking small wetlands to larger water bodies.
- Coasts and littoral classes (e.g., 521 Coastal lagoons; 523 Sea water) with guidance on estuarine shapes and coastal morphology.
- Other natural and semi-natural categories (e.g., 331 Sea beaches; 332 Lapis and rocky areas; 324 Forest degradation; 335 Glaciers and perpetual snow) with patterns, textures, and exclusions.

### Generalisation and country particularities
- Provides patterns, textures, representative imagery, and country-specific notes to standardise cross-country interpretation.
- Includes a framework for applying generalisation rules across landscape types while preserving essential land cover semantics.

## References and resources
- CEC (1994) CORINE Land Cover Technical Guide.
- Additional methodological references and national contributions documenting validation, quality management, and image interpretation techniques.