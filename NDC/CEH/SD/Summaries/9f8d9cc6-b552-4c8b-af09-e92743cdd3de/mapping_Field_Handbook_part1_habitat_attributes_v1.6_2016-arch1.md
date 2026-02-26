# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 1: Habitat attributes

- Purpose and outputs
  - Map habitat attributes in 1 km squares to support Glastir Monitoring and Evaluation and enable time-series analyses.
  - Maintain compatibility with Countryside Survey methods for historical trend comparisons.
  - Produce editable polygons with Broad Habitats (BH) and Priority Habitats (PH), plus vegetation and woodland attributes; establish a framework for data sharing and reuse.

- Classification framework
  - BH and PH are mapped at the polygon level; BHs may nest PHs as components.
  - Habitat types are divided into Broad Habitats (e.g., woodland, grasslands, wetlands, urban, etc.) and Priority Habitats (subcategories like Purple Moor Grass, reedbeds, fen, bog, calcareous/acid grasslands, etc.).
  - Upland/lowland, enclosed/unenclosed, and coastal/intertidal distinctions applied via GIS masks post-survey.

- Keys, mapping approach, and attributes
  - Vegetation Key: assigns patches to BH/PH based on plant composition and canopy attributes; supports nesting PHs within BHs where applicable.
  - Woodland Types/Features Key: classifies woody vegetation by structure, canopy, and spatial arrangement; defines primary and secondary attributes (e.g., Woodland/Forest, Belt of Trees, Clump of Trees) and details (species, DBH, growth stage).

- Field layer structure
  - Surveyors create polygons for unenclosed/enclosed habitats; a polygon may receive BH and one or more PH attributes.
  - Field entries include species composition, canopy cover, primary/secondary attributes, and relevant woodland/agricultural attributes.

- Data quality, provenance, and metadata
  - Emphasises tracking data sources and ensuring datasets are discoverable with metadata.
  - Documentation supports reproducibility and time-series analyses; GIS masks support boundary delineation.

- Mapping workflow and time management
  - Practical time cap: roughly 4 days (about 30 hours) per square; typical mapping is 2–3 days (20–24 hours).
  - Parallel mapping of areas, lines, and points to maximise efficiency.
  - Mapping priorities: complete area habitat map, record primary attributes and representative species, map woody features and water bodies, and record veteran trees and ponds.
  - Time-saving tips: limit species per parcel; avoid over-detail under time pressure; do not map habitats with GPS for precise positioning—emphasise relative placement and consistency.

- Repeat surveys and change mapping
  - In 2016 a subset focused on change in land cover/landscape features rather than de novo mapping.
  - Surveyors must distinguish genuine change from previous data errors (error change vs real change) and adjust polygon attributes accordingly.
  - Verification of polygon attributes, species composition, and habitat type against field observations is required.

- Detailed habitat and attribute guidance (highlights)
  - Non-native species: record occurrences within habitats (e.g., Buddleia, Reynoutria).
  - Tree diseases: capture woodland/tree-feature disease data (e.g., Chalara).
  - Bare ground: record as habitat component when extensive; otherwise nested under broader types.
  - Post-felling/felled areas: describe habitats based on canopy closure and regrowth rather than assumed future land use.
  - Woodland and hedgerows: document woody features with primary/secondary attributes; record veteran trees and DBH with standardized guidelines.
  - Orchards: PH category for traditional/orchards; map within timber/agricultural contexts with low-intensity management and diverse age structure.
  - Ponds and inland water: inventory ponds in every square; select a pond for detailed condition survey; delineate boundaries using standard criteria (winter water level, vegetation changes, water marks).
  - Montane and inland rock: capture montane PHs and inland rock outcrops/scree, including calcareous/acid grasslands.
  - Rivers, standing waters, wetlands: map canals, rivers, lakes, ponds, reedbeds, tall herb wetlands; apply primary qualifiers (Fen, Marsh, Swamp, Reedbed, Aquatic macrophytes).
  - Wetland mosaics: manage PHs and BHs for wetland communities; document hydrological context.
  - Boundary mosaics: describe as mosaic with component percentages when boundaries are indistinct or MMU-limited.

