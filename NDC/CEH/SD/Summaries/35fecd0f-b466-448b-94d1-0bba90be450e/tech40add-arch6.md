# CORINE land cover technical guide - Addendum 2000

## Aim and scope
- Provides additional information to collect and update CORINE Land Cover (CLC) data.
- Describes methodological developments, especially softcopy interpretation and (semi-) automated conversions toward CLC nomenclature.
- Extends and clarifies the CLC nomenclature, including Central/Eastern Europe extension and generalisation rules for mapping at 1:100 000.
- Improves understanding of landscape characteristics and guides data users on outputs and usage.

## Part I: State-of-play production methods of the CORINE land cover database

### Introduction
- Transition from hardcopy inventory (initial method) to softcopy/digital workflows enabled by computer technologies.
- Recognition that automated classifications alone cannot fully replace expert interpretation due to CLC’s qualitative, spatially structured classes.

### Hardcopy inventory
- Original method: computer-assisted photo-interpretation using transparencies over 1:100,000 hardcopy satellite prints with ancillary data.
- Emphasis on interpreting homogeneous zones, scale significance, and clear boundaries; digital evaluation used mainly for geometry and content checks.

### Softcopy inventory
- Interpretation and digitisation occur in a single pass using softcopy tools and integrated GIS.
- Emphasises human interpretation to complement pixel-based classifications; supports on-screen viewing of multiple data types.

### GIS and data integration (3.1–3.5)
- GIS-enabled environments manage raster and vector data in parallel windows with flexible data-type support.
- System needs: multiple data type support, robust import/export formats (raster: BSQ, BIL, BIP, TIFF, geoTIFF; vector: DXF, Arc/Info formats), and interoperability.
- Text, images, and icons can be linked to geographic objects; editable attributes and topologies are supported.
- System customisation options at various levels (UI, simple scripting, or advanced programming) with attention to standards for portability.
- Co-pilot software (JRC) provides an integrated MS-Windows GIS for softcopy production, maintenance, and updating of the CLC database; supports continuum data management and ASCII-based data structures.

### Conversion of (semi-) automated classifications
- Cautions about limits of automated classification due to image quality, mixed pixels, and the distinction between land cover and land use.
- Automated conversions can be valuable for positional accuracy and generalisation, but human interpretation remains essential.
- Generalisation approaches include reclassification, aggregation, amalgamation, smoothing, and simplification to manage complexity and achieve legibility.
- Spatial generalisation involves trade-offs: accuracy degrades as simplicity increases; methods must be chosen with clear objectives and scale considerations.

#### 4.1 Methodological aspects of a conversion
- Three main spatial generalisation types:
  - No contiguity considered
  - Contiguity considered (contextual influence)
  - Time-varying attributes
- Common UK/Swedish/Finnish approaches summarized into steps: reclassification, aggregation, amalgamation, smoothing, simplification.
- Quality outcomes depend on per-pixel accuracy, generalisation efficiency, manual interpretation, and the target scale.

#### 4.2 Specific conversion quality issues
- Land cover is a nominal, categorical variable; two data models are used: polygon (map-based) and raster (cell-based).
- Errors stem from spectral confusion, mixed pixels, system errors, and conceptual misalignment between land cover classes and imagery.
- phase-space model aids in understanding how taxonomic definitions relate to mapped outcomes.
- Generalisation quality assessment is challenging; relies on overlay comparisons and visual checks, with increased error due to scale reduction.

### Validation methodology
- Validation repeats data collection using the same sources, via random sampling, to build confusion matrices and assess omissions/commissions.
- Allows stratification by nomenclature level or geographic region; results yield validated area shares and per-stratum accuracy.

#### 5.1 Sampling methodology
- Stratified random sampling identifies land cover items and locations; aims for area-proportional representation.
- Points are allocated per stratum to minimize total sampling error; sample sizes adapt to stratum variation; practical limits (e.g., max 2 points per km²) may apply.

#### 5.2 Determination of the number of sampling points
- Number of points nh per stratum is derived from a binomial-based formula involving expected error ph and accepted standard error sh.
- Higher expected error or larger strata require more points; density adjustments consider practicality for small strata.

