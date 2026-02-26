GLASTIR MONITORING & EVALUATION PROGRAMME MAPPING FIELD HANDBOOK Part 1: Habitat attributes

- Purpose and scope
  - Field handbook for the Glastir Monitoring and Evaluation project (GMEP) to map habitats in 1 km squares using GIS, aligning with historical time-series methods and policy relevance. Latest revision noted as 1.6 (2016).
  - Defines core data model (Broad Habitats and Priority Habitats), mapping at polygon level, and detailed component-level attributes organized into themes (e.g., Forestry, Agricultural Crops, Inland Water).

- Core data model and mapping approach
  - Broad Habitats (BH) and Priority Habitats (PH) as primary classifications; BHs are polygon-level, PHs nest within BHs where relevant.
  - Two primary keys guide classification: Vegetation Key (plant species composition) and a woodland types/features key (woody features such as belts, lines, hedges).
  - Component-level data capture includes detailed attributes for themes like woodland structure (DBH, canopy cover, species), forestry features, agricultural/grassland attributes, and linear features (ditches, fences, hedges).

- Mapping units and accuracy
  - Minimum Mapping Unit (MMU) is 1/25 hectare (400 m2); areas smaller are not mapped as discrete polygons unless part of a larger unit.
  - Emphasis on accurate extent and relative location over perfect geometric precision.

- Ponds and water features
  - Detailed pond mapping protocol: every square with ponds identified; one pond per square selected for a detailed freshwater survey.
  - Pond definition: standing water 25 m2 to 2 ha, typically present for at least four months/year; boundary delineation may extend beyond visible water due to seasonal changes.
  - Clear distinctions among ponds, ditches, flushes, and other water bodies; includes temporary ponds and connected waterbodies.

- Woodland, trees, and veteran trees
  - Woodland features described within Forestry theme (woodland/forest, belts, clumps, scattered trees, scrub; with primary and secondary attributes such as DBH, species, canopy cover).
  - Veteran/ancient trees defined by age indicators, large girth, substantial dead wood, hollow trunks, epiphytic plants, and other characteristic features; non-native and dead trees can be ecologically important.
  - Tree girth thresholds are species-specific and presented in a reference table; however, girth alone is not definitive—shape, health, hollowing, and contextual features are considered.

- Boundaries, linear features, and woody linear features (WLFs)
  - Boundaries and linear features mapped as Broad Habitat 3 when area-wide ( >5 m wide or multiple features totaling >5 m).
  - WLFs include hedges, lines of trees, and similar features with attributes such as height, base height, linearity, species composition, DBH, management history, margins, and protection measures.

- Change mapping, repeats, and data quality
  - For repeat surveys, map genuine changes and correct prior misallocations; distinguish real habitat change from survey error.
  - Non-native/invasive species and tree diseases to be recorded where they occur above MMU; pilot data collection on diseases is encouraged.
  - Historic environment assets (HEA) recorded with unique identifiers (SAM No. or PRN) on standard forms and as polygon features in GIS.

- Field methodology and workflow recommendations
  - Start GIS work with points and lines, then build polygon extents; mosaic mapping used when unit-wide delimitation is not possible.
  - Ensure that primary/secondary attributes across themes are coherent and that component-level descriptions sum to 100% in mosaics.
  - Use tablet forms and ArcGIS layers for data capture; maintain unique identifiers and clear photograph naming conventions; prioritize field data quality and traceability.
  - Practical notes emphasize not overspecifying boundaries, mapping partial features where uncertain, and considering margins/buffers for conservation.

- Practical field tips and cautions
  - Prefer plausible extents and recognizable features over meticulous boundary delineation in uncertain cases.
  - If a feature cannot be fully mapped in one visit, map what you can and return to refine later.
  - Use buffering to support cross-compliance contexts where applicable.

- Visit status: monitoring data capture and QA
  - Every Event, Point, and Area includes a VISIT STATUS field to indicate survey progress and access constraints.
  - Status codes:
    - 0 = unsurveyed
    - 1 = IN PROGRESS
    - 2 = COMPLETED
    - 3 = REFUSED ACCESS
  - IN PROGRESS acts as a reminder to complete species composition where full extent is not yet verified.
  - COMPLETED should be used only after the feature is fully surveyed; otherwise keep as IN PROGRESS or REFUSED ACCESS.
  - Upon square completion, all features should be marked as COMPLETED or REFUSED ACCESS; status-aware layers help visualize progress.

- Tools and methods to manage VISIT STATUS
  - Layer options: Landscape Points, Landscape Events, Landscape Areas; search by VISIT STATUS using:
    - Find ( binoculars ) to locate features by status within a layer
    - Select by Attribute to highlight features by multiple criteria (e.g., unsurveyed or in progress) across a layer
    - Attribute Table to systematically work through selections; can invert selections to find non-completed features
  - Limitations:
    - Find searches one layer at a time and cannot combine criteria across layers
    - Select by Attribute can highlight features across the map but requires manual inspection for non-list results
    - Attribute Table requires careful handling to avoid missing features when criteria are complex
  - Tips:
    - Use unique values for quick selection
    - Save and reload search terms for efficiency across different parts of a square
    - Use “Zoom to feature” to locate items obscured by the search window
    - Clear selections to reset the view when needed

- Dealing with MMUs in editing
  - If a small piece lies near an edge, include it with the adjoining polygon; if a part is the end of a long feature, leave it.
  - Two main options to handle MMU-sized splits:
    - Merge and then split (may lose field data)
    - Use UPDATE tool to split/merge in one operation; carefully select the area to modify
  - Copy+ and Copy- functions allow adding/removing areas across layers (e.g., Landscape Areas vs MasterMap) in a flexible, non-linear editing workflow.

- Ancient trees: identification guidance (summary)
  - Ancient/veteran trees are characterized by age indicators beyond general size, including large girth for species, substantial dead wood, hollow trunks, cavities, epiphytic flora, and a suite of wildlife indicators.
  - Girth thresholds are species-specific and presented as minimums; however, girth alone is not determinative—visual assessment of age indicators and context is essential.
  - The guidance provides a table with species-specific maximum girth values and corresponding qualitative statuses (potentially interesting, valuable, truly ancient) used to support field assessments.

- Data management and accessibility
  - Data collection relies on tablet-based forms and GIS layers; HEA (Historic Environment Assets) have polygon footprints and unique identifiers linked to forms.
  - Clear field data validation, photograph naming conventions, and cross-layer interactions are emphasized to ensure data integrity and traceability.

- Endnotes and next steps
  - The handbook references future Parts (e.g., Part 2 on Habitat Change, Part 3 on vegetation keys) and reinforces standardized field practices and GIS consistency to support ongoing mapping work.