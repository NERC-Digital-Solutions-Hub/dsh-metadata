# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Overview
  - Comprehensive guide for the CS2007 field mapping, documenting digital mapping of habitats and landscape features (polygons, lines, points) and collecting detailed attribute data across upland and lowland contexts.
  - Aims to standardise data collection, change detection, and attribute coding to enable cross-square comparability and data reuse.

- Data model and mapping units
  - Spatial components: Areas (polygons), Lines, Points; minimum mapping unit (MMU) for areas is 1/25 ha (400 m2) with exceptions.
  - Change handling: If habitat change occurs, a new polygon is created; otherwise, edits are made to attributes. Mosaic habitats are allowed when components are indistinct.
  - Attribute structure: Each polygon/component has primary and secondary habitat attributes with component-level percentages summing to 100%.

- Classification keys and habitat structure
  - Broad Habitats (BH) and Priority Habitats (PH) are reported at the polygon level, with additional component-level attributes.
  - Vegetation Key: assigns BH/PH based on vegetation composition; supports dominant habitat allocation and attribute decisions.
  - Woodland Types/Features Key: categorises woody vegetation (belt of trees, clump of trees, woodland/forest, line of trees, etc.) and captures species, canopy, DBH, and related attributes.
  - Enclosed vs unenclosed habitats: Enclosed lowland habitats edit polygons defined in 1998 CS; PHs nest within BHs. Unenclosed upland habitats integrate CS1990 data with CS2000 for finer vegetation detail and allow merging adjacent uniform vegetation polygons.

- PH integration and data sources
  - Post-survey GIS masks delineate PH ranges for countrywide extent reporting and estimation.
  - Non-native species are recorded from a predefined list.

- Mapping keys in practice
  - Vegetation Key: Uses flora composition to allocate BH/PH and capture primary/secondary attributes, with context rules for upland vs lowland and calcareous vs acidic environments.
  - Woodland Types/Features Key: Classifies woody vegetation into Belt of Trees, Clump of Trees, Wood/Forest, Scattered Trees, etc.; records species, canopy cover, DBH, and supplementary attributes (parkland, understorey, regeneration, buffers).

- Digital mapping system and workflow (CS Surveyor)
  - Platform: CS Surveyor extension embedded in ArcMap; login required; pre-configured data layers.
  - Editing workflows: Area Edits, Line Edits, Point Edits via Landscape Feature Editing toolbox; frequent saving; End Session saves; unsaved work discarded.
  - Area editing (6.a): Edit polygon attributes; assign BH/PH via vegetation key; assess 1998 BH accuracy; classify changes as REAL or ERROR; document visit status; allow creation of new PH baselines when needed.
  - Topology and component editing: Areas may contain multiple components; add/copy/delete components; update primary/secondary attributes per component.
  - Operations: Copy Area, Split Areas, Merge Areas (with mandatory Reason for Change), Modify Area (topology-aware), Update Areas (splits/merges consolidated into a single update).
  - General mapping rules: Continuous woodland ⇒ BH/PH; avoid MMU breaches (map as line if necessary); new polygons for primary attribute/habitat changes; record 2 plant species per polygon (up to 4) for habitat attribution.
  - Ponds: map all ponds; use CS2007 Pond Mapping Recording Sheet; designate a survey pond per square from preselected pond lists; field-based re‑selection allowed when new ponds are found.
  - Data capture guidance: Ponds include boundary definitions, pond condition, and drivers of change; pond data support square-to-square comparisons over time.

- Points and woody features (points)
  - Points store individual landscape elements (trees, standing water bodies, ponds, etc.) and support creation, movement, deletion, and copying of attributes; multiple points can share components; buffers can be recorded.
  - Woody features capture species, DBH, canopy cover, and buffer zones; veteran trees documented with detailed attributes (buffer, ivy cover, live canopy, dead wood, etc.) up to specified limits.

- Linear features and events (lines)
  - Linear features are narrow (<5 m wide) with minimum length 20 m; include fences, hedges, walls, woody lines, ditches, tracks, streams.
  - Events along lines carry attributes (type, length, status) and support copying/editing; margins and other features can be recorded.
  - Line editing: create new lines, split/merge events, adjust event lengths; shared boundary nodes are edited via specialized tools.

- Broad Habitats (BH) and habitat descriptions
  - BHs cover a wide range of landscape types; detailed attribute schemes span Agriculture/Natural Vegetation, Physiography, Structures, Boundaries, and more.
  - Examples of BH classifications include BH1 (Broadleaved Woodland), BH2 (Coniferous Woodland), BH4 (Arable/Horticultural), BH5–BH18 (grasslands, heaths, wetlands, urban, coastal), BH21–BH23 (various coastal and mosaic types), and mosaic BHs.
  - PH integration: PHs are nested within BHs; GIS masks enable accurate PH extent estimation and reporting.

- Pond details and condition assessment
  - Pond Mapping Recording Sheet captures per-pond data (area, maximum winter water level, water presence, reasons for pond loss/creation, drivers such as fishing, shooting, wildlife, etc.).
  - Survey ponds are selected from mapped ponds; preselected ponds may be used; re-selection is allowed if new ponds are found.
  - The approach supports cross-square comparison of pond condition over time.

- Special notes and guidance
  - Spatial accuracy is not the primary objective; emphasis is on faithful representation of habitat extents and changes.
  - Non-native species, buffer zones, orchards, and hedgerows have specific attribute rules to support ecological interpretation and policy relevance.
  - Edge cases (temporary ponds, ditches, urban features, mosaics) have dedicated guidance to ensure consistency across squares.

- Appendices, supports, and data governance
  - Appendices cover electricity of old field assessment formats, CS2000/CS1990 themes, veteran tree girth rules (Appendix 5), and squares with loops (Appendix 6) for data quality handling.
  - Additional resources include field assessment booklets (FABs), electronic copies, and references to field-handbooks for deeper interpretation.
  - Support: Helpdesk, wiki, and system updates available for field issues and methodology changes.

- Endnotes and practical access
  - The document is produced by NERC/CEH with guidance for field data collection and mapping workflows; updates and further information are available through the Countryside Survey program.