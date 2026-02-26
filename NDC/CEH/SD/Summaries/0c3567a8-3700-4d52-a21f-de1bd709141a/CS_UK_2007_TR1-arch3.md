# CS Technical Report No 1/07: Field Mapping Handbook v1.0

- Purpose and scope
  - Countryside Survey 2007 maps habitats and landscape features across 1 km squares using a GIS-based system, building on CS2000 with refined habitat attributes and introduction of Priority Habitats (PH) alongside Broad Habitats (BH).
  - Aims to report land cover change by BH/PH, map PHs, collect detailed data in upland/unenclosed habitats, and extend coverage to Wales while maintaining a consistent time-series structure.

- Data model and structure
  - Core data types: Areas (polygons), Lines (linear features), and Points (discrete features) forming a single landscape dataset.
  - Areas carry primary attributes (BH/PH) with components and secondary attributes; lines and points tie into the same dataset.
  - MMU (minimum mapping unit) for areas is 1/25 ha (400 m2); polygons below MMU are not mapped unless part of a larger boundary.
  - Components allow sub-units within an area; mosaics and percentage shares enable multiple habitat allocations within a single polygon.

- Mapping workflow and change management
  - Change status classifications for attributes: Real change (genuine habitat change since 1998), Error (correction of prior data), or New Baseline (new subdivision).
  - Lines, points, and areas are edited with robust change logging to support auditable time-series data.
  - Editing constraints:
    - Points and lines require editing at scales of 1:5000 or finer; areas have MMU constraints.
    - Lines support events, splits, merges, and vertex-level editing; shared nodes ensure topology consistency.
  - Change justification is mandatory for traceability of alterations.

- Keys for habitat allocation
  - Vegetation Key: Allocates BH/PH attributes from vegetation composition using detailed guidance on associating vegetation stands with BHs and PHs.
  - Key to Woodland Types/Features: Classifies woody vegetation by canopy form and extent (e.g., woodland/forest, belts, clumps, hedgerow trees) and supports mosaic allocations; provides decision rules for canopy cover, width, and geometry.
  - Application flow: First apply woodland keys to determine canopy >25% and BH/PH eligibility; otherwise refine allocation with the Vegetation Key.

- Broad Habitats (BH) and Priority Habitats (PH)
  - BHs cover major habitat types with primary attributes, usage notes, and species/cover guidance (e.g., BH1–BH19 categories such as Broadleaved Woodland, Coniferous Woodland, Arable, Grasslands, Wetlands, Rivers/Waters, Urban, etc.).
  - PHs are nested within BHs and mapped post-survey; PH extents may be masked by GIS to reflect native ranges.
  - Special handling notes:
    - Enclosed vs. unenclosed delineation affects detail level and data integration with earlier CS datasets.
    - Orchards are treated as an Agriculture/Natural Vegetation attribute; traditional orchards can be PHs.

- Ponds and standing water
  - Ponds are a central focus within Standing Open Waters and Canals; a pond mapping sheet records basic attributes for every pond in a square.
  - Field procedures:
    - One pond per square is selected for detailed condition assessment (water chemistry, vegetation, etc.).
    - Preselected ponds from CS2000 may be reused if valid; otherwise field selection occurs via randomization.
  - Boundary delineation uses winter water level boundaries and may consider vegetation fringe and hydrology; temporary ponds may be recorded if they typically hold water for ≥4 months.

- Data capture, attributes, and components
  - Areas: mandatory BH/PH assignment; attributes organized by themes (Inland Physiography, Agriculture/Natural Vegetation, Forestry, Structures); species records per polygon (2–4) with cover category bins (<10% to 95–100%).
  - Components: areas can be subdivided; each component records modal DBH, vegetation type, species, and cover where relevant.
  - Woodland features: components capture primary attributes (e.g., Belt of Scrub, Belt of Trees, Clump of Trees, Wooded features) plus supplementary attributes (fencing, grazing, regeneration, veteran trees, buffers).
  - Margins and orchards: margins mapped as standalone features; orchards have specific attribute handling (traditional vs. intensively managed).

- Digital mapping system and field procedures
  - CS Surveyor (ArcMap extension) is used to capture and edit Areas, Lines, and Points; strict session management and regular saving are required.
  - Editing constraints:
    - Points and Lines: editing scale ≤ 1:5000; Areas follow MMU rules.
    - Change reason codes and audit trails are mandatory for all edits.
  - Workflows:
    - Area editing: create, copy, split, merge, modify boundaries; update attributes per theme.
    - Component editing: add/copy/delete components; edit theme-specific attributes.
    - Line editing: manage events, copy events, split/merge lines, adjust geometry; handle shared nodes carefully to preserve topology.
    - Point editing: create/move/delete points; manage multiple components per point; scale-limited editing.
  - Pond procedures: use pond mapping sheets; select survey pond; follow pond boundary rules; record pond ID, area, water presence, and creation/loss reasons.

- Quality, consistency, and reporting
  - Emphasizes consistent classification, detailed attribute capture, and rigorous change logging to support time-series analyses and monitoring programs.
  - Data governance is built on standardized vegetation and woodland keys and established habitat definitions to ensure comparability across squares and years.

- Appendices and supporting notes
  - Field Assessment Booklets (FABs) and CS2000/CS1990 codes and documentation.
  - Pond recording sheets and random-number tables for pond selection, plus guidance on veteran trees and other specialized observations.
  - Additional guidance on pulse/disturbance vegetation, set-aside management, margins, and non-native species recording to maintain cross-cycle comparability.

- Practical considerations for monitoring frameworks
  - The handbook provides a structured, auditable workflow suitable for long-term monitoring programs.
  - It supports time-series comparability through standardized keys, explicit change codes, and consistent data governance practices.
  - It also highlights data-related challenges relevant to monitoring frameworks (data gaps, data access, data silos, metadata quality, data transformation needs, and data-sharing constraints) and outlines mechanisms to address them (stakeholder consultation, data provenance, openness standards, and governance processes).