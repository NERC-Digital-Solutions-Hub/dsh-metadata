# Final Report for LCM2007 - the new UK land cover map

- UK-scale, policy-relevant land cover map designed to support environmental health monitoring, biodiversity assessment, ecosystem services, landscape planning, and catchment management.
- Provides both detailed thematic mapping (23 land cover classes linked to Broad Habitats) and aggregated outputs (1 km summaries), enabling multi-tiered monitoring and evidence-based policy decisions.
- Emphasizes robust, auditable data supply chains with metadata, openness where feasible, and governance around data use.

## Key outputs and data products

- Land cover classes: 23 LCM2007 classes mapped to Broad Habitats plus 10 aggregated classes.
- Spatial framework: continuous UK vector coverage assembled from OS MasterMap-derived parcels and related boundaries; MMU of 0.5 ha; minimum feature width of 20 m.
- Data products:
  - Full vector product with 10 processing-related attributes (e.g., Construct, ProbList, KBE).
  - Main 25 m raster product (23 classes).
  - 1 km raster products: percentage cover and dominant class for each 1 km square, for both 23 classes and 10 aggregate classes.
- UK-wide consistency achieved through chunk-based assembly to ensure continuous vector coverage.
- Rich parcel-level metadata documents processing history and knowledge-based enhancements (KBEs).

## Data sources and production approach

- Satellite imagery and composites (3.1):
  - Primary sources: Landsat-TM5, IRS-LISS3, SPOT-4/5; AWIFS as backup.
  - Multitemporal summer+winter composites to improve class separation; ~91% of UK mapped from composites in 2007.
- Additional spatial data (3.2):
  - Ground reference points (CEH) for training/validation.
  - Countryside Survey Broad Habitat data (2007) for cross-validation.
  - External data: national cartography, DEM, soils, urban boundaries, agricultural boundaries for refining delineation.
- Spatial frameworks (3.3–3.4):
  - GB: OS MasterMap-based framework, integrated with agricultural boundaries and image segments; generalised to MMU constraints.
  - Northern Ireland: LPS vector data converted to polygons and integrated with image segments.
- Image processing and segmentation (3.5):
  - Pre-processing includes cloud masking, atmospheric/topographic correction, and 6-band 2-date composites.
  - Segment-based vector framework formed by combining segmentation with OSMM parcels and agricultural boundaries.
- Image classification (3.6):
  - Parcel-based supervised maximum likelihood classification using ground-reference training data.
  - Iterative refinement with multi-date composites to reduce spectral confusion; manual edits and hole-filling for rare or missing classes.
- Knowledge-based enhancements (KBEs) (3.7):
  - Seven automated rules using context, terrain, soils, coastal proximity, and urban boundaries to refine land cover classifications.
  - KBEs address spectral confusions and improve thematic resolution; rules documented in vector attributes and can be overridden by user needs.
- Assembly and QA (3.8–3.9):
  - Continuous UK coverage via priority merging across overlaps.
  - Ground reference validation: overall accuracy ~83% across 9127 points; class-level accuracy varies (e.g., Bog producer ~93%, user ~39%; Improved Grassland producer ~89%, user ~83%).

## Data access, metadata and governance

- Access:
  - 1 km raster outputs via CEH Information Gateway.
  - Full vector product and 25 m raster available on license by request from CEH.
- Metadata and provenance:
  - Comprehensive metadata documenting processing steps for each polygon to ensure transparency and reproducibility.
- Data governance:
  - Clear licensing and data provenance to support reuse in policy monitoring contexts.

## Change mapping and temporal comparisons

- Change mapping is complex due to:
  - Differing base maps and spatial structures across LCM1990, LCM2000, and LCM2007.
  - Classification errors (typical ~20%) complicating true-change detection.
  - No universally robust method to separate real land cover change from structural differences yet.
- Recommendation: use multi-temporal analyses with careful error budgeting; consider aggregating to common or KBEs-informed classes, and acknowledge structural differences when interpreting change.

## Validation, accuracy, and comparison with Countryside Survey

- Overall accuracy: ~83% (9127 ground-reference polygons); class-level performance varies:
  - Bog: producer ~93%; user ~39% due to spectral confusion with adjacent classes.
  - Improved Grassland: producer ~89%, user ~83%.
  - Neutral Grassland: relatively low correspondence due to spectral similarity with other grasslands.
  - Montane Habitats: generally well captured; coastal and montane habitats more challenging.
- Comparisons with Countryside Survey (CS) 2007:
  - CS vs LCM2007: 62% Broad Habitat correspondence; 67% aggregate; 76% BH-level correspondence.
  - Grassland classes show notable disagreements due to differences in definitions and patch structure; spectral confusion and MMU differences contribute to discrepancies.
  - Fen, Marsh and Swamp estimates vary by order of magnitude due to mosaic nature of fen; much of CS fen may be mapped as rough grassland or acid grassland in LCM2007.
- Implications: while there is policy-relevant alignment for some classes (e.g., arable land), broader habitat extents show variability, underscoring the need for careful validation and cross-walking (BHA) rules.

## Practical implications for monitoring frameworks

- LCM2007 delivers a robust, UK-wide land cover framework suitable for policy monitoring, habitat assessment, and ecosystem-service analysis with:
  - Transparent metadata, data lineage, and processing notes enabling reproducibility.
  - Multi-scale outputs (25 m vector, 25 m raster, 1 km raster) to support diverse monitoring needs.
  - A structured data-integration approach combining cartography, soils, elevation, and urban boundaries with knowledge-based enhancements.
- Limitations to acknowledge:
  - Uncertainties in upland and semi-natural habitats.
  - Challenges differentiating certain grassland types and peatlands from spectral data alone.
  - Change detection requires careful handling of classification error and structural differences between datasets.
- Monitoring guidance:
  - Use 1 km outputs for broad policy analyses; employ 25 m vector and 1 km class outputs for habitat connectivity, biodiversity assessments, and landscape planning.
  - Calibrate and validate regionally using field surveys or CS-type data, mindful of habitat-definition differences and mapping units.
  - When assessing change, apply multi-temporal analyses with error budgets and leverage KBEs and soil/terrain context for interpretation.

## Summary of recommendations for monitoring practice

- Use LCM2007 as a baseline UK-wide land cover reference with explicit documentation of uncertainties and KBEs.
- Deploy 1 km aggregate outputs for broad policy analyses; use 25 m vector and 1 km class outputs for habitat connectivity, biodiversity assessments, and landscape planning.
- Combine LCM2007 with field surveys and CS-type data for regional calibration/validation, acknowledging potential habitat-definition discrepancies.
- For change detection, perform multi-temporal analyses with rigorous error budgeting; interpret potential changes in light of KBEs and soil/terrain context.
- Ensure data governance and metadata accessibility to support policy monitoring, decision-making, and reuse.

## Additional context and accessibility

- LCM2007 data are intended to integrate with related European data (e.g., Corine) and other national datasets, strengthening pan-European environmental assessment.
- The approach reflects a shift toward using a common, real-world spatial framework to improve future monitoring efficiency and change detection consistency.