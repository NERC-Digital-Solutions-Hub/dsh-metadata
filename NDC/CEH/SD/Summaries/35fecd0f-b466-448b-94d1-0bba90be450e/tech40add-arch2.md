# CORINE land cover technical guide - Addendum 2000

## Executive summary
- Provides enhancements for producing and updating CORINE Land Cover (CLC) data, including new methodologies, tools, and nomenclature refinements.
- Emphasizes softcopy (on-screen) interpretation, semi-automated classification conversions, and better data transparency for Central/Eastern Europe.
- Introduces GIS-based workflows, Co-pilot software, and standardized validation, sampling, and generalisation procedures to improve consistency over time.
- Extends the CLC nomenclature with detailed class descriptions, interpretation patterns, representative visuals, and country-specific particularities to support accurate image analysis at 1:100,000 scale.

## Part I: State-of-play production methods of the CORINE land cover database

- Introduction and purpose
  - Addendum to the 1994 CORINE Land Cover Technical Guide; aims to provide additional information, methodological developments, and extended class descriptions.
  - Supports data collection, updating, and interpretation, with a focus on softcopy tools, data accessibility, and landscape interpretation.

- Hardcopy inventory
  - Traditional method: computer-aided photo-interpretation using transparencies over 1/100,000 hardcopy satellite prints, with ancillary data.
  - Strengths: proven, with manageable workflow.
  - Limitations: prone to digitisation errors, border-matching issues, and multiple intermediate products.

- Softcopy inventory
  - Shift to computer-based interpretation and digitisation; use of on-screen data in integrated GIS environments.
  - GIS considerations: multi-dataset management, raster/vector interoperability (e.g., geoTIFF, BSQ/BIL/BIP formats), and flexible visualization.
  - System components include text/images/icons linked to objects, editable attributes, and robust metadata.

- System customization and functionalities
  - Emphasis on modular, extensible software architectures; support for user interfaces, development kits, and standards (where possible).
  - Core functionalities required: interactive editing of geometry/attributes/relations, image management, diverse query capabilities, configurable database structures, import/export, georeferencing, and statistical tools.
  - Co-pilot software (JRC): an integrated MS Windows GIS environment for continuous data management across time; uses geographic objects (points/lines/surfaces) with catalogues, typelook, and ASCII-stored structures.

- Conversion of (semi-)automated classifications
  - Acknowledges limits of automated classification due to data quality, ground truth variability, and the difference between pixel-based and holistic human interpretation.
  - Conversion approaches (generalisation) include:
    - Reclassification: regroup into CORINE classes (often hierarchical relabelling).
    - Aggregation: merge proximate small features.
    - Amalgamation: join or divide contiguous features with consideration of semantic class proximity.
    - Smoothing: boundary adjustment to reduce raster stepping effects.
    - Simplification: reduce boundary complexity.
  - Conversion quality is influenced by per-pixel accuracy, generalisation efficiency, human interpretation accuracy, and the intended output scale.

- Specific conversion quality issues
  - Two data models: polygon (homogeneous value areas) vs raster (dominant class per cell).
  - Errors originate from spectral class confusion, mixed pixels, system errors, and conceptual misalignment with class definitions.
  - Phase-space/statistical considerations for discrete, nominal classes; generalisation adds error in exchange for simplicity and legibility.
  - Important to consider scale change and that quality measures often understate generalisation-induced errors.

- Validation methodology
  - Validation uses random sampling to re-interpret national areas with the same data sources, producing confusion matrices to assess omission/commission errors.
  - Enables reliability flags for individual items and aggregated levels of nomenclature.
  - Supports stratification (by nomenclature level or geography) to manage uncertainty.

- Sampling methodology (5.1)
  - Stratified random sampling; determination of sampling points per stratum to minimise total standard error.
  - Points proportional to area; density limits (e.g., max ~2 points per km²) to balance practicality and precision.
  - Phases: select strata and point counts; draw sampling points within strata/units; ensure area-proportionate, distributed placement.

- Determination of the number of sampling points (5.2)
  - n_h = p_h(1 - p_h) / σ_h^2; sample size depends on estimated error rate p_h and desired standard error σ_h.
  - Higher error rates demand more points; a 50% initial guess yields the most points; standard error guides refinement.
  - Practical limits per stratum considered to balance feasibility.

- Random sampling steps (5.3)
  - Step 1: area-proportional selection of land cover units using a step-size and a random start; ensures proportional representation across units.
  - Step 2: location of points within each unit via local random/systematic sampling tailored to unit size and point count.
  - Methods account for single, multiple, or grid-based point placement depending on n.

