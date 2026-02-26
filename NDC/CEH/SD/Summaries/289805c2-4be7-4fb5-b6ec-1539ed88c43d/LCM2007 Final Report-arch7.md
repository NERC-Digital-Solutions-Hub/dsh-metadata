# Final Report for LCM2007 - the new UK land cover map

## Overview and aims
- UK-wide, parcel-based land cover map (LCM2007) produced to support biodiversity, landscape planning, and policy; builds on prior LCM editions.
- Outputs include a vector parcel product, 25 m raster, and 1 km raster products; aligned to Broad Habitats for UK biodiversity reporting.
- Utilizes a UK-wide spatial framework derived from detailed cartography (Ordnance Survey MasterMap and LPS Large-scale Vector) to enable better data interoperability and change detection.

## Data structure and outputs
- Vector product: 23 LCM2007 classes mapped to 10 Aggregate/Broad Habitat groupings; 9,127 ground-reference validation points; MMU of 0.5 ha; includes extensive parcel metadata and knowledge-based enhancements (KBEs).
- Raster products:
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: (a) per-class percentage cover and (b) dominant class per pixel.
- Attributes and metadata:
  - Parcel-level attributes include area, source images, Broad Habitat (BH) and sub-classes, KBE history, ProbList (top spectral variants), core pixels, and construction history.
  - KBEs post-classification refine classifications; users can disable KBEs if needed.
- Data access:
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m raster data available on request (licensing may apply).

## Data inputs, processing, and spatial framework
- Data sources:
  - Multi-date satellite imagery (Landsat TM/ETM+, SPOT, IRS LISS/AWIFS) with cloud masking and atmospheric/topographic corrections.
  - National cartography (OS MasterMap GB, LPS NI), DEMs, soils, urban boundaries, and other ancillary layers.
  - Ground reference data from CEH fieldwork and CS datasets for validation.
- Image processing workflow:
  - Pre-processing, image segmentation, parcel-based classification (maximum likelihood) with KBEs applied iteratively.
  - Segmentation uses multi-date composites (winter NIR, summer red, summer MIR); background NI segmentation supplements composites.
  - Post-classification refinement through seven automated KBEs to resolve spectral confusion and improve thematic resolution.
- Spatial framework:
  - GB framework based on OSMM with agricultural boundaries; NI framework uses generalised LPS with segmentation integration.
  - Generalisation includes MMU 0.5 ha and minimum feature width (MFW) 20 m; segmentation enhances spectral coherence.

## Knowledge-based enhancements (KBEs)
- Seven automated KBEs applied to reclassify parcels using contextual data (urban context, coastal proximity, terrain, soils, etc.).
- KBEs help distinguish montane habitats, bogs, calcareous/acid grasslands, and refine to separate Rough grassland into Neutral/Calcareous/Acid Grassland where applicable.
- KBEs are documented in parcel attributes and can be disabled by users if desired.

## Change mapping and comparability with Countryside Survey (CS)
- Change detection between LCM editions is challenging due to differing class definitions, spatial structures, and error rates (~20% per image).
- 4.3.2 and 4.3.3 discuss causes of dissimilar area estimates between LCM2007 and CS2007, including:
  - Definitions and classifications of Arable and Horticulture, Improved/Neutral Grasslands.
  - Spectral confusion and the inclusion of Boundary/Linear Features in LCM2007.
  - MMU-related differences and the impact of multi-year image composites on land-use categorisation.
  - Spatial structure differences and patch size effects (Fen/Marsh/Swamp, Montane, coastal habitats).
- 4.5 emphasizes that grassland classifications are particularly problematic due to one-to-many relationships with Broad Habitats; the Broad Habitat Association (BHA) approach adds a third-level accuracy check for cross-walker correspondences with CS.

## UK Land Cover distribution and cross-country variation
- Overall UK distribution: over half of land is intensive (Arable & Horticulture + Improved Grassland) or built-up; woodland ~12%; semi-natural ~30%.
- Country-level patterns:
  - England: highest intensive land use (~76%).
  - Scotland and Northern Ireland: substantial semi-natural cover and woodland; Scotland has the largest proportion of Coniferous Woodland and upland semi-natural habitats.
  - Wales: notable Arable/Grassland dynamics; variability in boundary and urban components.
- LCM2007 vs LCM2000: broad shifts include higher Arable and semi-natural grassland extents; woodland and urban areas show modest changes.

## Validation, accuracy, and interpretation
- Overall accuracy around 83% against ground reference data.
- Class-level performance varies:
  - Bog tends to be well-predicted; some grassland classes show confusion (Neutral, Calcareous, Acid) and upland mosaic effects.
  - Fen, Marsh and Swamp shows clear differences from CS due to mosaic and small patch sizes.
- Validation suggests strengths in woody, arable, and freshwater classes; weaker performance for several semi-natural upland habitats.

## Access, usage, and applications for GIS specialists
- Data are designed for map-based visualization and analysis in policy contexts, biodiversity assessments, landscape planning, habitat connectivity, and catchment management.
- The vector product provides detailed attribute histories (KBE tracks) and probabilistic class information (ProbList) for advanced QA and validation workflows.
- The 1 km raster product is suitable for UK-scale modelling and integration with climate, meteorological, or species distribution data.
- Guidance on use:
  - For change detection or policy-relevant analyses, consider aggregating to more stable Broad Habitats or using BH Association rules to interpret grassland dynamics.
  - Be mindful of MMU limitations and sub-class uncertainties, especially for small patches and mosaics (Fen, Montane, Coastal habitats).
  - Leverage parcel-level KBEs and metadata to assess attribution confidence at your location.

## Significance and policy context
- LCM2007 provides a cohesive, coast-to-coast UK land cover framework suitable for policy and monitoring, enabling cross-country comparisons and integration with European datasets (e.g., Corine Land Cover).
- Serves as a robust baseline for habitat networks, landscape planning, carbon accounting, flood risk modelling, urban studies, and biodiversity surveillance.
- Emphasizes the importance of combining in situ data with satellite-derived maps for comprehensive understanding of the UK landscape.

## Practical notes for implementation and future work
- Change detection between LCM editions requires sophisticated approaches due to structural differences; re-organising prior maps into a common spatial framework could improve temporal comparability.
- Additional data integration (e.g., fine-scale habitat data, improved grassland classifications) could enhance Fen, Marsh, Swamp mapping and grassland discrimination.
- Future work could focus on refining KBEs, improving boundary feature handling, and extending the shared spatial framework for ongoing national land cover monitoring.

## Summary takeaways for GIS practitioners
- LCM2007 delivers a high-quality, parcel-based UK land cover map with rich metadata, multiple data formats, and strong policy relevance.
- Expect variability in grassland-related classes and certain upland/coastal habitats when aligning with CS or other land cover products.
- Use the KBEs and ProbList to assess classification confidence and to guide validation and application-specific decisions.
- Data access is available with licensing; vector and 25 m data offer the most detail, while 1 km rasters are ideal for national-scale analyses.