# Final Report for LCM2007 - the new UK land cover map

## Overview
- First continuous parcel-based land cover map for the UK, covering Great Britain and Northern Ireland.
- 23 LCM2007 classes mapped to 17 Broad Habitats; minimum mapping unit 0.5 ha.
- Spatial structure derived from detailed national cartography (OS MasterMap and LPS Large-scale Vector) to enable integration with other national datasets.
- Outputs include a high-resolution vector product and raster products at 25 m and 1 km scales.
- Aims to support biodiversity policy, habitat monitoring, change detection, and landscape planning across the UK.

## data sources and spatial framework
- Data sources:
  - Multi-temporal satellite imagery: Landsat TM/ETM+, SPOT-4/5, IRS LISS-III; 73 images processed; 34 multi-date composites; 91% UK mapped from composites.
  - External data: ground reference points, Countryside Survey Broad Habitats for validation, elevation (NEXTMap Britain), soils, urban boundaries, and agricultural boundaries.
- Spatial frameworks:
  - Great Britain: OS MasterMap topography with integrated agricultural boundaries and image segments for refined parcel delineation.
  - Northern Ireland: LPS Large-scale Vector framework; agricultural boundaries not integrated in NI framework.
- Generalisation and fragmentation:
  - OSMM data generalised to MMU 0.5 ha; segmentation integrates cartographic boundaries to improve delineation and change detection.
  - UK-wide coverage assembled into a continuous vector product across production chunks with a priority classification system.

## processing pipeline and knowledge-based enhancements
- Image processing:
  - Pre-processing: cloud/shadow masking, atmospheric correction, geo-registration (high accuracy), topographic correction.
  - Segmentation and raster-to-vector: 60 composite inputs emphasizing winter NIR, summer red, and MIR bands; parcel-based classification.
- Classification:
  - Parcel-based supervised classification (maximum likelihood) into Broad Habitat-based classes; training data from ground references; iterative refinement and reclassification.
  - Manual edits for rare/ambiguous cases; small holes filled with auxiliary data (e.g., Landsat-7 ETM+).
- Knowledge-based enhancements (KBEs):
  - Seven automated rules applied post-classification to resolve spectral confusion using contextual data (urban context, terrain, soils, coastal proximity, etc.).
  - Examples include altitude-based adjustments (montane), soil-type rules for grasslands, urban boundary considerations, coastal and water context rules.
  - KBEs affect ~20% of parcels; changes are traceable via vector attributes to allow reversion if needed.
- Outputs and traceability:
  - Vector product with 10 processing attributes, including Construct, ProbList, KBE history.
  - 25 m raster with 23 LCM2007 classes; 1 km raster products (percentage cover and dominant class across 23 classes).

## data products, access and licensing
- Core products:
  - Vector: parcel polygons with metadata on processing history and KBE applications.
  - Raster: 25 m resolution, 23 LCM2007 classes.
  - 1 km raster: two summaries per location (percentage cover and dominant class for 23 LCM2007 classes and 10 aggregates).
- Access and licensing:
  - 1 km raster data available via the CEH Information Gateway.
  - Full vector and 25 m raster data available on request under licence; fees may apply for some users/applications.

## quality assurance, validation and comparison with Countryside Survey
- Validation:
  - 9,127 ground-reference polygons (2006–2008); overall accuracy ~83%.
  - Class-level accuracy varies (e.g., Bog ~93% producer; Improved Grassland ~83% user, ~89% producer).
- Countryside Survey (CS) comparison:
  - Broad Habitat (BH) level: GB correspondence ~62%; BH Association level correspondence ~76%.
  - Grassland and upland areas show notable divergences due to spectral variability and classification of grassland types.
  - Differences attributed to: spatial structure and MMU, mosaic classifications, and context-based interpretations.
  - Key issues:
    - Arable and Horticulture: LCM2007 tends to overestimate compared with CS upper limit; differences partially due to inclusion of boundaries/linear features and temporal multi-year imagery affecting crop status.
    - Improved Grassland vs Neutral Grassland: discrepancies largely due to how each product classifies species composition and soil data limitations.
    - Fen, Marsh and Swamp: CS and LCM2007 differ by an order of magnitude due to mosaic nature and small patch sizes; many CS “Fen” areas map to Rough Grassland or Acid Grassland in LCM2007.
- UK-wide vs country-level patterns:
  - England shows highest proportion of intensive land use; Scotland has more Coniferous Woodland and upland habitats; NI/Wales show intermediate patterns.
  - LCM2000 vs LCM2007 differences partly reflect spatial framework changes; direct area comparisons require careful interpretation.

## applications, implications and strategy for data leaders
- Applications:
  - Provides a robust, coast-to-coast UK land cover framework for biodiversity assessments, habitat monitoring, ecosystem services, landscape planning, habitat connectivity, and catchment management.
  - Serves as a contextual base for higher-resolution habitat mapping and for policy evaluation (e.g., Natura targets, woodland expansion planning).
  - Facilitates change detection through a stable, generalised spatial framework suitable for national-scale monitoring.
- Data governance and interoperability:
  - Integrates cartography, elevation, soils, urban boundaries, and agricultural data to improve thematic accuracy and usability.
  - Provides parcel-level metadata and a transparent KBE history to support reproducibility and revalidation.
  - Aims for stable spatial structure to enable cross-dataset comparability and future monitoring efficiency.
- Practical takeaways:
  - LCM2007 demonstrates mature, UK-wide data governance with detailed metadata, traceable processing steps, and contextual enhancements that improve thematic accuracy.
  - The 1 km products offer policy-relevant summaries; vector and 25 m data provide high-resolution detail and a foundation for change detection.
  - When using LCM2007 with other datasets, practitioners gain a robust evidence base for policy, planning, and resource management, while acknowledging residual uncertainties in barked areas like grasslands, fen, and coastal mosaics.
- Limitations and considerations:
  - Spectral confusion remains for some grassland and upland habitats; KBEs help but do not fully resolve all ambiguities.
  - Comparisons with CS are informative but constrained by differing spatial structures, MMU, and field survey methods.
  - Some coastal, montane and mosaic landscapes remain challenging; access to full vector/25 m data may be licensing-limited.
- European and broader context:
  - LCM2007 feeds into European-level assessments (e.g., Corine Land Cover) and aligns with pan-European datasets (e.g., IMAGE2006).
  - Emphasises the value of integrating multiple information sources (remote sensing, field surveys, soils, hydrology) for policy-relevant land information.

## key figures and takeaways (high-level)
- 23 LCM2007 classes map to 17 Broad Habitats; MMU 0.5 ha.
- Outputs: 25 m raster (23 classes), 1 km raster (percent and dominant class), and vector parcels with 10 attributes.
- Accuracy: ~83% overall (ground reference validation).
- Major advantages: coast-to-coast coverage, stable spatial framework, KBEs that improve thematic discrimination, robust governance and metadata.
- Notable challenges: spectral variability in grassland, fen, and coastal mosaics; differences with Countryside Survey due to methodological and spatial-structure differences.
- Strategic value for Data Leaders: demonstrates data-rich, governance-forward land cover mapping that supports policy, planning, and cross-dataset change detection, while highlighting the importance of contextual rules (KBEs) and transparent provenance.