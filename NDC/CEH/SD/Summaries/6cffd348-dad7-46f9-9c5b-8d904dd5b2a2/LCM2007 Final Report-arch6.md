# Final Report for LCM2007 - the new UK land cover map

- The UK Land Cover Map 2007 (LCM2007) is a parcel-based land cover map produced from multi-sensor imagery, designed to map Broad Habitats across the UK with a linked suite of raster products and detailed vector metadata.
- It integrates high-resolution national cartography with multi-temporal imagery and knowledge-based enhancements to deliver a spectrum of data products for policy, planning and environmental research.

## Data scope and structure

- Data volumes and units
  - ~10 million land parcels (GB ~8.6 million; NI ~0.9 million)
  - Minimum mapping unit: 0.5 ha; minimum feature width: 20 m
- Classification and aggregation
  - 23 LCM2007 land cover classes aligned to Broad Habitats
  - Aggregation to 17 terrestrial Broad Habitats for higher-level analyses
- Spatial framework
  - GB: Ordnance Survey MasterMap (OSMM) core, generalised to MMU 0.5 ha and MFW 20 m
  - NI: LPS Large-scale Vector polygons integrated with image segments
  - Agricultural boundaries and image segments are used to refine delineation

## Data sources and processing

- Satellite and imagery
  - Primary sources: Landsat-TM5, IRS-LISS3, SPOT-4/5 (20–30 m pixels)
  - AWIFS (60 m) used as backup
  - 91% classified from summer–winter composites; remainder from single-date images; manual hole-filling where needed
- Ground truth and reference datasets
  - Ground reference points for training/validation (CEH)
  - Countryside Survey Broad Habitat data (CS 2007)
  - Supporting national cartography, soil data, digital elevation models, urban outlines
- Pre-processing and segmentation
  - Cloud masking, atmospheric correction, geo-registration (RMSE < 0.3 pixel), topographic correction
  - Creation of 6-band summer–winter composites; 60 composites segmented
  - Segments integrated with OSMM and agricultural boundaries to create a segment-based vector framework
- Data formats
  - Vector: polygons with 10+ attributes per parcel
  - Raster: 25 m (23 classes) and 1 km products (percent cover and/or dominant class)

## Classification approach and knowledge-based enhancements

- Classification
  - Parcel-based supervised maximum likelihood classifier
  - Training areas derived from ground reference data
  - 23 LCM2007 classes mapped to Broad Habitats; probability of top spectral classes recorded
- Knowledge-based enhancements (KBEs)
  - Seven automated KBEs applied in sequence to refine parcel classifications using context and auxiliary data
  - Contextual types include urban, coastal proximity, terrain and soil information
  - KBEs typically modify around 20% of parcels; the original spectral classification remains accessible via ProbList
- Interpretability
  - Outputs designed to support decomposition of some classes (e.g., various grassland types) using KBEs
  - Some mismatch with field-based Broad Habitats acknowledged due to spectral vs. species-based indicators

## Data products and content

- Class structure and outputs
  - 23 LCM2007 classes mapped to 17 Broad Habitats
  - 1 km raster products: either percent cover or dominant class per pixel (for all 23 classes and 10 aggregates)
  - 25 m raster: 23-class detail
  - Vector product: parcel-level polygons with detailed metadata and processing history
- Metadata and provenance
  - Vector attributes include Construct, ProbList, KBE history, and linkage to source images
  - ProbList provides the five most likely spectral variants for quality assessment
- Access and licensing
  - 1 km raster data via CEH Information Gateway
  - Full vector and 25 m data available on request (licence may apply)

## Quality assurance, validation and limitations

- Validation data and accuracy
  - Ground reference: 9,127 points (2006–2008)
  - Overall accuracy: 83% across classes
  - Class-level accuracy varies; example: Bog ~93% producer’s accuracy
- Validation structure
  - Producer’s accuracy reflects how well reference classifications are captured
  - User’s accuracy reflects how well LCM2007 classes align with field-validated classes
- Limitations and caveats
  - Some classes show lower accuracy due to spectral similarity and confusion
  - KBEs can improve thematic resolution but may reduce accuracy for some externally sourced data (soil/urban datasets)
  - Differences in spatial structure and MMU between LCM2007 and CS introduce complexities in cross-comparisons

## Comparison with Countryside Survey (CS) 2007

- Thematic correspondence and aggregation
  - Broad Habitat correspondence to CS ~62% UK-wide
  - Broad Habitat Association (BH adjacencies) improves to ~76%
  - Aggregate class correspondence ~67%
- Country-level patterns
  - England: BH correspondence ~67%
  - Scotland: BH correspondence ~56% (BH Association ~81%)
  - Wales: BH correspondence ~58% (BH Association ~72%)
- Key mismatches and causes
  - Woody cover, conifer vs broadleaved woodland, grassland sub-types, fen/marsh/swamp mosaics
  - Differences in urban boundary mapping and feature inclusion
  - Grassland reclassification (e.g., collapse into a single grassland class) improves CS–LCM correspondence
- Implications
  - Grassland classification remains a challenge; Broad Habitat Associations aid crosswalks with CS concepts
  - Level of agreement varies across habitats; complex mosaics and scale differences influence results

## Change mapping and temporal considerations

- Complexity of change analysis
  - LCM1990, LCM2000, and LCM2007 differ in spatial structure and class definitions, complicating change detection
  - Per-parcel change error can be high; robust change methods are not fully established
- Suggested approaches
  - Use aggregated classes or focus on consistently mapped classes
  - Reorganise earlier LCM maps into a common spatial framework based on real-world land-use units for improved change detection

## Applications and data use

- Scientific and policy relevance
  - Provides a robust baseline for habitat monitoring, biodiversity assessment, ecosystem services, and landscape planning
  - Supports policy contexts such as Natura biodiversity targets, woodland expansion analysis, and cross-country comparisons
- Data synergy
  - Works best when combined with in situ data, LiDAR, climate, soil and hydrology datasets
  - Facilitates evidence-based environmental decision making across multiple sectors

## Access, licensing and quick references

- Data access points
  - 1 km rasters: CEH Information Gateway (gateway.ceh.ac.uk)
  - Full vector and 25 m data: on request via CEH data portal or spacialdata@ceh.ac.uk
- Licensing notes
  - Some products may require licences or fees depending on user category and product type

## Key figures and quick takeaways

- Ground truth: 9,127 validation points
- Overall accuracy: 83%
- Parcels: ~10 million (GB ~8.6M; NI ~0.9M)
- Imagery: ~91% composite; ~9% single-date; small proportion hole-filled
- KBEs: typically affect ~20% of parcels
- Land cover distribution (UK) highlights intensive agriculture and built-up areas as dominant components, with significant regional variation

## Takeaway for data support and reuse

- LCM2007 delivers a comprehensive, multi-resolution UK land cover framework with a transparent uncertainty context, robust QA, and a rich vector metadata trail to support re-use, validation, and integration with other national datasets.
- Users should heed spatial and thematic uncertainties, particularly for grassland and fen-related classes, and leverage Broad Habitat Associations for crosswalks with other habitat classifications.
- The data are suited for national-scale analyses,change detection planning, and policy-support workflows when used alongside complementary high-resolution, ground-based datasets.