- Specific data capture and field practices
  - Species and coverage: record at least two species per polygon (up to four) with cover percentages.
  - Sward attributes: height, tussockiness, variation; document management indicators (grazing, mowing, leys).
  - Woody features: for woodland polygons, record DBH, species composition, cover, and management indicators; differentiate natural vs hedgerow-like woody features.
  - Buffers/margins: document buffer zones and margins with separate composition if > MMU.
  - Historic Environment Assets: record Scheduled Ancient Monuments (SAMs) and Historic Environment Features (HEFs) with identifiers; provide notes and photography for condition assessment.

- Ponds: identification, boundaries, and condition
  - Every square with ponds is inventoried; a dedicated pond survey is selected for detailed sampling.
  - Boundaries rely on winter water level and hydrological/vegetation indicators; temporary ponds recorded if water for at least four months.
  - Ponds may merge with fen/marsh; boundary decisions may be semi-arbitrary in bog contexts.

- Spatial and data quality considerations
  - Prioritise extent and consistency of polygons over exact shapes; polygons should be appropriately sized and roughly placed.
  - Minimum mappable unit (MMU) is 1/25 ha (400 m2); features smaller may be merged or omitted.
  - Editing scale: editing requires scale < 1:5000; ensure minimum feature lengths and square boundary adherence.
  - Change recording in repeats: classify as Error Change vs Real Change; update polygon attributes accordingly.

- Data structure, reporting, and analysis
  - Comprehensive set of primary/secondary attributes and qualifiers across BHs, PHs, and woodland features.
  - Thematic data structure covers Forestry, Inland Water, Agriculture/Natural Vegetation, Structures, Recreation, Transport, Coastal features, and Inland Physiography.
  - Guidance notes provide decision rules for complex mosaics, wood-pasture, orchards, and calcareous/acid grasslands.
  - Purpose-built data model supports correlations, pattern identification, and predictive modelling; time-series analyses rely on consistent methodology, GIS masks, and metadata.

- Practical guidance for data analysts
  - Emphasises data provenance, version history, and metadata quality to support governance, policy evaluation, and scientific research.
  - Enables robust cross-habitat analysis and temporal trend detection through standardized attributes and repeatable workflows.

- Visit status and data querying (practical data-management tools)
  - Visit status fields (unsurveyed, IN PROGRESS, COMPLETED, REFUSED ACCESS) track survey progress and data availability.
  - Filtering approaches to locate unsurveyed/in-progress features:
    - Use Find to search by layer, field (VISIT STATUS), and code (0, 1, 2, 3); results highlight on the map.
    - Use Select by Attributes to highlight features matching criteria; can search for multiple terms but may not produce a list.
    - Use the Attribute Table to show selections; SHOW SELECTION must be used to focus on selected features; can invert selections to identify non-completed features.
  - MMU handling and editing tips
    - Small parts at the edge of a square may be integrated into adjacent polygons if MMU limitations prevent splitting.
    - UPDATE tool can split/merge polygons in one operation; use Copy+ and Copy- to combine areas from different layers and contexts when editing.
    - Freehand drawing can be combined with existing polygons through selection tools to avoid losing attributes during edits.

- Ancient trees guidance
  - Defines ancient/veteran trees by appearance relative to species, with indicators such as large girth, substantial dead wood, hollowing, cavities, decay, bark loss, and epiphytic life.
  - Girth-based thresholds are species-specific and should not be used alone; assess age using multiple indicators.
  - Provides a practical table of species-specific minimum girths as a rough guide, but emphasizes holistic assessment and contextual features.
  - Recognizes that some young trees may display ancient characteristics due to damage, so verification should consider multiple indicators.

- Overall takeaway for analysts
  - A structured, metadata-rich field-mapping framework enables robust data-driven questions about habitat distribution, change over time, and environmental relationships.
  - Consistent methodology, clear provenance, and practical data-management tools (visit statuses, MMU handling, and querying options) are central to reliable analyses, modelling, and policy-relevant insights.