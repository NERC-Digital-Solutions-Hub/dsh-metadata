# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Overview
- Establishes a nationwide, digitally captured mapping framework for habitat change and extent.
- Focuses on Broad Habitats (BH) and Priority Habitats (PH) with integrated vegetation and landscape features.
- Enables country- and UK-level reporting, with emphasis on change since previous surveys to support monitoring and policy needs.

## Data Model and Mapping Framework
- Mapping conducted in 1 km grid squares using a digital GIS model that aggregates prior themes (forestry, agriculture/natural vegetation, boundaries, structures, physiography).
- Surveyors edit a digital map representing all features in a square, recording change and correcting past classifications.
- Data types include polygons (areas), lines (linear features), and points (point features) with associated attributes and optional metadata.
- Minimum Mapping Unit (MMU) is 1/25 hectare (400 m2).

## Keys and Habitat Classification
- Vegetation Key: assigns areas to BH/PH based on plant composition and habitat attributes.
- Key to Woodland Types/Features: classifies woody features (line of trees, belt of trees, clumps, etc.) and supports BH/PH attribution.
- Clear guidance on when to classify areas as BH vs PH and handling enclosed vs unenclosed habitats.

## The Vegetation Key
- Allocates polygonal vegetation to BHs/PHs using primary/secondary attributes from species composition, physiography, and habitat context.
- Distinguishes enclosed (lowland) vs unenclosed (upland) habitats; incorporates refinements to support PH identification.
- PHs are nested within BHs; GIS masks may be used regionally for PH boundaries.

## Woodland Types and Features
- BHs can include belts of trees, lines of trees, clumps, woodland/forest, and other woody features.
- Attributes cover canopy, dominance, DBH, species, and ancillary features (buffers, veteran trees, management).
- Woodland attributes are captured at polygon and component levels; components capture finer-grained woodland types within a BH/PH polygon.
- Orchard considerations: traditional orchards may be PH; apply Orchard as an attribute with Gardens/ground where trees for curtilage cases.

## The Digital Mapping System (CS Surveyor in ArcMap)
- CS Surveyor integrated into ArcMap; surveyors log in, load the square, and edit polygon/line/point layers.
- Data frame holds layers with preset symbology; system enforces change recording for habitats/features.
- Guidance: edit at scales ≤ 1:5000; focus on habitat extent and change rather than precise spatial accuracy; regularly save sessions; End Session discards changes.

## Mapping Areas, Change, and Attributes
- Areas: edit via Landscape Feature Editing toolbox; key fields include BH/PH habitat assignment, change reason (REAL CHANGE vs ERROR CHANGE), and visit status.
- Determining Change: distinguish REAL change from erroneous past data and from new baseline PH codes.
- Components: areas may contain multiple components with attributes organized by themes (Physiography, Inland Water, Agriculture/Natural Vegetation, Forestry, etc.).
- Area Operations: Copy Area, Split Areas, Modify Area, Update Areas with attribute copying; margins (hedges/field margins) recorded where applicable.

## Points, Linear Features, and Events
- Points: include trees, standing water bodies, ponds, etc.; edited individually; each point must have at least one component.
- Woody Linear Features (WLFs): lines representing lines of trees, hedges, or straightened features; classify natural vs managed status.
- Lines: edited via Lines tab; events along lines have their own attributes and lengths; lines edited one at a time.
- Borders, margins, and buffers: record where applicable.

## Ponds and Inland Water
- Ponds: map in CS2007 Pond Mapping Recording Sheet; identify a survey pond per square for detailed condition assessment.
- Definition: standing water body from 25 m2 to 2 ha, typically water-filled for at least four months annually.
- Selection: survey pond chosen randomly from mapped ponds; verify preselected ponds and reselect if needed.
- Detailed pond attributes collected for the survey pond; other ponds mapped with basic attributes.

## Non-native Species and Other Considerations
- Maintains a list of non-native species to monitor within habitats for potential habitat qualification.
- Emphasizes consistent coding, thorough metadata, and robust national/subnational habitat statistics.

## General Rules and Habitat Descriptions
- BHs described for a wide range of habitat types (e.g., various woodlands, grasslands, heaths, wetlands, rivers, urban habitats, coastal/foreshore features, mosaics).
- Each BH/PH includes primary attributes, qualifiers, vegetation type, species lists, and percent-cover frameworks.

## Output, Reporting, and Metadata
- Supports reporting by BH and PH with time-series analysis to inform policy and biodiversity monitoring.
- Datasets should be stored with metadata, sourced-tracking, and made discoverable via data portals where applicable.

## End-of-Session and Support
- After editing, save the session to commit changes; End Session to discard changes.
- For issues, contact the CS Surveyor helpdesk and consult Latest News for methodology updates.

## Practical Data Handling Notes (from the Text)
- WLF Unnatural Shape: a structured data field set (height, canopy base height, species composition, management evidence, line of stumps, vertical gappiness, margins, staked trees, tree protectors) used to classify and describe linear woody features with coded categories.
- The document includes example coding schemes and figure references to standardize interpretation of WLF shapes and related attributes.
- Line editing, copy features, and advanced line manipulations (reshape, cut, shared nodes) are detailed to maintain topological integrity and data accuracy.
- Loops in linear features are flagged as data issues requiring a defined remediation workflow (mark as Deleted Feature, complete with valid reasons for change, then re-create the line).

## Historical Context (CS1990/CS2000)
- Describes evolving mapping practices prior to CS2007, including themes mapped and attribute coding approaches, to contextualize the CS2007 methodology and data lineage.