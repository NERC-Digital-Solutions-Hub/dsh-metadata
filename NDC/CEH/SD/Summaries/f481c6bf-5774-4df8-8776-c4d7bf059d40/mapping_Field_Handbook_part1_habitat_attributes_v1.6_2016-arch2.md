# GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 1: Habitat attributes

- Purpose and scope
  - Field protocol to map habitat attributes for the Glastir Monitoring and Evaluation Programme.
  - Aims to produce consistent, time-series environmental data for monitoring health and policy performance; aligns with Countryside Survey data for historical trend analysis.

- Data concepts and outputs
  - Alpine of Broad Habitats (BH) and Priority Habitats (PH) mapped in a GIS Editable Polygon/Habitats layer; PHs nest within BHs.
  - Two mapping keys: Vegetation Key (based on species composition) and Wood/woody-feature Key (woody features).
  - Attribute structure with primary (core BH/PH) and secondary (descriptive) attributes; component-level details (species, canopy, etc.).
  - Emphasis on reproducibility, dataset storage/updating on portals, repeat-squares mapping, and change-tracking.

- Mapping approach and keys
  - Editable polygons for unenclosed/enclosed habitats; polygons can carry BH/PH attributes and component attributes.
  - Vegetation Key assigns patches to BH/PH by floristic composition; exceptions for habitat complexes and coastal PHs.
  - Wood/woody feature Key classifies woody features (trees, belts, clumps, scrub, lines) by structure and canopy; guides BH/PH vs linear features (hedges, lines of trees).
  - Canopy thresholds (e.g., around 25%) influence BH/PH allocation; use woodland key first to decide woodland-type vs line.

- Recording and attributes
  - Primary attributes determine BH/PH; secondary attributes add descriptive detail.
  - Species data: minimum of two and maximum of four characteristic species per polygon; percent cover categories provided.
  - DBH and veteran trees: DBH recorded where applicable; up to 10 veteran trees per square, limited by species.
  - Broad range of themes across BHs: Forestry, Agriculture/Natural Vegetation, Inland Physiography, Inland Water, Coastal features, Structures, etc.

- Major habitat categories
  - Broad Habitats: woodland types (broadleaf, coniferous, mixed, beech/yew), boundaries/linear features, arable/horticultural land, grassland types, moorland/heath, fen/marsh/swamp, bog, rivers/standing waters, montane/inland rock, urban, coastal/marine interfaces, and mosaics.
  - Priority Habitats (PH): key open-water, peatland, and specialized grasslands; GIS masks constrain native ranges post-survey.
  - Framework supports recording component-level details alongside polygon-level classifications.

- Ponds, standing water and aquatic habitats
  - Ponds defined by size (25 m2 to 2 ha) and water presence (typically ≥4 months); all ponds in a square must be identified.
  - Boundaries set by winter water levels; use vegetation breaks, water marks, or topography.
  - Temporary ponds identifiable by wetland vegetation and shoreline indicators.
  - One pond per square selected for detailed condition assessment.

- Woodland attributes and forestry guidance
  - Distinguishing BHs vs PHs in woodlands; PH criteria applied when floristic composition meets PH rules.
  - Woodland types/features: primary attributes include Woodland/Forest, belts, clumps, scattered trees, scrub patches; secondary attributes capture species and composition.
  - Recording/management: notes on forest management, edge rides, tree health (disease), and regeneration.
  - Orchard guidance: traditional orchards defined by low density, long-lived trees with permanent grass sward; margin orchards use Arable/Horticulture as primary attributes.
  - DBH measurement guidelines emphasize consistent measurement on the thickest stem for age estimation when possible.

- Non-native species and tree health
  - Record non-native invasive species within habitats; examples include rapeseed, Buddleia, Mimulus, Reynoutria.
  - Pilot data capture for tree diseases (e.g., Ash dieback, Sudden Oak Death, Dutch Elm disease) with dedicated fields.

- Bare ground, margins, and clearfell
  - Bare ground treated as context-dependent; record detailed bare-ground attributes when relevant.
  - Clearfell scenarios: document post-operations habitats and whether restoration returns to heathland or remains conifer woodland.

- Historic environment assets (HEA)
  - Recording of Historic Environment Assets (SAMs/HEFs) via fieldnote forms; documentation includes SAM numbers/PRNs and photography for condition records.
  - ~1,400 site types; procedures for threat identification and condition assessment.

- Condition assessment and data quality
  - Condition classes range from Excellent to Damaged; includes guidance notes and photographic examples.
  - Practical field tips: mapping order, extents vs shapes, and avoiding over-detailed GPS mapping.
  - Change management: 2016 protocol for repeat CS squares focuses on genuine change and correcting mis-allocations; emphasize attribute changes and spatial extent over absolute precision.

- Data collection, editing, and workflow
  - Mapping a square typically 2–4 days; prioritize complete area maps, primary attributes, representative species per parcel, and core pond/inland water data.
  - Minimum Mapping Unit (MMU) is 1/25 ha (400 m2); strategies to handle edge-cases include merging, splitting via UPDATE, and careful mosaic use.
  - Editing guidance: 1:5000 scale or better; strict rules for line/edge creation, and ensuring polygons reflect extent rather than exact geometry.

- Appendices and practical notes
  - Mapping notes on strategy, line mapping, snapping, and line adjustment; guidance on building/adjusting line features, intersections, splits, and endpoints.
  - Emphasis on consistent data capture, minimizing GPS-centric mapping unless required, and aligning with land-use/habitat semantics.

- Output expectations for analysts
  - Standardized GIS-ready BH/PH datasets with component-level attributes where applicable.
  - Robust time-series data to support trend analyses and policy evaluation.
  - A coherent, cross-survey compatible repository enabling data sharing and long-term environmental monitoring across Wales and the Glastir programme.

- Visit status and data management (as described in the Visit Status guidance)
  - VISIT_STATUS field: 0 unsurveyed, 1 IN PROGRESS, 2 COMPLETED, 3 REFUSED ACCESS.
  - Use to track survey progress, determine when to complete features, and triage squares.
  - Practical search methods:
    - Use Find to locate features by layer and VISIT_STATUS (0 or 1) with quick flash-to-map.
    - Use SELECT BY ATTRIBUTE to highlight unsurveyed/in-progress features across layers; supports multi-criteria searches.
    - Use ATTRIBUTE TABLE to manage selections; allows inverting selections to identify non-completed features.
  - MMU-related guidance includes handling small protrusions, updating via UPDATE to split/merge polygons, and combining selections across master and non-master layers.
  - Approach encourages not relying solely on GPS; focus on land-use and habitat semantics for accurate mapping.

- Identifying Ancient Trees (Ancient/Veteran trees)
  - Ancient trees defined by age-related characteristics; not solely by size.
  - Key indicators include large girth, substantial dead wood, hollow trunks, cavities, water pools, bark/decay features, fungal fruiting bodies, epiphytes, and high wildlife interdependencies.
  - Caution: diameter/girth alone can be misleading; use a holistic assessment of old-age indicators.
  - Girth-based guidance provides species-specific thresholds (minimum girth or diameter) to inform veteran status, but concludes that species vary and context matters.
  - Measurement note: diameter at breast height (DBH) is commonly recorded at 1.3 meters; relationship between girth and age is species- and condition-dependent.

- Practical notes on tree girth guidance
  - Species-specific, tiered thresholds link maximum potential girth to age indicators; rule-of-thumb notional thresholds suggest notable status when reaching certain proportions of max girth for the species.
  - The document includes detailed species-specific figures and calculations to support veteran-tree assessment and recording.