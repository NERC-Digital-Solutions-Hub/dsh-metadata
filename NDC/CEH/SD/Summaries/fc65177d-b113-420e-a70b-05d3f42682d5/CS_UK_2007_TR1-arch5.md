# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Purpose and Scope
- Establishes a comprehensive protocol for Countryside Survey 2007 (CS2007) field mapping, including digital data capture, habitat classification, and woodland/linear features.
- Aims to produce harmonised, detailed GIS datasets of Broad Habitats (BH) and Priority Habitats (PH) across 1 km squares, with change reporting and time-series continuity.
- Introduces a unified CS Surveyor digital mapping model that consolidates vegetation, woodland, boundaries, structures, and physiography into one editable map.

## Data Model and Classification
- Datasets comprise polygons (areas), lines (linear features), and points (point features) representing habitats and landscape elements.
- BH/PH are mappable at the polygon level; detailed attributes recorded at the component level under them.
- Classification includes 21 BH types (plus mosaic) and various coastal, inland, and freshwater types, each with detailed attribute schemas.
- Two core keys guide classification: Vegetation Key (habitats and attributes) and Woodland Types/Features Key (woody structure and related BH/PH attribution).
- Thematic attribute organization covers Inland Physiography, Inland Water, Agriculture/Natural Vegetation, Forestry, Structures, and Coastal features.

## Data Capture System and Workflow
- CS Surveyor: a custom ArcMap extension used to capture/edit data in each 1 km square.
- Change recording is mandatory, distinguishing genuine habitat change from corrections.
- Surveyors edit Areas (polygons), Lines (linear features), and Points within the editing environment; spatial accuracy is subordinate to accurately representing habitat extent and change.

## Mapping Units and Change Rules
- Minimum Mapping Unit (MMU) is 1/25 hectare; smaller unmapped features are not separately recorded.
- New polygons created when habitat type changes; internal species composition changes may not warrant new polygons.
- Mosaic polygons allow multiple habitat types within a polygon, with component percentages summing to 100%.
- Change interpretation categories: REAL CHANGE (true shift), ERROR CHANGE (correction of prior error), NEW BASELINE (subdivision of a habitat type).

## Pond and Water Features
- All ponds in a square must be recorded; a survey pond is selected for detailed condition assessment (random unless preselected).
- Pond data include area, water presence, boundary, and potential reasons for loss/creation; detailed conditions captured by freshwater surveyors.

## Point Features and Woody Elements
- Points capture individual trees, shrubs, veteran trees, water bodies, and discrete features; editing is scale-dependent (≤1:5000).
- Woody Linear Features (WLFs) cover hedges, rows, belts, and lines of trees; classification differentiates natural-shaped lines vs. managed hedges.
- Buffers, veteran trees (up to two per species per square), and DBH measurements are recorded; Points support multiple components with component-based editing.

## Linear Features: Events and Margins
- Linear features are managed as lines with events (e.g., fence, hedge, ditch) along their length; continuous lines may represent multiple events.
- Events have attributes (type, length, height, condition, margins) and associated vegetation where relevant.
- If a linear feature exceeds minimum size, it may be converted to an area and assigned BH/PH accordingly.

## Woodland: Habitat Attributes and Management
- Woodland BH/PH attributes can be at the polygon level; forestry attributes captured at the component level.
- Primary woodland attributes include belts, clumps, and larger woodlands; secondary attributes cover species, cover, and DBH.
- Forestry details include management signs, regeneration, planting, windthrow, and other indicators.
- Orchard guidance emphasizes identifying traditional orchards for PH mapping; orchards treated as an additional attribute.

## Data Quality, Metadata and Governance Considerations
- Rigorous change-tracking framework ensures provenance: REAL vs ERROR vs NEW BASELINE changes.
- Detailed attribute schemas and keys support consistent data capture across teams and squares.
- Tooling acknowledges potential CS Surveyor bugs; support channels include a helpdesk and wiki-based fault logging.
- Documentation covers extensive attribute definitions, species lists, and cover percentage coding to support reproducibility and interoperability.
- Data capture is designed to support UK biodiversity monitoring with emphasis on time-series continuity.

## Challenges and Considerations for Data Stewards
- Incomplete understanding of user needs and interoperability across habitats, tools, and teams.
- Timely delivery and consistent adherence to standards across diverse systems and field conditions.
- Ensuring metadata completeness (habitat keys, attribute schemas, change logs) and edit traceability.
- Managing complex mosaic mappings and post-survey GIS masking for PH/BH delineations.
- Handling large volumes of high-detail data (vegetation species, habitat attributes, woody features) while maintaining quality.

## Appendix and Practical Details
- Guidance on non-native species and habitat recording.
- Detailed BH/PH attribute definitions, including woodland, margins, calcareous/acid grasslands, bogs, fens, rivers, lakes, and coastline.
- Pond boundary identification, temporary ponds, and distinction from ditches/streams.
- Orchard, margins, and agricultural margins/use classifications.
- CS2000 and Field Assessment Booklets (FABs) provide historical context and coding references for mapping and data capture.