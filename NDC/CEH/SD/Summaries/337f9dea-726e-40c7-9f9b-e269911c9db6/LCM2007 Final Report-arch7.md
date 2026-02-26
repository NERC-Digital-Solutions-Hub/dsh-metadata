# Final Report for LCM2007 - the new UK land cover map

## Overview
- First continuous parcel-based (vector) UK land cover map (LCM2007) with linked raster products.
- Built from national cartography (OS MasterMap, LPS MasterMap-like data) and multi-date imagery.
- Adds image segmentation, agricultural boundaries, and knowledge-based enhancements (KBEs) for improved thematic resolution.
- Delivers multi-resolution data products: vector (parcels), 25 m raster, and 1 km raster.

## Data framework and processing
- Spatial framework derived from detailed national cartography; enhanced by integrating agricultural boundaries and image segments to capture spectral variation.
- Minimum mapping unit: 0.5 ha; segments with fewer pixels are dissolved into similar neighbors.
- Image data: multi-date imagery (Landsat TM/ETM+, SPOT-4/5, IRS AWIFS/LISS-III); cloud masking and pre-processing (atmospheric/topographic correction, georegistration).
- Segmentation and post-segmentation integration with cartography to improve spectral homogeneity within parcels.
- Knowledge-based enhancements (KBEs): regionally adaptive rules using context such as terrain, soils, urban boundaries, and coastal proximity; seven KBE algorithms guiding reclassifications (Terrain, Soil, Terrestrial zone, Offshore, Within urban boundary, Outside urban boundary, Water).

## Data products and formats
- Vector product: land parcels with attributes including area, source images, Broad Habitat (BH), KBE history, ProbList (top 5 spectral class probabilities), CorePixels, and Construct history.
- 23 LCM2007 classes, with Broad Habitat aggregation to 10 groups for higher-level analyses.
- 25 m raster: 23 LCM2007 classes.
- 1 km raster: two outputs per location – (A) percentage cover per LCM2007 class; (B) dominant class per 1 km cell.
- Accessibility: 1 km rasters via CEH Information Gateway; full vector and 25 m rasters available on request (licensing may apply).

## Quality assurance and accuracy
- Ground reference data: 9127 points (2006–2008) for training and validation.
- Overall accuracy: approximately 83% across LCM2007 classes; class-specific accuracies vary (e.g., Bog producer/overall user accuracies around high-70s to low-90s in examples).
- Validation approach compares LCM2007 polygons with ground references; Producer’s accuracy (how CS classes map to LCM2007) and User’s accuracy (how likely LCM2007 class corresponds to CS truth) are reported.
- KBEs and spectral variability contribute to some remaining misclassifications, notably in grasslands and mosaic habitats.

## Dissimilarity with Countryside Survey (CS) 2007 and change mapping
- Dissimilar area estimates identified for: Arable and Horticulture; Improved Grassland; Neutral Grassland; Dwarf Shrub Heath; Bog; Montane Habitats; and coastal habitats.
- Key factors driving differences:
  - Classification definitions and spectral confusion.
  - Inclusion of Boundary and Linear Features in LCM2007’s Arable/Horticulture and field delineations.
  - Differences in how grassland types are defined and mapped (Neutral vs Improved; Rough grassland composition).
  - MMU-related spatial structure differences affecting area estimates (e.g., Fen, Marsh and Swamp being mosaics and small patches).
  - Temporal mismatches and the need for multi-year imagery in LCM2007 mapping.
- Fen, Marsh and Swamp areas are especially divergent due to spectral mosaic and small patch sizes; CS may classify such areas differently (often as Rough grassland or other grassland types).

## UK-wide and country-level extents
- LCM2007 indicates the UK is dominated by intensive land use (Arable + Improved Grassland) and Built-up areas; woodlands ~12% (Broadleaved + Coniferous).
- England exhibits the highest proportion of intensive land use; Scotland shows the largest share of Coniferous Woodland and more semi-natural mountainous habitats.
- 2007 vs 2000 comparisons show shifts in Arable and semi-natural grassland extents, with LCM2007 generally increasing arable area and slightly reducing urban figures relative to LCM2000 in some areas.

## Practical implications for GIS specialists
- LCM2007 provides a robust, reusable spatial framework suitable for national-scale habitat monitoring, biodiversity planning, ecosystem service assessment, and landscape planning.
- The parcel-based vector, complemented by 25 m and 1 km raster products, enables both detailed, parcel-level analyses and broad-scale spatial analytics.
- KBEs demonstrate how ancillary data (terrain, soils, urban context) improve thematic resolution beyond spectral classification; use ProbList and KBE history to assess uncertainty and apply custom validation.
- For change detection, be cautious about comparing products with different spatial structures; consider aggregating classes or reworking earlier maps into a common spatial framework before comparison.

## Accessibility and licensing
- 1 km raster data: CEH Information Gateway.
- Full vector and 25 m raster data: available on request from CEH (licensing may apply).
- Data suitable for a range of GIS applications, from national to parcel-scale analyses.

## Key takeaways for GIS practice
- LCM2007 marks a major advance in national scale land cover mapping by grounding classification in a durable, geometrically consistent spatial framework derived from national cartography and enhanced with multi-date imagery and KBEs.
- The multi-resolution data suite (vector, 25 m, 1 km) supports diverse GIS workflows, from policy-relevant landscape assessments to fine-grained habitat analyses.
- While offering improved consistency and change detection potential, users should be mindful of differences with CS and previous CEH maps when conducting cross-product change analyses, and leverage the parcel-level metadata (KBEs, ProbList) for validation and uncertainty assessment.