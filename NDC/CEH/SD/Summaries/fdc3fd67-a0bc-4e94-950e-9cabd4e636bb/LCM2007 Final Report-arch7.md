# Final Report for LCM2007 - the new UK land cover map

## Overview
- First continuous parcel-based (polygon) UK land cover map (LCM2007) produced for Countryside Survey 2007.
- Provides UK-wide stock and distribution of Broad Habitat-based land cover, with a strong emphasis on spatial units that are real-world, reusable boundaries for monitoring and change detection.
- Supports policy-relevant biodiversity, landscape planning, ecosystem services, and catchment-scale analyses; designed to integrate with other datasets and national products.

## Data products and formats (GIS-focused)
- Vector product: land parcels (polygons) with 10 processing attributes, 23 LCM2007 classes, and 17 Broad Habitats via aggregation; includes KBE (knowledge-based enhancements) history and ProbList per parcel.
- Raster products:
  - 25 m resolution: 23 LCM2007 classes (rasterized from vector).
  - 1 km resolution: two variants per pixel (A) percentage cover by class and (B) dominant class.
- Spatial framework: approximately 10 million parcels; minimum mappable unit (MMU) 0.5 ha; minimum feature width 20 m; separate GB and NI databases to accommodate different spatial references.
- Accessibility and licensing:
  - 1 km rasters via CEH Information Gateway.
  - Full vector and 25 m rasters available on license, by request to CEH.
- Metadata and traceability: full lineage, processing steps, and KBE history stored per parcel; Targeted data formats to support GIS workflows and post-processing.

## Spatial framework and data sources
- Data foundations: detailed national cartography (Ordnance Survey MasterMap, LPS Large-scale Vector), agricultural boundaries, soils, DEM (NEXTMap), coastal and contextual layers.
- UK-wide segmentation:
  - GB: segments aligned to MMU/Minimum Feature Width; integrated with agricultural boundaries and image segments to create a seamless vector product.
  - NI: uses NI-specific vector data and segmentation; integration with image segments.
- Pre-processing and segmentation inputs include multi-date satellite composites (e.g., Landsat TM/E, SPOT, LISS-III) and associated ancillary data.

## Processing workflow (image analysis and GIS-ready outputs)
- Pre-processing:
  - Cloud masking, atmospheric and topographic corrections; geo-registration achieving sub-pixel RMSE (<0.3 px).
  - Topographic correction using NEXTMap DEM; multi-date composites created.
- Image segmentation:
  - Three-band (winter NIR, summer red, summer MIR) segmentation on 60 composite images.
  - Segments merged with OSMM parcels and agricultural boundaries to enhance delineation.
  - Manual hole filling where composites were insufficient.
- Classification:
  - Parcel-based supervised maximum likelihood classification; training data from ground references; 37 composites and 21 single-date images.
  - Final product maps 23 LCM2007 classes aligned to Broad Habitats; 0.5 ha MMU; 25 m raster used for vector-to-raster product consistency.
- Knowledge-based enhancements (KBEs):
  - Applied to ~20% of parcels to resolve spectral confusion and refine thematic resolution using context (terrain, soils, proximity to coasts, urban context, water).
  - KBEs support reclassification (e.g., grassland subtypes) and enhanced habitat mapping; many KBEs are reversible at user option via vector attributes.

## Accuracy, validation, and comparisions (GIS practitioner relevance)
- Validation dataset: ground reference points (~9,127 points) from 2006–2008.
- Overall accuracy: about 83% across classes; class-level accuracy varies.
- Countryside Survey (CS) comparisons:
  - 1 km CS squares show notable correspondences at various levels:
    - ~62% correspondence at Broad Habitat level; ~67% at Broad Habitat Association; ~76% at aggregate BH Association level (GB).
  - Grassland-related classes show higher variability due to one-to-many mappings between spectral classes and BHAs; KBEs and BHAs developed to address this.
  - Major discrepancies observed in:
    - Arable and Horticulture: LCM2007 may include boundaries/linear features and temporary grass in the mapped area, leading to higher area estimates than CS.
    - Improved vs Neutral Grassland: differences largely reflect how each product handles neutral/Improved grassland and soil context.
    - Fen, Marsh, Swamp: large disparities due to spectral complexity and small patch sizes; many Fen areas in CS map as Rough Grassland or Acid Grassland in LCM2007.
- Change mapping considerations:
  - Real change vs mapping/classification errors is difficult to separate; different base class definitions across generations (LCM2000, LCM2007) complicate temporal change detection.
  - Robust change detection requires methodological alignment or reorganization of earlier maps into a common spatial framework.

## Practical GIS implications and guidance
- Use Broad Habitat Associations (BHAs) to interpret correspondences with CS and other datasets; expect differences due to class definitions and MMU/generalisation.
- Leverage parcel-level metadata (KBE history, ProbList, etc.) to assess classification confidence and to inform reclassification or local adaptation.
- For grassland subtype mapping, consider using the single grassland class approach to improve correspondence with field surveys.
- When integrating with other data (e.g., soils, elevation, urban data), KBEs provide a transparent trail of adjustments (e.g., soil corrections, coastal masks, urban context) that aid interpretation.
- The 1 km raster product is suitable for UK-wide modeling with coarser resolution needs; 25 m raster and vector formats are better for site-level analyses and policy-relevant reporting.

## Change detection and temporal considerations
- LCM2007 represents a shift to a generalized, static spatial framework built from national cartography, enabling consistent large-scale monitoring but requiring careful interpretation when comparing with previous maps.
- Temporal alignment challenges arise because image acquisition spans multiple years and class definitions differ; robust change detection benefits from aggregating to stable/broader classes or re-projecting to a common structure.

## Applications and significance for GIS workflows
- Provides a coherent UK-wide land cover reference aligned to Broad Habitats, enabling habitat monitoring, landscape planning, biodiversity policy support, and ecosystem-service analyses.
- Facilitates spatially consistent change detection and cross-country comparisons due to standardized parcel-based structure.
- Rich metadata and KBEs enable flexible post-processing and adaptation to local contexts or alternative habitat schemes.

## Access and licensing (summary)
- 1 km rasters: CEH Information Gateway (gateway.ceh.ac.uk).
- Full vector and 25 m rasters: licensing on request via CEH data portal or by contacting spatialdata@ceh.ac.uk.
- Fees may apply; licensing terms vary by use case.

## Takeaways for GIS specialists
- LCM2007 offers a high-resolution, parcel-based UK land cover framework with extensive metadata and knowledge-based corrections, designed for robust GIS analysis and policy-relevant applications.
- Expect and plan for differences relative to field surveys and earlier maps; use BHAs and KBE traces to interpret classifications and to calibrate local applications.
- Choose the appropriate data product (vector, 25 m, or 1 km) based on the scale and computational considerations of the GIS workflow, while leveraging the extensive metadata for quality assessment and methodological transparency.