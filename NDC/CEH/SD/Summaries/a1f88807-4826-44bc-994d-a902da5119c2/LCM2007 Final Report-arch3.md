# Final Report for LCM2007 - the new UK land cover map

## Overview
- First continuous parcel-based UK land cover map (LCM2007) with vector parcels and derived 25 m and 1 km raster products.
- 23 land cover classes mapped to Broad Habitats; Minimum Mapping Unit of 0.5 ha; supports habitat monitoring, biodiversity policy, and landscape planning.
- Spatial framework built from detailed national cartography (OS MasterMap and LPS Large-Scale Vector); segmentation and knowledge-based enhancements (KBEs) used to refine classifications.
- Output includes full UK-wide vector, 25 m rasters, and 1 km aggregated products; data governance and provenance are documented.

## Relevance for Monitoring Frameworks
- Provides a robust, reusable base for habitat monitoring and policy scrutiny across biodiversity, ecosystem services, and landscape planning.
- Enables spatially explicit monitoring and potential change detection when integrated with other datasets (e.g., CS, soil, climate).
- Establishes a common spatial framework that facilitates cross-country comparisons and policy evaluation at multiple scales.

## Data and Methodology (high-level)
- Spatial framework: parcels derived from OS MasterMap (GB) and LPS Large-scale Vector (NI); 9 UK-wide chunks assembled for seamless UK coverage.
- Data sources: multi-temporal satellite imagery (Landsat TM, SPOT, LISS-III; AWIFS as backup); 6-band, 2-date composites to maximize class separation.
- Processing: cloud/mask, atmospheric correction, geometric correction (RMSE < 0.3 px), segmentation into image-based segments linked to OS boundaries; parcel-based supervised maximum likelihood classification with training data.
- Enhancements: seven automated KBEs using contextual data (urban proximity, soils, terrain) to refine grassland and Montane habitat classifications; KBEs and their sequence are recorded in vector attributes.
- Validation: ground reference validation with 9127 points; overall accuracy around 83% across LCM2007 classes; class-specific accuracy varies, with better performance for some grassland and woodland categories when analyzed via Broad Habitat Association (BHA).

## Data Products and Access
- Vector product: polygons with attributes including area, source images, Broad Habitat (BH) and BHSub, KBE history, ProbList, and CorePixels.
- 25 m raster: 23 LCM2007 classes.
- 1 km raster: two products per pixel — (A) percentage cover by each LCM2007 class, (B) dominant class per pixel.
- Access: 1 km rasters via CEH Information Gateway; vector and 25 m rasters available on request under licence from CEH (licence fees may apply).

## Validation, Comparisons with Countryside Survey
- UK-wide comparisons with Countryside Survey 2007 show varying agreement by Broad Habitat.
- Grassland mappings are challenging due to one-to-many correspondences between grassland observed in CS and multiple BH classes; BHA rules were developed to improve interpretability.
- Arable and Horticulture: CS UK estimate around 46,574 km2; LCM2007 approx. 63,005 km2; differences arise from classification definitions, spectral variability, and inclusion of boundary features in LCM2007.
- Fen, Marsh and Swamp: CS estimates differ by order of magnitude from LCM2007 due to complex mosaics and small patch sizes; improvements may come from additional data and KBEs.
- Thematic areas such as Montane Habitats, coastal habitats, and water classes show regional and methodological variations; CS patch size and MMU impact comparisons.

## Key Challenges and Limitations for Monitoring
- Data gaps and access barriers; silos and metadata gaps hinder data integration.
- Public sharing requirements for underlying data can constrain reuse.
- Change mapping is complex due to differences in spatial structures and time-range of input imagery; differentiating real change from methodological differences remains difficult.
- Grassland and Fen areas present notable uncertainty; spectral confusion and one-to-many mappings persist despite KBEs.
- Boundary and linear features often below MMU in CS, leading to differences in field delineations versus LCM2007 polygons.
- Comprehensive data governance and detailed provenance are essential for longitudinal monitoring.

## Data Governance, Metadata
- KBEs and their processing history are stored with each parcel; this enables traceability and independent validation.
- Metadata and provenance support traceability of polygon-level decisions and the sequence of KBEs applied.
- Licencing arrangements for vector and 25 m rasters, with clear access pathways and potential fees.

## Policy Implications and Recommendations
- LCM2007 offers a robust platform for policy evaluation, habitat connectivity analysis, and Natura-type reporting at UK scales.
- The BH/BHA framework provides a structured way to interpret grassland and mosaic habitats and to align satellite-derived classes with field-based surveys.
- For monitoring programs, integrate LCM2007 with higher-resolution, ground-truth, and ecosystem-service data to strengthen evidence bases.
- Ongoing QA, refinement of KBEs, and preservation of a common spatial framework will enhance comparability over time and support change detection.
- Consider harmonising spatial structures across map versions to improve long-term monitoring continuity.

## Similar and Dissimilar Area Estimates (4.3.2)
- Similar area estimates (UK-wide, within CS 95% confidence bounds) for: Broadleaved woodland, Acid Grassland, Inland Rock.
- Dissimilar area estimates (beyond CS 95% bounds) for: Arable and Horticulture, Improved Grassland, Neutral Grassland, Dwarf Shrub Heath, Bog, Montane Habitats, coastal habitats.
- Notable explanatory factors for differences:
  - Classification definitions and what is included in each class.
  - Spectral confusion and temporal mismatch (LCM images from multiple years).
  - Inclusion of Boundary and Linear Features in LCM2007 that CS maps separately.
  - Grassland typologies and one-to-many mappings affecting comparability.
  - Fen mosaic complexity and small patch sizes affecting detectability and QA.
- The report discusses how temporary grassland, uncropped land, and field-structure differences contribute to observed discrepancies; it also notes the potential alignment of CS and LCM2007 via broader habitat associations.

## Conclusion
- LCM2007 provides a comprehensive, parcel-based baseline for UK land cover with multiple data products and a clear framework for monitoring policy-relevant habitats.
- While offering strong capabilities for evaluation and spatial analysis, it also highlights ongoing challenges in grassland, fen, montane, and boundary-feature mapping that require careful interpretation and supplementary data.
- The integrated approach, with KBEs and a consistent spatial framework, supports more robust monitoring and informed decision-making, alongside clear guidelines for data governance and future improvements.