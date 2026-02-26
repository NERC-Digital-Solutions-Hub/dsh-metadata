# DATA HEADER INFORMATION for: Root_ramification_data_per_direct_measured_tree_voronoi_method.csv Please also see Manual_2_Belowground_Root_Survey, page 10.

## Purpose and scope
- Documents target tree root architecture by recording each coarse root (up to 1 cm diameter) branching for every target tree.
- Measurements are associated with the Voronoi method to attribute ramification to specific excavation Triangles (Voronoi) or to indicate a taproot (PV).
- Data originated under ESPA and P4GES; DOI provided for data provenance.
- Acknowledgement to Laboratoire des Radio Isotopes, Université d'Antananarivo required for products derived from these data.

## Data structure and key fields
- ZOI: Zone of Interest; categorical; units: ZOI2 (Andasibe), ZOI3 (Anjahamana).
- Site: Code tied to the collection site; Site information provided as text; Unit: (.).
- Local name: Vernacular/local name of the inventoried tree species; Text.
- DBH Class: Diameter at Breast Height class; categorical; Units: L (Large), M (Medium), S (Small).
- Code_target_tree: Unique code for each target tree; Text String.
- Number of ramification: Count of ramification emanating from the north; Numeric.
- DiH: Horizontal diameter beginning of each ramification; Numeric; Unit: cm.
- DiV: Vertical diameter beginning of each ramification; Numeric; Unit: cm.
- DfV: Vertical diameter ending of each ramification; Numeric; Unit: cm.
- DfH: Horizontal diameter ending of each ramification; Numeric; Unit: cm.
- DfM: Mean diameter ending of each ramification; Numeric; Unit: cm; DfM = (DfH + DfV) / 2.
- Total_weight: Weight of each ramification; Numeric; Unit: g.
- Total_length: Length of each ramification; Numeric; Unit: cm.
- Orientation: Indicates the direction or origin of ramification; Categorical; possible values: Vor (Voronoi triangle), PV (taproot), N, S, E, W; NA for not available (ramification not visible or root immovable).
- NA: Not available indicator for ramification direction; used when direction cannot be observed.

## Data context and interpretation
- Each ramification entry includes both physical measurements (diameters, length, weight) and spatial/orientation context (Vor, PV; cardinal directions).
- DfM provides a summary metric for ending diameters, enabling comparison across ramification units.
- The Voronoi-based classification ties ramification to specific excavation contexts, while PV identifies taproot contributions.

## Relevance for environmental monitoring and data reuse
- Provides standardized, per-tree root architecture metrics suitable for monitoring soil-plant interactions and root distribution patterns over time.
- Structured with explicit units and categorical encodings to facilitate quality assurance, comparability, and integration into monitoring portals.
- Designed for dataset aggregation and cross-dataset combination to enhance the value and accessibility of root morphology data.