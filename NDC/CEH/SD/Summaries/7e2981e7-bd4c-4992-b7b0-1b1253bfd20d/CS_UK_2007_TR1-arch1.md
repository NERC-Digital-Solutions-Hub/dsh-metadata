# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Aim and scope
- Documents the field mapping framework for Countryside Survey 2007, focusing on digital mapping of Broad Habitats (BHs) and Priority Habitats (PHs) within 1 km squares to report land cover change and biodiversity trends.
- Establishes a time-series dataset to support policy monitoring and biodiversity assessments, with standardized data provenance and discoverability.

## Data model and mapping units
- Mapping entities: polygons (areas), lines (linear features), and points (discrete elements) edited within each 1 km square.
- Minimum mappable unit (MMU): 1/25 hectare; features below MMU are not mapped unless part of a larger feature.
- Detailed pond mapping protocol: every pond mapped; one pond per square chosen for detailed condition assessment (survey pond).
- Integration across themes: ponds and water features linked across Inland Water, Agriculture/Natural Vegetation, and Structures where relevant.
- Scale constraints: general editing of areas < 1:5000; point edits require 1:5000 or finer.

## Digital mapping system and workflow
- Platform: CS Surveyor extension within ArcMap; dedicated edit sessions with predefined symbology.
- Change recording: mandatory tagging of genuine changes, error corrections, and new baselines; session saves and commits are controlled to maintain data integrity.
- Data provenance: strong emphasis on metadata, source tracking, and making datasets discoverable (including cross-round provenance with CS1990/CS2000 data where appropriate).

## Vegetation and woodland classifications
- Vegetation Key: assigns primary/secondary attributes to BHs/PHs based on species composition within uniform habitat polygons.
- Woodland types/features: classify by canopy form, density, width, and structure; used to allocate woodland components to BH/PH at polygon and component levels.
- Woodland components: include primary (e.g., belt of trees, patch of scrub) and secondary attributes (species, cover, DBH); allows mosaics within a single polygon.

## Broad Habitats (BHs) and Priority Habitats (PHs)
- BHs provide the primary habitat framework; PHs nest within BHs and offer refined attributes post-survey.
- Example BH categories include broadleaved woodland, coniferous woodland, arable, improved grassland, various grasslands, heath, bog, rivers/streams, standing water, urban, and other marine/inland features.
- PHs are mapped within BHs with GIS masks applied post-survey to constrain extents (e.g., upland vs. lowland).

## Habitat mapping methodology
- Habitat attributes: per polygon, record habitat type, dominant vegetation, and indicator species; unenclosed uplands receive enhanced detail when possible.
- Unenclosed vs enclosed habitats: unenclosed uplands linked to CS1990 data for improved detail; enclosed lowland polygons mapped within predefined BHs with PHs as relevant.
- New baseline PHs: when refining a BH into PHs, apply new baseline PH codes while preserving BH attributes.
- Non-native species: guidance to record notable non-native species for potential PH/BH qualifiers.
- Orchards: treated as agricultural within BH4, with orchards as secondary attributes; traditional orchards considered for PH.

## Pond mapping and sampling
- Pond definition: standing water body from 25 m2 to 2 ha, holding water for at least four months annually.
- Mapping process: all ponds recorded; a survey pond is randomly selected from mapped ponds within the square for detailed aquatic characteristics and water chemistry.
- Boundary identification: guidelines distinguish ponds from ditches, flushes, bogs, streams; temporary ponds (dry during survey) identified via hydrology cues.

## Point features and linear features methodology
- Points: edited individually (e.g., trees, standing water, ponds); each point must have at least one component and can be moved, added, or deleted with attribute copy options.
- Woody Linear Features (WLFs): include hedges, lines of trees, belts, and other linear woody forms; classified by natural vs managed shapes, with attributes like DBH, species, canopy cover, margins, and buffers.
- Linear features: recorded as events along lines (e.g., fences, hedges, banks); lines can be split, merged, or updated with new events; multiple events can exist on a single line.

## Data quality, provenance, and reporting
- Provenance and metadata: datasets carry lineage and change history; ensure discoverability and traceability across survey rounds.
- Change reporting: distinguish genuine landscape change from mis-recordings; integrate older datasets (CS1990) to improve accuracy for unenclosed habitats.
- Data integrity: enforce MMU compliance, consistent habitat coding, and consistent application of vegetation/woodland keys.
- Documentation and support: CS Surveyor is maintained with bug-reporting channels and system updates.

## Practical field guidelines and constraints
- Survey scale and navigation: ArcMap editing requires zooming to up to 1:5000 for points; polygon edits emphasize extents over precise locations.
- Mosaic mapping: indistinguishable habitats or sub-MMU components may be described as mosaics with defined shares (e.g., 30% Other Bog, 70% Dwarf Shrub Heath).
- Minimum data capture: each habitat type requires recording of multiple species per polygon; standardized vegetation cover percentages are applied.
- Buffers and curtilage: document buffer zones and respect landowner or curtilage constraints when mapping.

## Appendices and data artifacts
- Field assessment and coding references: field assessment forms, CS2000 codes, pond mapping sheets, veteran trees guidelines, and random-number selection procedures.
- CS2007 pond recording and pond selection forms: detailed templates for pond counting, area, water presence, and reasons for pond creation/loss.
- CS2000/CS2007 code sheets: extensive code lists for attributes, species, and landscape features to support standardized entry.
- Appendix 5: veteran tree girth rules of thumb for assessing notable trees.
- Appendix 6: examples of squares with loops and procedures to correct corrupted loop data by deleting and re-adding features.

## Practical notes for analysts
- The handbook provides a comprehensive, field-tested workflow for data capture, editing, and validation in a GIS-enabled environment, with explicit procedures for line edits, shared nodes, and quality controls.
- It emphasizes data interoperability across survey rounds, robust provenance, and actionable outputs for policy and biodiversity monitoring.