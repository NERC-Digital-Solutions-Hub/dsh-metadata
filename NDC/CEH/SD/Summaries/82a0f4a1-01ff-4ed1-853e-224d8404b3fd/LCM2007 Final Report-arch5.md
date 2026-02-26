# Final Report for LCM2007 - the new UK land cover map

## Overview for Data Stewards
- LCM2007 delivers the first continuous parcel-based UK land cover map, with 23 land cover classes aligned to Broad Habitats and multiple derived products (full UK vector, 25 m raster, 1 km rasters).
- A single, cross-border spatial framework underpins the dataset, enabling consistent monitoring and change detection across GB and Northern Ireland.
- The data are intended to support habitat monitoring, policy reporting, and landscape analysis, with a strong emphasis on provenance, reproducibility, and reusability.

## Data sources, provenance and spatial framework
- Spatial framework:
  - Based on Ordnance Survey MasterMap (GB) and LPS Large-scale Vector (NI), generalised to real-world land units.
  - Minimum mappable unit (MMU) of 0.5 ha; segmentation and integration of image segments with cartographic boundaries to improve spectral coherence.
- Data sources:
  - National cartography, agricultural boundaries, urban datasets, soils, DEM, coastline and terrain data.
  - Satellite imagery: multi-temporal composites from Landsat, SPOT, LISS-III, AWIFS across multiple dates to maximise spectral information.
- Data processing:
  - Image pre-processing (atmospheric, topographic corrections), cloud masking, georeferencing accuracy aiming for sub-pixel precision.
  - Parcel-based vector framework created by merging segmentation results with cartography, enhancing boundary delineation.

## Data products and metadata
- Vector product: 23 land cover classes with 10 processing attributes (e.g., Construct, ProbList, KBE history) at parcel level; includes Broad Habitat sub-classes and FieldCode descriptors; ProbList provides top spectral class probabilities.
- Raster products:
  - 25 m resolution with 23 LCM2007 classes.
  - 1 km rasters: percentage cover per class and dominant class per pixel.
- Metadata and provenance:
  - Rich processing history, KBEs (Knowledge-Based Enhancements), and traceability to inputs and processing steps; enables reproducibility and post-hoc validation.

## Classification workflow and knowledge-based enhancements
- Parcel-based supervised classification using multi-temporal imagery to derive 23 classes aligned with Broad Habitats.
- Knowledge-Based Enhancements (KBEs):
  - Seven automated rules applied in sequence to resolve spectral confusions and improve thematic resolution.
  - KBEs incorporate context like urban boundaries, proximity to coast, terrain, soil type; terrain and soil data help distinguish complex upland habitats.
  - ProbList maintains original spectral classifications to allow inspection and potential reversal of KBEs.

## Quality assurance, validation, and caveats
- Validation:
  - Ground reference data: 9,127 points; overall accuracy around 83% with class-dependent variations.
  - Validation conducted during and after classification, with attention to alignment between polygon boundaries and ground-truth points.
- Limitations and interpretation:
  - Grassland categories exhibit notable ambiguity due to one-to-many relationships with Broad Habitats; Broad Habitat Association (BHA) rules are used to interpret correspondences.
  - Spatial framework differences between LCM2007 and Countryside Survey (CS) complicate direct change detection.
  - Fen, Marsh and Swamp areas show substantial differences between CS 2007 and LCM2007 due to mosaic nature and spectral complexity; some CS fen areas are mapped as Rough Grassland or Acid Grassland in LCM2007.
  - Some classes (e.g., Montane, coastal habitats) are less well represented in CS comparisons due to sampling design.

## Change mapping and comparison with Countryside Survey (CS)
- Methodological notes:
  - CS provides national estimates and a field-based baseline for comparison; LCM2007 offers coast-to-coast coverage and consistent spatial framework.
  - Robust change detection is challenging due to differing spatial structures, class definitions, and temporal ranges; emphasis suggested on aggregated classes or trajectory-based methods.
- Key comparative insights:
  - LCM2007 shows high correspondence with CS 2007 for Arable and Horticulture at the 1 km square level, but overall Broad Habitat extents for Arable and Horticulture tend to be higher in LCM2007.
  - Grassland-related classes require careful interpretation; BHA rules improve cross-dataset correspondence in some regions, especially upland/mosaic areas.
  - Fen, Marsh and Swamp exhibits large discrepancies; a substantial portion of CS fen areas map to Rough Grassland or Acid Grassland in LCM2007, suggesting potential KBEs to reallocate some areas in future work.

## UK distribution and extents (highlights for governance)
- UK distribution: more than 50% of land in intensive use (Arable and Horticulture plus Improved Grassland) or Built-up Areas; remaining land is semi-natural, with woodlands around 12% (split between Broadleaved and Coniferous).
- Country breakdown:
  - England: about 76% intensive land use (40% Arable and Horticulture; 27% Improved Grassland; 9% Built-up). 
  - Scotland: 36% intensive; large shares of Coniferous Woodland and semi-natural habitats (montane, grassland).
  - NI and Wales: around 64% intensive land use.
  - Coastal and semi-natural categories account for the remainder, with notable regional variation.

## Access, licensing and dissemination
- 1 km raster datasets are available via the CEH Information Gateway.
- Full vector and 25 m raster products are available on request under licence; licensing fees may apply.
- The data portfolio supports habitat monitoring, policy reporting, and landscape analyses; intended for broad use across sectors.

## Practical implications for Data Stewards
- Data governance and interoperability:
  - Integrated, multi-source spatial framework enhances interoperability with other national products and supports consistent monitoring.
  - Timely updates and versioning require careful management to maintain comparability with prior products.
- Metadata, provenance and reproducibility:
  - Rich parcel-level metadata (KBEs, ProbList, processing steps) enables reproducibility and informed reprocessing as inputs evolve.
- Quality assurance and validation:
  - An 83% overall accuracy indicates ongoing need for region-specific QA, potential user-driven validation, and regionally targeted improvements.
- Licensing and licensing management:
  - Mixed data sources necessitate clear attribution and licensing compliance; plan for distribution costs in large-scale or commercial use.
- Change detection and policy relevance:
  - Sophisticated change-detection approaches are needed due to structural differences between maps; consider aggregations or cross-walks (Broad Habitats, BH/BHA frameworks) for robust monitoring and reporting.
- Forward-looking governance:
  - The KBEs and Broad Habitat Association rules provide a framework for ongoing refinement; future work could incorporate additional data layers (e.g., soil, habitat quality, species composition) to improve accuracy for mosaic and fen-type habitats.

## Key takeaways
- LCM2007 represents a major advance in UK land cover mapping: parcel-based, coast-to-coast coverage with a robust spatial framework and a suite of data products (vector, 25 m, 1 km rasters).
- The integration of multi-temporal imagery, image segmentation, and knowledge-based rules yields improved thematic resolution but also reveals persistent classification challenges, notably for grassland, fen, bog, montane, and coastal habitats.
- External benchmarks (Countryside Survey) are valuable for validation but emphasize the need for careful interpretation due to methodological differences.
- For data stewards, the document underscores the importance of rigorous provenance, clear licensing, ongoing QA, and thoughtful approaches to change detection in the context of evolving inputs and rules.