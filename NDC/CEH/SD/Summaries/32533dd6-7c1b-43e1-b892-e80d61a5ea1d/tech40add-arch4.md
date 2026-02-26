# CORINE land cover technical guide - Addendum 2000

- Purpose of the addendum
  - Provide additional information not in the 1994 CORINE Land Cover (CLC) Technical Guide.
  - Describe new methodological developments, especially softcopy (on-screen) interpretation and (semi-) automated classification conversions.
  - Extend the CLC nomenclature and interpretations to Central/Eastern Europe and provide generalisation rules for mapping at 1:100 000.
  - Improve understanding of landscape characteristics and class descriptions.

## Part I: State-of-play and production methods

- Introduction
  - Shift from hardcopy to softcopy data production due to digital technologies; automated classification is possible but human interpretation remains essential because CLC classes are partly functional/structural and not fully automatable.
- Hardcopy inventory
  - Original approach: computer-aided photo-interpretation on 1:100 000 satellite image transparencies with ancillary data; data were digitised after manual interpretation.
  - Pros/cons: robust for its time but prone to digitisation errors, border-matching issues, and dependence on physical transparencies.
- Softcopy inventory
  - Advances: interpretation and digitisation done in a single on-screen pass using GIS; supports integration of multiple data types and continuous data updates.
- GIS and data management
  - Integrated GIS environments are essential for handling raster and vector data, multiple data sets, and diverse formats (e.g., geoTIFF for rasters; Arc/Info formats for vectors).
- Text, images, and icons
  - Geographic objects can have alphanumeric attributes, images, icons, and non-georeferenced documentation linked to them; editable text is supported.
- System customisation
  - Emphasis on modular software architecture, user interfaces, and porting to different OS environments; aim for standards-compatible design.
- Required functionalities (minimal system requirements)
  - Basic: editing and displaying geometry, attributes, and relations.
  - Image tools: raster/vector display, image enhancement, import/export.
  - Queries: geographic, arithmetic, Boolean; support for geometry and topologic relations.
  - Database management: customizable structure and geographic indexing.
  - Import/export: exchange with other platforms/formats.
  - Georeferencing and metadata: coordinate transforms, GCP-based references.
  - Statistical tools: quantitative analysis and potential for principal components/spectral classifications.
- Co-pilot software
  - JRC’s Co-pilot: an integrated MS Windows GIS for softcopy production, maintenance, and updates; data are managed in a continuum across maps and time; objects are the basic units (points/lines/surfaces) with Catalogue (types), Typelook (display), and GraphicSet (graphics); distributed by JRC to national CLC teams.

## Part I: Conversion of (semi-)automated classifications

- Key caveats
  - Automated per-pixel classifications are limited by varying image quality, the difference between land cover (CLC concepts) and land use, and the need for human interpretation to form coherent CLC classes.
  - Conversion rules depend on data input, objectives, operator decisions, and output scale/format.
- Methodological aspects of conversion
  - Spatial generalisation reduces data complexity but increases some errors; balance between simplicity and accuracy is required.
  - Three types of spatial generalisation procedures:
    - Non-contiguity-based (ignore contiguity)
    - Contiguity-based (consider surrounding area)
    - Time-varying attributes
  - Common user-controlled approaches:
    - Reclassification (hierarchical relabelling to match 44-class hierarchy)
    - Aggregation (merging nearby features)
    - Amalgamation (joining or dividing contiguous features with semantic or spatial rules)
    - Smoothing (boundary adjustments to reduce raster-step effects)
    - Simplification (reducing boundary detail)
- Specific conversion quality issues
  - Land cover is a categorical variable; data models include polygon (vector) and raster (grid of cells).
  - Pixel size vs minimum mapping unit: when sufficiently small, pixel-based errors near boundaries may be negligible.
  - Main error sources in multispectral classifications: spectral confusion, mixed pixels, system errors, conceptual (class coherence) errors.
