# Final Report for LCM2007 - the new UK land cover map

- The UK’s first continuous parcel-based land cover map (LCM2007) with 23 land cover classes mapped to 17 Broad Habitats, produced by CEH (NERC) in 2011.
- Provides coast-to-coast coverage of Broad Habitats and supports habitat monitoring, ecosystem services assessment, landscape planning, and policy development.
- Data products include vector parcels, 25 m raster, and 1 km summaries, designed for integration with national cartography and various GIS applications.

## Data sources and spatial framework

- Spatial frameworks and data inputs:
  - GB: generalised OS MasterMap topography and LPS large-scale vector; MMU 0.5 ha and minimum feature width 20 m (MFW).
  - NI: polygon framework created from LPS large-scale vector lines; integration with image segments.
  - Satellite imagery: combined use of Landsat TM/ETM+, SPOT, and LISS-III/AWIFS; multi-date composites (summer/winter) and some single-date images; cloud/cloud-shadow masking and atmospheric/topographic corrections applied.
  - Ground reference points and Countryside Survey (CS) data for validation and cross-checks.
- Segmentation and processing:
  - Image segmentation used to delineate spectral regions; segment-based vector framework integrated with GB/NI spatial frameworks.
  - Pre-processing included geo-registration, atmospheric and topographic corrections, and multi-date compositing to capture phenology.

## Data products and formats

- Vector product:
  - Land parcels with 10 attributes per polygon detailing processing steps, spectral classification, and knowledge-based enhancements (KBEs).
  - Includes Broad Habitat sub-classes (BHSub) and FieldCode, plus ProbList and KBE history.
- Raster products:
  - 25 m resolution raster with 23 LCM2007 classes.
  - 1 km raster products: (a) class percentage summaries per 1 km pixel; (b) dominant class per 1 km pixel.
- Scale and coverage:
  - ~10 million land parcels across GB (roughly 8.6M GB; 0.9M NI); 91% UK mapped from composites; 9% from single-date imagery; 0.5% manually corrected.
- Access:
  - 1 km rasters via CEH Information Gateway.
  - Full vector and 25 m raster data available under licence on request from CEH; licensing fees may apply.

## Classification and knowledge-based enhancements (KBEs)

- Classification approach:
  - Parcel-based supervised maximum likelihood classification of 37 composite images and 21 single-date images.
  - Training areas drawn from ground references and OS maps; iterative reclassification to improve accuracy.
- KBEs:
  - Seven automated KBEs applied sequentially to refine classifications using contextual data (urban, coastal, terrain, soils).
  - Approximately 20% of parcels revised by KBEs; KBEs are adjustable and can be deactivated to preserve user control.
  - KBEs enhance discrimination in challenging areas (e.g., uplands, semi-natural grasslands) but introduce additional uncertainty where signatures are ambiguous.
- Traceability:
  - Original spectral classification retained in ProbList for transparency and traceability.

## Validation, accuracy, and cross-dataset comparison

- Validation results:
  - Ground-reference validation: overall accuracy around 83% with class-level variation (higher for major classes; lower for upland/semi-natural categories).
  - Example class performance: Arable/Horticulture and Coniferous Woodland generally higher; Montane Habitats and several grassland types more challenging.
- Countryside Survey (CS) comparison:
  - Across 1 km CS squares and national estimates, CS and LCM2007 show varying levels of agreement by Broad Habitat.
  - Grasslands are a major area of discrepancy due to one-to-many relationships between grassland observed and Broad Habitat classifications; this led to the Broad Habitat Association (BHA) rules.
  - 1 km CS alignment: around 62% for Broad Habitats; 76% for Broad Habitat Association; higher alignment (~88–90%) when consolidating Grassland types.
  - Fen, Marsh and Swamp estimates show large differences due to complexity and small patch sizes; many CS Fen areas map as Rough Grassland or other categories in LCM2007.
- Interpretation framework:
  - The Broad Habitat Association rules provide a way to interpret cross-dataset correspondences and improve comparability between LCM2007 and CS.

## Change mapping and methodological considerations

- Change detection:
  - Change mapping is complex due to historical class differences (LCM1990, LCM2000, LCM2007) and evolving spatial frameworks.
  - Pixel-level change detection is difficult given typical classification error rates (~20%) and spectral/classification differences.
  - Recommended approaches include focusing on aggregated classes, using Broad Habitat Association mappings, or reorganising prior CEH maps into a common spatial framework to enable robust change analysis.

## Practical takeaways for GIS practitioners

- LCM2007 provides a robust, UK-wide, map-based data resource with rich metadata and a structure that supports change detection and integration with national cartography.
- Use KBEs to improve thematic detail in upland and semi-natural grassland areas, but account for increased uncertainty where signatures are ambiguous.
- The 1 km raster products enable scalable analyses and are suitable for coupling with climate, hydrology, or species distribution datasets.
- For cross-dataset comparison or integration with field surveys, aggregating grassland categories or using Broad Habitat Association mappings can enhance alignment with survey results.
- Be aware of:
  - Spectral confusion, especially for grasslands and complex mosaics.
  - Inclusion of boundary/linear features in Arable and Horticulture due to MMU considerations.
  - Temporal range of input imagery influences field classification and change interpretation.

## Key figures and highlights

- Land cover classes and Broad Habitats:
  - 23 LCM2007 land cover classes mapped to 17 Broad Habitats.
- Spatial scope:
  - UK-wide, GB-focused vector and 25 m raster, plus 1 km summaries.
- Validation and comparison:
  - Overall accuracy ~83%; stronger performance for arable, coniferous woodland; weaker for montane and some semi-natural classes.
  - Notable discrepancies with Countryside Survey for grasslands and fen-related classes; BHA rules aid interpretation.

## Data accessibility and licensing

- 1 km rasters: accessible via CEH Information Gateway.
- Full vector and 25 m raster: available under licence on request from CEH; licensing fees may apply.
- Data format trade-offs:
  - Vector datasets provide rich metadata per parcel but larger file sizes and heavier processing.
  - 25 m raster offers detailed land cover without extensive metadata; useful for some modeling scenarios.
  - 1 km rasters suitable for UK-scale modeling and integration with other large-scale datasets.