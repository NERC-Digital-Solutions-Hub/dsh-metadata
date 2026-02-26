# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and scope
  - Provides methodology for field mapping habitats and landscape features in Countryside Survey 2007 (CS2007) across 1 km squares.
  - Aims to report land cover change by Broad Habitats (BHs) and Priority Habitats (PHs), including new PHs and upland/enclosed vs unenclosed differences.
  - Introduces digital data collection and a unified GIS model to enable time-series analysis and UK biodiversity monitoring aligned with Biodiversity Action Plans.
  - Includes Wales mapping and enhances over CS1990/CS2000 with more detailed habitat attributes.

- Mapping framework and data model
  - Data units: polygons (areas), lines (woody/linear features), and points (individual features) within each 1 km square.
  - Minimum mapping unit (MMU): 1/25 hectare (400 m2); polygons below MMU generally not mapped unless representing a distinct habitat occurrence.
  - Emphasis on reporting extent/change of BHs/PHs; spatial accuracy secondary to correct habitat representation.
  - Polygon-level BH/PH allocation; component-level attributes organized under themes (Inland Physiography, Inland Water, Agriculture/Natural Vegetation, Forestry, Structures, Recreation, Transport).
  - Woodland rules: woodland components defined with primary/secondary attributes; include buffer considerations around features.
  - Ponds and aquatic features require detailed pond mapping and a dedicated pond recording workflow.

- Keys and classification
  - Vegetation Key: assigns uniform vegetation stands to BHs/PHs based on plant composition; handles habitat complexes and coastal exemptions.
  - Key to Woodland Types/Features: classifies woody features by canopy form (trees, shrubs, belts, clumps, lines) and assigns BH/PH and related attributes.
  - Two-tier approach: vegetation key first, then woodland key for precise woodland attributes; ensures consistent BH/PH allocation.

- Broad Habitats (BHs) overview
  - BH categories cover broad woodland, grassland, wetlands, aquatic, urban, boundaries/linear features, and mosaic/polygons with multiple habitats.
  - Examples include BH1 (Broadleaved/Mixed woodland), BH2 (Coniferous woodland), BH4 (Arable/Horticultural), BH5/6/7/8 (various grasslands), BH11/12 (Fen/Marsh/Swamp and Bog), BH13 (Rivers/Streams), BH14 (Standing Open Waters/Canals), BH23 Mosaic, among others.
  - BHs provide a structured framework for habitat reporting and time-series analysis.

- Ponds and aquatic features
  - Every pond in a square must be identified; record basic attributes on a dedicated CS2007 Pond Mapping Recording Sheet.
  - A survey pond is selected per square for detailed condition assessment (randomly from mapped ponds or preselected options).
  - Pond boundaries can be difficult to delineate; includes rules for temporary springs, delineation, and distinctions among ponds, ditches, flushes, and connected waters.

- Habitat and vegetation attributes
  - Attributes include primary/secondary codes, vegetation type, species, and cover proportions (often up to 4 species per polygon; cover categories from <10% to 95–100%).
  - Non-native species lists recorded where present.
  - Orchard and woodland management attributes highlighted to ensure accurate BH/PH assignment.

- Data collection system and workflow
  - CS Surveyor: a custom ArcMap extension integrated with a central database; requires user login and fault reporting.
  - Field workflow prioritizes detecting ecological change and correcting mis-allocations from prior surveys; differentiates real change from data errors.
  - Landscape Feature Editing toolbox used for editing areas/lines/points; changes saved via session Save, End Session to discard.
  - Data governance and metadata considerations highlighted; data sharing can be a barrier.

- Methodology for mapping areas (areas, lines, points)
  - Area editing
    - Modify polygons, copy attributes, split/merge areas; ensure identical attributes when merging; document reasons for changes.
    - Polygon may contain multiple components; component-level attributes editable.
  - Copy area attributes
    - Copy attributes from a source area to multiple targets; overwrites existing attributes.
  - Split Areas
    - Digitize split line; ensure resulting parts meet MMU; edit attributes for new areas.
  - Merge Areas
    - Merge areas with identical attributes; inherit attributes from a source area.
  - Modify Area
    - Adjust shared boundaries/topology via topology edit; reposition shared nodes as ground truth dictates.
  - Update Areas
    - Create a new update polygon by splitting/merging affected areas to reflect new intersecting areas.
  - Stop Editing
    - Save or End Session to finalize or discard changes.

- Methodology for mapping lines and events
  - Linear features (<5 m wide, >20 m long) with events capturing along-line changes (e.g., fence types).
  - Edit event attributes, copy/move events; adjust event lengths on map.
  - Margin mapping (field margins/hedgerows) captured as line events alongside larger features.

- Point features methodology
  - Points (<20 m × 20 m) updated for attributes; may include multiple components; buffers may be recorded.
  - Veteran trees: up to 10 per square (max 2 per species) with dedicated data fields per tree.
  - Buffer zones and access considerations recorded as Yes/No.

- Practical notes and support
  - Field-ready instructions for ArcMap, CS Surveyor integration, fault reporting.
  - Emphasis on verifying mapped components and prioritizing habitat extent over exact spatial precision.
  - Helpdesk and update channels; methodology updates in Latest News.

- Challenges and considerations for monitoring frameworks
  - Barriers include:
    - Data gaps or low-quality data
    - Data access delays
    - Organizational data silos
    - Public sharing requirements
    - Keeping data up to date
    - Inadequate metadata hindering verification
    - Data format/transformation efforts
    - Clear communication of complex findings
    - Implementing data governance and sharing standards

- Practical implications for policy and decision-making
  - Provides a structured, repeatable approach to biodiversity and habitat data collection to scrutinize policy, monitor progress, and inform future decisions.
  - Emphasizes change detection, transparency, and governance to support evidence-based policymaking and impact assessment.