# Final Report for LCM2007 - the new UK land cover map

- Overview
  - A national, parcel-based land cover map for the UK, with UK-wide vector data and accompanying raster products at 25 m and 1 km resolutions.
  - Provides Broad Habitat (BH) mappings and related datasets to support biodiversity assessment, landscape analysis, and policy applications.

## Data scope and classifications
- 23 LCM2007 classes mapped, aggregated to 17 Broad Habitats for higher-level interpretation.
- Minimum mapping unit (MMU) of 0.5 ha.
- GB-wide products: vector with attributes and a 25 m raster; NI data integrated into production but stored separately.
- Nine GB spatial chunks used to assemble seamless UK-wide coverage.

## Data sources and processing workflow
- Based on more than 70 satellite images (Landsat-TM5, IRS-LISS3, SPOT-4/5; AWIFS as backup) and 34 multi-date composites (summer + winter) plus some single-date imagery.
- Spatial framework anchored to Ordnance Survey MasterMap (GB) and NI Large-scale Vector datasets; supplemented with agricultural boundaries and image segments.
- Image pre-processing includes cloud masking, atmospheric and topographic corrections; geo-registration to sub-pixel accuracy; segmentation to create a segment-based vector framework.
- Segmentation bands typically winter NIR, summer red, and MIR; selective hole-filling and manual edits applied where needed.

## Classification and knowledge-based enhancements
- Parcel-based supervised maximum likelihood classification using training data from ground references and CS Broad Habitats.
- 37 composites and 21 single-date images classified into 23 LCM2007 classes; post-classification knowledge-based enhancements (KBE) applied to resolve spectral confusion.
- Seven automated KBEs (e.g., Terrain, Soil, Zoning, Urban, Water) applied sequentially to refine classes; KBEs adjust around 20% of parcels; manual QA maintained to minimize errors.

## Spatial framework and segmentation
- Boundaries generalised from high-resolution cartography to fit the MMU/MFW constraints, with segment-level segmentation capturing spectral regions not evident from cartography alone.
- Core pixels used for training and classification; a comprehensive metadata trail (KBE history, ProbList, etc.) attached to parcels.

## Validation and accuracy
- Ground truth: 9,127 points collected (2006–2008) for validation.
- Overall accuracy: 83% across classes; class-specific accuracy varies (some grassland and upland classes more variable).
- Validation considers producer’s accuracy (how well reference areas map to intended class) and user’s accuracy (likelihood a mapped parcel matches ground truth).

## Data products and access
- Vector data: polygons (parcels) with attributes including area, source images, Broad Habitat, KBE history, ProbList, CorePixels, and Construct.
- Raster data:
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: either percent cover per class or dominant class per pixel.
- Access:
  - 1 km raster datasets available via the CEH Information Gateway.
  - Full vector and 25 m raster products available under licence on request from CEH (licence fees may apply).
  - Comprehensive documentation and metadata accompany data products.

## Relationship to Countryside Survey and key divergences
- Comparisons with Countryside Survey (CS) 2007 show varying agreement across Broad Habitats.
- Grassland classes drive much of the discrepancy due to one-to-many mappings to Broad Habitats and spectral variability; Broad Habitat Association (BHA) rules were developed to improve interpretability.
- Fen, Marsh and Swamp shows large UK-scale discrepancies (CS ~4392 km2 vs. LCM2007 ~101 km2) due to mosaic nature, small patch sizes, and spectral confusion; many CS fen areas map as Rough Grassland or Acid Grassland in LCM2007.
- LCM2007 aligns well with CS for 1 km squares in Arable and Horticulture, but total Broad Habitat extents often differ due to class definitions and temporal imagery requirements.
- The document discusses potential future work to allocate certain grassland/fen components via KBEs to improve cross-walks with CS.

## Practical implications and use cases
- Provides a consistent UK-wide evidence base for biodiversity trend analysis, habitat connectivity, ecosystem services assessment, and catchment management.
- Facilitates multi-source data integration with explicit metadata on processing steps and knowledge-based adjustments.
- Supports policy and planning activities with standardized, map-based representations of Broad Habitats and land cover patterns.

## Limitations and considerations
- Change mapping across LCM1990, LCM2000, and LCM2007 is challenging due to differing class schemes and spatial structures; robust change detection requires careful methods and potential re-organisation of earlier maps into a common spatial framework.
- Spectral similarity and KBEs can still yield misclassifications, particularly for grassland and upland habitats; some classes (e.g., Fen-related categories) are difficult to resolve spectrally and contextually.
- Differences in urban and boundary representations between CS and LCM approaches affect fine-scale comparability.
- MMU of 0.5 ha means very small features or rare habitats may be underrepresented or generalized.

## Change detection and future work
- Emphasises the need for sophisticated methods to distinguish real land-cover change from artefacts arising from different spatial/thematic structures.
- Suggests future reorganisation of earlier CEH maps into a common spatial framework based on real-world land-use units to enable robust change detection and monitoring.

## Governance, licensing and metadata
- Documentation provides governance notes, licensing information, and data schemas.
- Includes Broad Habitat Association (BHA) framework to aid cross-walks between CS and LCM classifications where direct mapping is not one-to-one.
- Appendices cover validation approaches, BHA rationale, and detailed metadata for data products.

## Notable data access points and contacts
- CEH Information Gateway for 1 km raster data.
- CEH data licensing for full vector and 25 m raster products (spatialdata@ceh.ac.uk or www.ceh.ac.uk/data).