- Interpretation of random sampling points (5.4)
  - Interpretations follow the CORINE methodology from exterior to interior, ensuring minimum mapping size considerations.
  - Validation on-screen at scales not exceeding 1:40,000; virtual interpretation (no field surveys during validation) with strong metadata and documentation.
  - Validation points interpreted with access to original data sources; roving circle interpretation (eccentric 1 km radius) to emulate standard practice.

- Conducting and verification of validation (5.4.1–5.4.2)
  - GIS checks for topology and consistency; documentation plots and error logging; final verification by a separate interpreter.
  - Validation outputs include a confusion matrix, and area-based accuracy estimates per stratum and per aggregated levels.
  - Standard errors computed for accuracy estimates; aggregation across strata weighted by area.

- The raising (5.5)
  - Overlay validated data with random points; produce confusion matrices and estimate correctly classified area by stratum.
  - Overall accuracy estimation combines stratum-level results weighted by area; presentation of standard errors and variance formulas.
  - Stratification can be aligned with nomenclature levels or geographic regions; results can be aggregated to higher levels.

- References (6)
  - Foundational sources and related methodological guidance (CEC 1994; DIN; Douglas & Peucker; etc.).

## Part II: Addendum to the CORINE land cover nomenclature illustrated guide

- Introduction
  - Based on extensive experience interpreting Landsat and SPOT imagery; refines and clarifies class definitions without changing core content.
  - Adds detail to help interpreters distinguish classes, with patterns, textures, representative photos, and country-specific particularities.
  - Aims to support consistent interpretation across Europe at 1:100,000 scale.

- Methodology for compilation
  - Visual interpretation continues to be central; emphasis on land cover objects and their satellite-image manifestations.
  - Adds interpretation elements (texture, pattern, representative imagery) to class descriptions.
  - Country-specific particularities and generalised mapping guidance are included.

- Class-level clarifications and generalisation rules
  - Urban fabric (Class 1.x)
    - Density thresholds and extension rules (e.g., 111 Continuous urban fabric: >80% impermeable surfaces; 112 Discontinuous urban fabric: impermeable surfaces 30–80%; 100 m buffers; 25 ha thresholds; housing estates patterns).
    - Particularities and generalisation guidance for urban expansion and irregular patterns.
  - Industrial, commercial and transport units (Class 121; Subclasses 122, 123, 124)
    - Differentiation by built-up area, road/port infrastructure, and accessory lands; generalisation rules for combining or splitting units.
  - Agricultural and horticultural classes (2.x, e.g., 211, 212, 213, 221, 222, 231, 232, 233, 242–244)
    - Definitions for arable land, irrigated land, rice fields, vineyards, fruit trees, pastures, complex cultivation patterns, agroforestry, and related patterns.
    - Notes on thresholds and dominance when multiple crops share parcels; detailed texture cues.
  - Forests and natural vegetation (3.x)
    - 31x (forests) and 32x–33x subtypes (broad-leaved, coniferous, mixed; shrub/grass associations; open spaces).
    - Crown cover thresholds (e.g., 30%), density rules, and patterns for distinguishing forest types, scrub, grassland, and bare rock.
  - Wetlands and water-related classes (4.x, 5.x)
    - Inland wetlands (4.1) and coastal wetlands (4.2) with vegetation regimes and hydrological context.
    - Inland waters (5.1) and marine waters (5.2) with guidance on water bodies, estuaries, lagoons, and coastal morphology.
  - Other notes
    - Extensions and exclusions for specific transitions (e.g., dunes, salt marshes, saline surfaces, mining and waste sites).
    - Guidance on special cases, such as reticulated patterns, dune vegetation zoning, and habitat-specific textures.

- Practical outputs for analysts
  - Enhanced, illustrated definitions and patterns to improve image interpretation consistency.
  - Structured, rule-based guidance to support cross-country comparability and update processes.
  - Clear generalisation rules to help map across scales and update cycles without losing core classification integrity.

## Implications for Analysts Monitoring the Environment
- Standardization and reproducibility
  - The addendum provides a consistent framework for data collection, interpretation, and validation across Europe, enabling time-series analysis and policy assessment.
- Data quality and transparency
  - Emphasizes documented workflows, provenance, and validation metrics (confusion matrices, standard errors) to quantify reliability.
- Tooling and data management
  - Encourages use of softcopy GIS environments (Co-pilot and similar tools) and standardized data formats to enhance accessibility and reuse.
- Nomenclature clarity and comparability
  - Refined class definitions and patterns reduce misclassification risk and support cross-national comparability at the CORINE scale.
- Practical constraints and caveats
  - Acknowledges limitations of automated classifications and the need for human interpretation, especially during generalisation and edge cases.
  - Highlights the importance of scale, data quality, and context in conversion and validation processes.