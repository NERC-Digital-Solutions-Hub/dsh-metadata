# Final Report for LCM2007 - the new UK land cover map

## Overview
- Presents the first continuous parcel-based UK land cover map (LCM2007) with a suite of raster and vector products at multiple resolutions.
- Aims to support environmental monitoring, policy evaluation, change detection, and habitat planning by providing a consistent, ground-truthed framework across the UK.
- Built to facilitate integration with other national and European datasets (e.g., Countryside Survey, Corine).

## Data sources and spatial framework
- Primary data sources: multi-date satellite imagery (Landsat-5 TM/ETM+, SPOT-4/5, LISS-III, AWIFS), plus supplemental imagery for gaps.
- National coverage achieved via 34 multi-date composites (summer and winter) and several single-date images.
- Ground reference data from CEH (2006–2008) and external validation datasets (e.g., Countryside Survey 2007).
- Spatial framework anchored to detailed national cartography (Ordnance Survey MasterMap and LPS), harmonised across Great Britain and Northern Ireland.
- Framework supports UK-wide MMU of 0.5 ha and minimum feature width of 20 m, enabling consistent spatial comparisons and potential change detection.

## Image processing, segmentation, and classification
- Pre-processing includes cloud masking, atmospheric and topographic correction, and rigorous geo-registration.
- Image segmentation creates homogeneous spectral regions; segments are linked with OSMM parcels and agricultural boundaries to form a robust UK segmentation framework.
- Knowledge-based enhancements (KBEs) apply contextual rules (urban/coastal boundaries, soils, terrain) to resolve spectral confusion and improve classification plausibility.
- Parcel-based supervised maximum likelihood classification using 37 composites and 21 single-date images; training areas derived from ground references; probabilities for top five spectral classes stored (ProbList).
- Post-classification manual edits for rare or problematic areas; hole-filling where data were missing.
- KBEs help differentiate grassland types, montane vs coastal classes, and complex mosaics (e.g., Fen, Marsh and Swamp).

## Knowledge-based enhancements and thematic resolution
- KBEs address spectral confusion (e.g., arable vs urban; various grassland types) using ancillary data (urban boundaries, soils, terrain, coastlines).
- Thematic resolution extends beyond spectral signal; Broad Habitat associations map ecological definitions (e.g., grassland types linked to soil/altitude).
- Ability to reverse KBEs to retrieve original spectral classifications when needed.
- Outputs include both detailed 23 LCM2007 classes and 17 Broad Habitats, with accompanying metadata for traceability.

## Data products, metadata, and access
- Primary data products:
  - 25 m raster: 23 LCM2007 classes.
  - Vector product: polygons with 10 processing-stage attributes (e.g., Construct, ProbList, KBE history).
  - 1 km raster summaries (percent cover or dominant class for each of the 23 classes and 10 aggregates).
- Rich metadata for traceability and decision auditing; KBEs and classification decisions documented.
- Access: 1 km rasters via CEH Information Gateway; full vector and 25 m rasters available on request (licensing may apply).

## Quality assurance, validation, and comparisons
- Ground-truth validation: about 9127 CEH ground reference points; overall accuracy roughly 83% across LCM2007 classes, with variable class-level accuracy.
- Countryside Survey (CS) comparisons show varying agreement by Broad Habitat; grassland areas often problematic due to one-to-many relationships and boundary delineations.
- Fen, Marsh and Swamp estimates show large discrepancies due to mosaic and small patch sizes; many Fen areas in CS map to Rough Grassland or Acid/Neutral Grasslands in LCM2007.
- Differences partly explained by temporal imagery range, spectral variability in Arable and Horticulture, and boundary feature treatment (CS includes boundaries that LCMMMU may not map).
- Spatial structure differences (MMU, segmentation) complicate direct change detection between LCM2007 and earlier maps.

## Change mapping and monitoring implications
- Change detection between LCM2007 and previous maps is challenging due to different spatial and thematic structures.
- Reliable change assessment may require:
  - Aggregation to common, stable classes or harmonised spatial units.
  - Focusing on consistently mapped classes and using trajectory-based statistical approaches.
  - Reorganising earlier maps into a common spatial framework based on real-world land-use units.

## Applications for environmental monitoring and policy
- Provides a robust, scalable evidence base for habitat monitoring, biodiversity assessments, ecosystem services planning, and landscape management.
- Enables cross-border comparability and integration with other datasets for policy evaluation (e.g., biodiversity targets, land-use planning, catchment management).
- Acts as a contextual base map for higher-resolution habitat mapping and network/connectivity analyses.
- Supports policy-relevant indicators and monitoring programs while acknowledging limitations for certain habitat classes and mosaic landscapes.

## Practical implications for Analysts Monitoring the Environment
- Use LCM2007 as a baseline UK land cover reference across 1 km (coarse-scale modelling) and 25 m (detailed analyses) products.
- Leverage the vector parcel metadata (KBEs, ProbList) to assess classification uncertainty and validate outputs against imagery in specific locations.
- Integrate LCM2007 with field surveys (CS) and other datasets (soils, topography, urban boundaries) to improve interpretation in complex habitats (grasslands, fen, montane, coastal mosaics).
- Exercise caution when interpreting changes in habitats with mosaic definitions or boundary-driven classifications; employ aggregation or trajectory analysis for robust monitoring.

## Appendix and validation notes (highlights)
- Broad Habitat Association rules (BHAs) provide working correspondences between LCM2007 and Countryside Survey classifications to aid cross-walks.
- Validation methodology emphasises fit-for-purpose accuracy rather than absolute pixel-level perfection; encourages local validation using parcel-level metadata.
- Data accessibility and licensing details provided for researchers and policy teams needing full vector/25 m data.