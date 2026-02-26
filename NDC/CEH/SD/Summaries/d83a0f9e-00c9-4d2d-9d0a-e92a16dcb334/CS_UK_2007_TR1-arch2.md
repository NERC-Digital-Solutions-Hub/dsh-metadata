# CS Technical Report No 1/07: Field Mapping Handbook v1.0

## Aim and Scope
- Establishes a geographically comprehensive, digital field-mapping approach for Countryside Survey 2007 (CS2007) to report land cover change and habitat extent at 1 km square resolution.
- Documents methods to map Broad Habitats (BH) and Priority Habitats (PH) including upland unenclosed and Wales-specific areas, enabling country- and UK-level trend analyses.
- Emphasises time-series data, quality assurance, standardized outputs (reports, maps, charts), and dataset storage/upload to portals; records genuine ecological change and corrections to previous mappings; supports UK biodiversity and policy planning.

## Data Model and Classification
- Two primary keys for habitat allocation:
  - Vegetation Key (BH/PH assignment based on plant composition and habitat attributes).
  - Key to Woodland Types/Features (woody vegetation structures and BH/PH implications).
- Habitat structure:
  - BH encompasses a broad typology (BH1–BH23, including Mosaic) with nested PHs inside BHs.
  - Enclosed vs unenclosed habitats have tailored mapping detail.
- PHs are mapped within the BH framework; GIS masks constrain upland/lowland extents for accurate area estimates.
- Minimum mapping unit (MMU) is 1/25 hectare; mosaic polygons allow multiple BH/PH components with percentage area splits totaling 100%.

## Data Collection Platform and Workflow
- CS Surveyor: an ArcMap extension for data capture, editing, and change assessment.
- Requires compulsory change recording against mapped habitats and features; supports corrections to earlier allocations; in-field fault logging; methodology updates published as Latest News.

## Mapping Scope and Change Detection
- Focuses on polygon-level changes in land cover and landscape features.
- Change statuses include REAL change, ERROR (correction), and NEW BASELINE PH changes.
- For unenclosed habitats, integrates CS1990 data with CS2000 data to improve vegetation-type detail and PH identification.
- For enclosed habitats, uses 1998 data to guide current BH/PH attribution, with potential PH baseline updates.

## Habitats, Woodland, and Feature Descriptions
- Broad Habitats (BH): high-level categories such as BH1 Broadleaved Woodland, BH2 Coniferous Woodland, BH4 Arable/Horticultural, BH5–BH23 (e.g., various grasslands, wetlands, urban, sea, mosaic).
- Priority Habitats (PH): nested within BHs; require post-survey GIS masks for extent estimation.
- Woodland types/features (BH/PH components): belts, lines, clumps, scattered trees/shrub, woodland/forest; components capture species, cover, DBH, age structure, regeneration, and management history (fencing, grazing, windthrow, etc.); notes on beech, oak, conifer conversions, and orchard interpretations.

## Vegetation Key and Allocation Rules
- Vegetation Key assigns primary and secondary BH/PH attributes based on species composition and habitat characteristics.
- Every polygon must be allocated to a BH or PH, including urban or sparsely vegetated areas; guidance emphasizes practical interpretation and cross-referencing to NVC communities for major BHs.

## Using the Digital Mapping System (CS Surveyor)
- Embedded in ArcMap; login via CS Surveyor extension; pre-set data frame with layers and symbology.
- Editing workflow:
  - Areas (polygons), Lines (linear features), Points (point features).
  - Regular saves; edits may modify area shapes but must preserve habitat accuracy.
  - Bug-reporting channels provided; in-field changes are reflected in outputs.

## Editing Areas: Attributes and Change
- Polygon-level attributes: area, BH/PH designation, accuracy of BH, reason for change (Error, Real Change, New Baseline, etc.).
- Change determination based on whether 1998 allocations apply, whether new allocations reflect real change, or whether corrections are needed.
- Component-level attributes allow multiple components within a polygon to describe mosaics.

## Copy, Split, Merge, Update, and Modify
- Copy Area: propagate attributes from a source to targets.
- Split Areas: digitize new boundary; enforce MMU; assign attributes to resulting parts.
- Merge Areas: combine polygons with identical attributes; require valid Reason for Change.
- Modify Area: adjust boundaries/topology; ensure topological consistency.
- Update Areas: create new landscape areas by splitting/merging; may use copied shapes or external data (e.g., OS MasterMap).

## Points, Linear Features, and Woody Linear Features (WLFs)
- Points: edit individually; multiple components allowed; veteran trees recorded (up to 10 per square, max 2 per species).
- Woody Linear Features (WLFs): hedges, belts, lines of trees, natural vs managed shapes.
  - Attributes include height categories, base canopy height, species composition, evidence of management, line of stumps, vertical gappiness, margins, staked trees, and tree protectors.
  - If base height > 2 m, check that components or trees are not in unnatural shapes.
  - Visual exemplars illustrate WLF shapes and management signs.

## Ponds and Inland Water Features
- Ponds feature: identify all ponds per square; record basic attributes on a Pond Mapping Recording Sheet; select a survey pond per square via randomization if multiple ponds exist.
- Boundary delineation guided by winter water level and fringe vegetation; ponds may be temporary or permanent and natural or man-made.
- CS2007 includes detailed pond attributes and survey protocols; central to freshwater survey components.

## Data Quality, Access, and Value
- Emphasises data verification, quality assurance, cleaning, and transformation prior to outputs.
- Promotes combining CS2007 data with other datasets to increase value and enable broader analyses.
- Supports storage and sharing through portals to enhance policy relevance and environmental monitoring capabilities.

## Practical Guidance for Analysts
- Expect standardized habitat definitions and consistent attribute logging.
- Rigorous change-capture supports longitudinal assessments.
- Detailed rules for polygon creation, mosaic classification, and documenting uncertainties or boundary complexities.
- System designed to support broad monitoring and policy performance evaluation at national/UK scales.

## Context with CS2000 and CS1990 Appendices (Overview)
- References to older field assessment practices (CS1990/CS2000) and how themes, coding, and data forms evolved.
- CS1990 themes include Agriculture/Natural vegetation, Forestry, Boundaries, Physiography; BH mapping introduced later.
- Appendices provide coding schemes, universal codes, and historical datasets for cross-referencing and data interoperability.

## Endnotes and Access
- Copyright and usage terms; NERC as copyright holder with guidelines for reproduction.
- Contact details for the Countryside Survey project; funding by government bodies led by NERC and Defra.
- Online resources and project office contact for further information.