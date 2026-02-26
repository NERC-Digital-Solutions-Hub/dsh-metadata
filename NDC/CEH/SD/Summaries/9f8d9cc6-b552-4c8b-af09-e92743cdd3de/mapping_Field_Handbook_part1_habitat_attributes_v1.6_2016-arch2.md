# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 1: Habitat attributes

- Purpose and use
  - Standardizes data to demonstrate environmental condition and policy performance over time.
  - Produces auditable time-series outputs (maps, reports, charts) for monitoring environmental health.
  - Supports organisations with fixed monitoring responsibilities through consistent methodologies and outputs.

- Users
  - Field surveyors and analysts mapping habitat attributes in 1 km squares.
  - Personnel verifying, quality assuring, cleaning, transforming, storing, and uploading datasets.
  - Stakeholders needing comparable, repeatable biodiversity and habitat surveillance data.

- Data structure and classification
  - Editable polygon/habitat layer with Broad Habitats (BH) and Priority Habitats (PH) allocated at polygon level; detailed attributes at component level.
  - Keys driving classification:
    - Vegetation Key: assigns patches to BHs/PHs based on plant composition.
    - Woodland Types/Features Key: distinguishes woodland units by canopy structure and management status.
  - PHs nest within BHs; polygons may be BH and PH simultaneously.
  - Reporting aligned with BH/PH to ensure compatibility with Countryside Survey time-series analyses.
  - GIS masks constrain PH extents to national ranges.

- Habitat categories and granularity
  - BHs: broad landscape types including woodland, boundaries/linear features, arable lands, various grasslands, wetlands, rivers/standing waters, montane/rock, urban, coastal zones, etc.
  - PHs: specific habitats (e.g., Blanket Bog, Reedbeds, Fen/Marsh/Swamp, Saltmarsh, Limestone Pavement, montane forms) with diagnostic species and GIS masks.
  - Distinguish upland vs. lowland using GIS masks and floristic criteria.

- Field mapping workflow and practices
  - Mapping priorities: complete habitat area map, record primary attributes, capture 2–4 key species per parcel, map woody lines/features, fences, water features.
  - Editing at 1:5000 scale or finer; emphasize extent/position accuracy over exact polygon boundaries.
  - MMU (minimum mappable unit) is 0.04 ha; smaller features are generally not mapped unless part of a larger polygon.
  - Change mapping (CS 2016): adjust attributes/shapes to reflect real or error changes; emphasize attribute-level changes when needed.

- Classification keys and woodland attributes
  - Vegetation Key: dominant plant composition; informs BH/PH allocation and decisions on woodland vs herbaceous vegetation; includes canopy thresholds and GIS masking for habitat complexes.
  - Woodland Types/Features Key: records canopy structure, natural vs managed characteristics, DBH, species composition, and woody features (belts, hedges, margins, etc.).
  - Forestry themes and management indicators: detailed fields for woodland type, DBH, veteran trees, margins, buffers, and indicators (disease, regrowth, fencing, signs).

- Specific habitat guidance
  - BHs 2–19, 21–22, 27–28 cover a broad suite of habitats (woodland, boundaries, arable, grasslands, moorlands, wetlands, rivers/streams, water bodies, urban/coastal features).
  - PHs provide more detailed, regionally important habitats with corresponding diagnostic criteria and GIS masking.

- Ponds and water bodies
  - All ponds within a square must be identified; one pond per square selected for detailed condition survey.
  - Pond definition: standing water 25 m² to 2 ha, water at least four months per year.
  - Ditches, dammed streams, and flushes distinguished; boundary delineation may rely on vegetation or water marks.
  - Data collection uses two forms: grid square inventory for ponds and square inventory; pond sampling coordinated with freshwater survey teams.

- Non-native species and tree diseases
  - Recording of select invasive species to capture distribution within habitats.
  - Monitoring tree diseases (e.g., Chalara/Ash dieback, Dutch Elm disease) within woodland features; dedicated fields and appendices provide guidance.

- Historic Environment Assets (HEA)
  - Two classes: Scheduled Ancient Monuments (SAMs) and Historic Environment Features (HEFs).
  - Field forms, unique SAM/PRN identifiers, and polygon-based HEA mapping; photography and threat assessment included.

- Data management and access
  - GIS-based storage with uploads to appropriate portals.
  - Emphasis on reproducibility, data quality, and accessibility of underlying data for secondary analyses and policy evaluation.

- Quality assurance, change control, and mosaics
  - Change mapping distinguishes genuine habitat changes from mapping errors.
  - Mosaic mapping allowed when delineation is difficult; each component requires defined percent cover and attributes.

- Field practicality and analyst guidance
  - Time planning: allocate 2–4 days per square; map areas, lines, and points concurrently.
  - Do not rely solely on GPS for boundaries; map extents first, then refine.
  - Capture two characteristic species per habitat parcel (up to four) and document key woody features.
  - Record buffer zones for protected features and note condition indicators for future monitoring.

- Reporting and outputs
  - Standardized habitat maps, BH/PH allocations, and detailed attribute records suitable for longitudinal and policy analyses.
  - Framework supports integration with surveys like Countryside Survey for historical trend analyses and cross-survey comparability.

- Additional notes for analysts
  - Be mindful of GIS mask constraints for PH extents and correct BH/PH allocations at polygon level.
  - Use Vegetation and Woodland Keys to ensure consistent data capture across surveyors and years.
  - Document failures, changes, and data quality issues with prescribed forms to support transparency and reproducibility.

- Visit status (data capture and workflow)
  - All features have a VISIT STATUS: 0 unsurveyed, 1 IN PROGRESS, 2 COMPLETED, 3 REFUSED ACCESS.
  - IN PROGRESS acts as a reminder to complete species assignments or attributes where partial mapping exists.
  - COMPLETED used only when a feature is fully surveyed; REFUSED ACCESS indicates no data for that feature.
  - Methods to identify and manage status:
    - Use layer-specific searches (Landscape Points, Landscape Events, Landscape Areas) and field VISIT STATUS.
    - FIND command for quick listing by status; SELECT BY ATTRIBUTE for multi-criteria highlighting; ATTRIBUTE TABLE for managed selections.
    - Options support multiple criteria and can be saved for reuse; inversion can reveal unsurveyed or in-progress features.
  - Linears are initially unsurveyed; statuses update as mapping progresses.

- Minimum mapping units and editing tactics
  - MMU constraints may necessitate combining or updating polygons rather than splitting a small corner.
  - UPDATE tool sequences: merge, split, and re-enter attributes as needed without creating unattainable MMU-sized polygons.
  - Copy+ and other selection tools enable iterative editing across layers to refine polygons.

- Ancient (veteran) trees
  - Identification hinges on appearance of age and a set of indicators beyond size alone.
  - Girth/diameter measurements provide species-specific thresholds; other features include dead wood, hollows, cavities, water pools, bark loss, fungal fruiting bodies, epiphytic plants, wildlife diversity, and historical value.
  - A species-specific table links minimum girth to “potentially interesting,” “valuable,” and “truly ancient” statuses; thresholds vary by species and context.
  - Caution: large girth does not guarantee ancient status; assessment should combine girth with visual indicators and condition.

- Practical note on ancient-tree guidance
  - Species-specific thresholds are provided to inform field judgments, with guidance on measurement (DBH at 1.3 m) and interpretation.
  - The approach emphasizes holistic assessment rather than relying on girth alone.

- Integration and emphasis for analysts
  - The handbook supports reproducible, auditable, and comparable habitat surveillance data across years and surveys.
  - Ensures underlying data are accessible for secondary analyses, policy evaluation, and cross-survey trend analyses.