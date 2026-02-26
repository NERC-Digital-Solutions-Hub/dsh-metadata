# Final Report for LCM2007 - the new UK land cover map

- An end-to-end, parcel-based land cover mapping project for the UK, integrating diverse data sources to produce a continuous vector framework and supporting raster products at multiple resolutions.
- Builds on a Broad Habitats framework to support habitat monitoring, biodiversity policy, ecosystem service assessment, and landscape planning.

## Data sources and spatial framework

- Primary data inputs:
  - Satellite imagery (Landsat TM/ETM+, SPOT-4/5, AWIFS; LISS-3 for higher detail)
  - Ground reference and validation data (CS 2007, CEH field points)
  - External spatial datasets (Ordnance Survey MasterMap, NI LPS, agricultural boundaries, urban boundaries, soils, elevation)
- Spatial framework:
  - Great Britain: OS MasterMap-based framework generalised to MMU of 0.5 ha and MFW 20 m
  - Northern Ireland: NI LPS framework integrated with image segments
  - Nine UK-wide chunks to manage processing and ensure seamless vector output
- Image processing:
  - Multi-date summer/winter composites, atmospheric and topographic corrections, cloud masking, and precise geo-registration
  - Image segmentation producing a segment-based vector framework

## Data processing and classification workflow

- Pre-processing and segmentation
  - Cloud/shadow masking, atmospheric correction, topographic correction
  - 60 composite images segmented to form a segment-based framework
- Classification
  - Parcel-based supervised maximum likelihood classification
  - 23 LCM2007 land cover classes mapped to 17 Broad Habitats
  - Training data derived from ground references with iterative cross-scene checks
- Knowledge-based enhancements (KBE)
  - Seven KBEs applied to resolve spectral confusion and improve thematic resolution
  - KBEs use contextual cues (urban boundaries, coastal proximity, terrain, soils, water) and soils data
  - KBEs preserve original spectral classification via ProbList for user reversal if needed
- Data products
  - Vector data: polygons with 10 processing attributes, including Construct, ProbList, and KBE history
  - Raster data: 25 m resolution with 23 classes; 1 km data products with two summaries (percent cover and dominant class)
  - MMU: minimum mapping unit 0.5 ha; metadata tracks processing steps per polygon

## Validation, quality assurance, and caveats

- Validation
  - Ground reference validation: 9,127 points; overall accuracy around 83% for LCM2007 classes
  - Countryside Survey (CS) 2007 comparison shows varying agreement by Broad Habitat; grassland areas are particularly problematic
- Key challenges and sources of discrepancy
  - Grassland: one-to-many relationships between observed land cover and Broad Habitats; Broad Habitat Association rules added to improve interpretability
  - Arable and Horticulture: spectral variability and inclusion of boundaries/linear features affect area estimates; temporary grass and uncropped land contribute to discrepancies
  - Boundary and Linear Features: CS maps many features below the LCM MMU; LCM incorporates many into field polygons, increasing field sizes in some classes
  - Fen, Marsh and Swamp: CS vs LCM2007 show large differences due to mixed land cover mosaics and small patch sizes; many CS fen areas reclassified as Rough Grassland or Acid Grassland in LCM2007
  - Montane, Coastal, and Inland Water classes: representation and spatial structure differences affect comparisons
- Change mapping and interpretation
  - Change detection between LCM1990, LCM2000, and LCM2007 is complex due to differing spatial structures; robust change assessment requires aggregated classes and cautious interpretation
  - General conclusion: align older maps to a common, real-world spatial framework to improve change detection

## Data access, licensing, and documentation

- Access
  - 1 km raster data: CEH Information Gateway
  - Full vector and 25 m raster data: on request under licence from CEH (fees may apply)
- Documentation and metadata
  - Extensive metadata accompanying vector and raster products
  - Appendix and glossary sections detailing Broad Habitats, data terms, and validation approaches

## Applications, impact, and cross-dataset context

- Applications
  - Habitat monitoring, biodiversity assessments, ecosystem service evaluation, landscape planning, and catchment management
  - Cross-sector policy support and environmental monitoring at national and regional scales
- Cross-dataset context
  - LCM2007 complements Countryside Survey data, offering coast-to-coast coverage and integration-ready framework
  - European links: LCM2007 data underpin Corine Land Cover mapping in the UK and support pan-European environmental assessment
- Knowledge transfer and impact
  - The parcel-based approach with accompanying metadata (KBE history, ProbList) enables end users to audit, validate, and adapt classifications to specific local needs

## Summary takeaways for data support

- LCM2007 demonstrates a robust end-to-end data pipeline: multi-source data fusion, cartographic-based spatial framework, segment/parcel-level classification, and knowledge-based refinement to produce high-resolution national land cover products.
- Strong QA and cross-dataset validation (including Countryside Survey) underpin data reliability, with explicit caveats around grassland, fen, and boundary feature treatments.
- Data are accessible via CEH platforms, enabling self-serve exploration and downstream data product development for policy, planning, and research, with clear licensing and metadata to support reuse.