#### 5.3 Random sampling steps
- Step 1: area-proportional selection of land cover units within stratum, determining how many points per unit.
- Step 2: placement of points within units using pure random, systematic, or grid-based methods to ensure even spatial distribution.

#### 5.4 Interpretation of random sampling points
- Interpretation proceeds top-down on nomenclature levels; validation uses larger areas around sampling points (eccentric circle ~1 km radius) to reflect intended mapping scale.
- On-screen interpretation at a fixed scale (not exceeding 1:40,000) supports consistency with original data collection.

#### 5.4.1 Validation conduction
- Validation overlays, geometry checks, and documentation of errors on plots; meta-data and field survey histories aid the interpreter.

#### 5.4.2 Verification of interpretation results
- Topology checks and documentation ensure plausibility; key-codes are verified against originals.

#### 5.5 The raising
- Post-validation overlay with sampling points yields confusion matrices and estimates of correctly classified area per stratum and per nomenclature level.
- Accuracy estimates are area-weighted across strata; standard errors are computed per stratum and aggregated.

### References
- Core references include CEC (1994) CORINE Land Cover Technical Guide and related methodological/quality management literature.

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

### Introduction
- Reflects long-standing experience with Landsat/SPOT interpretation to refine definitions without altering core content.
- Provides enhanced definitions, inclusion/exclusion criteria, typical patterns, textures, representative photos, and country-specific particularities to assist image interpretation and cross-country consistency.

### Methodology for the addendum
- Emphasises the land cover–image interpretation relationship; focuses on interpretation elements and landscape objects that drive spectral reflection and emission.
- Delivers class-specific clarifications, patterns, textures, and typical exemplars at 1:100 000 scale to aid interpreters, with input from ETC/LC and Phare LC.

### Characteristics of the CORINE land cover classes
- Includes detailed, image-based refinements for Class 1.x (Urban fabric and related) through Class 5.x (Inland/marine waters, etc.), with:
  - Clarified definitions and class content
  - Dominant objects and typical arrangement/patterns
  - Representative textures and photographs
  - Generalisation rules and particularities
  - Extension notes and exclusions
- Provides measurement-based and heuristic generalisation guidance (e.g., urban fabric density thresholds, 80% impermeable surface criterion for continuous urban fabric, 25 ha minimum mapping sizes, etc.).
- Numerous class-specific notes address complex cases such as:
  - 111 Continuous urban fabric vs 112 Discontinuous urban fabric
  - 121 Industrial/commercial units and their relation to urban fabric
  - 122 Road and rail networks and associated land
  - 2.x Agricultural classes (arable land, permanent crops, pastures, complex cultivation patterns)
  - 3.x Forests (various forest types, texture descriptions, crown cover thresholds, and delineation rules)
  - 4.x Inland/coastal wetlands and 5.x Inland/marine waters
- Includes guidance on generalisation patterns, texture descriptions, and representative geographic examples (with figures) to support consistent classification across countries.

## Key data-support implications
- The addendum formalises methods and rules to improve data comparability and repeatability across Europe, including Central and Eastern Europe.
- Emphasises the balance between automated processing and expert interpretation to preserve semantic richness of land cover classes.
- Provides concrete guidance for data producers on:
  - How to evolve from hardcopy to softcopy workflows
  - How to implement validation and accuracy assessment using stratified random sampling
  - How to apply generalisation rules while preserving cartographic usefulness
  - How to handle class-specific edge cases and country particularities for harmonised mapping at 1:100 000

## Practical takeaway for Data Support archetype
- Use softcopy GIS workflows with integrated interpretation to improve efficiency and reduce digitisation errors.
- Apply stratified random validation to quantify accuracy and communicate reliability to end users.
- Leverage Part II refinements to ensure consistent class definitions, patterns, and textures across national datasets.
- Be aware of inherent trade-offs in generalisation: increased simplicity may degrade per-pixel accuracy; validation should account for these effects.
- Consider the Co-pilot framework or equivalent integrated tools to manage temporally consistent CORINE datasets across multiple map editions.