- Statistical properties and generalisation
  - Phase-space conceptualization helps relate classification accuracy to derived measures; many traditional statistics are not suitable due to nominal scales and spatial dependence.
  - Generalisation quality is not fully captured by standard quality measures; must consider scale change and the trade-off between accuracy and simplicity.

## Part I: Validation methodology

- Purpose
  - Validate CORINE inventories to convey reliability to data users; not to reassess the data collection method itself.
- Approach
  - Re-collect data using random sampling with the same sources; interpret selected areas again and compare to original results to build a confusion matrix.
  - Use weighted sums to derive overall accuracy and accuracy at different nomenclature levels; stratified sampling enables region- or class-based insight.
- Sampling methodology (5.1)
  - Stratified random sampling: strata can be land cover items or geographical regions; determine number of points per stratum; aim for area-proportionate sampling to minimize errors.
- Determining the number of sampling points (5.2)
  - Use a binomial-based formula to estimate the required number of points per stratum based on expected error rate and desired standard error; practical cap suggested (e.g., no more than 2 points per km² in small strata).
- Random sampling steps (5.3)
  - Step 1: select land cover units proportionally by area; allocate sampling points per unit.
  - Step 2: place sampling points within units using systematic and local random sampling; several cases depending on number of points per unit.
- Interpretation of random sampling points (5.4)
  - Interpretation is done on-screen within a fixed scale (not exceeding 1/40,000); delineation proceeds from larger units to finer categories; validation uses a circular area (1 km radius) around each point to assess context; interpreter blinded to point location to avoid bias.
- Conduction and verification (5.4.1, 5.4.2)
  - Validation maps are checked for topology; documentation and a summary table accompany results.
- The raising (5.5)
  - Overlay validated data with random points to build a confusion matrix; estimate correctly classified area per stratum and overall area; compute standard errors; aggregation across strata weighted by area.
  - Formulas provided for calculating estimated accuracy and its variance.

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

- Introduction and purpose
  - Over a decade of experience showed the need to refine class definitions without changing core content; provide clarifications, contents, typical patterns, representative photos, and country-specific particulars to support image interpretation and harmonization.
- Methodology
  - Visual interpretation remains core; addendum focuses on interpretation elements, landscape objects, and the relation between landscape objects and their image manifestations.
- Characteristics of CORINE land cover classes
  - Provides refined class descriptions, patterns, textures, representative photographs, and country-specific particularities to facilitate consistent image analysis at 1:100 000 scale.
  - Includes guidance on general patterns and the typical texture of classes; introduces thresholds and decision rules for classifying complex patterns (e.g., urban fabrics, agricultural mosaics, forests, wetlands, water bodies).
- Example class emphases (illustrative, not exhaustive)
  - Urban fabric and related classes (1.1–1.4, 111–112) with density thresholds (e.g., 80% impermeable surfaces for continuous urban fabric; 30% urban fabric within a patchwork for discontinuous fabric; grouping rules for small patches to meet area thresholds).
  - Agricultural classes (2.x) and forest classes (3.x), including patterns, textures, and specific peculiarities (e.g., alpine meadows, moors, dunes, and various vegetation associations).
  - Wetlands and water bodies (4.x and 5.x) with definitions and generalisation guidance for connecting or separating adjacent water features.
- General guidance
  - A large portion of Part II provides patterns, textures, and representative photographs to improve interpretation accuracy and consistency across countries and Phare/Phare-adjacent contexts.

## References and sources

- The addendum cites the original CORINE Land Cover Technical Guide (CEC, 1994) and subsequent methodological and quality-management references, along with country-level contributions and improvements.

- Overall, the document describes the evolution from hardcopy to softcopy data production, the integration of GIS and Co-pilot tooling, the careful balance between automated classification and expert interpretation, robust validation via stratified random sampling, and detailed refinements to the CORINE nomenclature to support consistent interpretation across Europe, including Central and Eastern Europe.