# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Field survey methodology for mapping habitat types and landscape features across the UK Countryside Survey 2007 (CS2007).
- Digital data collection enables time-series analyses and broad policy/science applications.
- Outputs designed for self-serve exploration (dashboards) and cross-topic data use.

## Data Model and Core Features
- Three spatial feature types:
  - Areas (polygons): map habitat types, change, and attributes; minimum area 1/25 hectare (400 m2); may contain multiple components.
  - Lines (linear features): woody features, fences, walls, etc., with events along lines; minimum length 5 m.
  - Points: individual landscape elements (e.g., trees, ponds) with components.
- Components and thematic attribute editors (e.g., Physiography, Forestry, Agriculture/Natural Vegetation, Inland Water, Coastal, Recreation, Transport).
- Features support multiple components and hierarchical attribute organisation.

## Habitat Classification and Keys
- Broad Habitats (BH) cover 1–19 categories plus mosaics; Priority Habitats (PH) mapped as subdivisions where relevant.
- Classification keys:
  - Vegetation Key: assigns primary/secondary attributes to BHs/PHs based on plant composition and vegetation structure.
  - Key to Woodland Types/Features: classifies woody vegetation by canopy form and assigns BH/PH attributes.
- Woods/woodlands have primary attributes and secondary qualifiers; can be BH or PH.

## Resources for Classification
- Vegetation Key: fundamental for habitat and PH assignments using plant composition and structure.
- Key to Woodland Types/Features: categorises woody vegetation by canopy form and assigns BH/PH attributes.

## Digital Mapping System and Workflow
- CS Surveyor extension in ArcMap used to view/edit features within a 1 km square.
- Change recording is mandatory for all edits to distinguish real ecological change from data errors.
- Regular updates and bug reporting via helpdesk and wiki; emphasis on data correctness and consistency over exact spatial precision.

## Editing and Data Management Processes
- Area editing (examples):
  - Create New Area: assign BH/PH, assess Broad Habitat accuracy, record change reason (real change, error correction, or baseline).
  - Copy Area: replicate attributes from a source area.
  - Split Areas: digitise split lines to create multiple areas; adhere to MMU constraints.
  - Modify Area: adjust boundaries/shared nodes; manage topology edits.
  - Update Areas: create new area by updating/intersecting existing areas; can consolidate multiple edits.
  - Saving: use Save Session to persist changes; unsaved edits are discarded on log off.
- General rules:
  - New habitat changes trigger new polygons; minimum mapping unit (MMU) is 400 m2.
  - When habitat type remains but species composition changes, a new polygon is not always required.

## Ponds and Pond Surveying
- Each square identifies all ponds; one pond is selected for detailed condition assessment (survey pond) via a preselected list or random selection.
- CS2007 Pond Mapping Recording Sheet captures pond ID, area, water presence, loss/creation reasoning, and notes.
- Guidelines cover temporary ponds, pond vs. other waters, connected pond boundaries, and pond attributes for later sampling.
- Post-mapping, survey ponds are used for detailed ecological/water chemistry assessments.

## Point Features and Woody Features
- Points: single features (e.g., individual trees, ponds); individual editing; veteran trees recorded (up to 2 per species per square).
- Buffers: presence/absence of buffer zones around mapped features.
- Woody Linear Features (WLFs) and woodland structure:
  - Distinguish natural shapes vs hedge-like management; record as lines or belts.
  - Features include belts of trees, belts >20 m, clumps, individual trees, and scrub patches; buffers and related attributes captured.

## Non-native Species and Additional Notes
- Guidance includes recording a set of non-native species encountered within habitats.

## Outputs, Uses, and Data Products
- Provides a comprehensive standard for data capture to enable self-serve dashboards and cross-topic data use.
- Emphasises auditable, consistent data describing habitat extent and change.
- Relevant for UK Biodiversity Action Plans reporting and time-series analyses.

## Practical Constraints for Data Collection
- Spatial accuracy prioritises extent/change over pinpoint positioning.
- Editing typically restricted to scale 1:5000 or better; MMU constraints apply for lines, margins, and areas.
- When uncertain, follow vegetation/habitat guidance to classify.

## Habitat Categories (BH) and Notes
- Detailed BH categories (e.g., BH1 Broadleaved Mixed & Yew, BH2 Coniferous Woodland, BH13 Rivers/Streams, BH14 Standing Open Waters, BH19 etc.) with notes on supplementary mosaic classifications where needed.
- Mosaic and patch-based classification options for ambiguous delineations.

## Appendix Highlights and Data Quality
- Appendix 6: Squares with loops - lists unique squares with looped/corrupted event data and prescribed procedures:
  - Change event themes to Deleted Feature, set Reason for Change to No Change, complete Visit Status to Completed, then delete loops and reinstate features from field data.
- Appendix 5: Girth sizes of veteran trees - rules of thumb for assessing veteran-tree significance by species.
- Appendix 1/Appendix 2: Supporting field assessment materials and coding references (CS2000 lineage and attribute codes), illustrating legacy data handling.
- Appendix 3: CS2007 Pond Mapping Recording Sheet structure and usage details.

## Final Note
- The Field Mapping Handbook serves as the framework for standardized data capture, editing, pond surveying, and woodland/wetland classification to support ecological reporting, trend analyses, and policy-relevant data products.