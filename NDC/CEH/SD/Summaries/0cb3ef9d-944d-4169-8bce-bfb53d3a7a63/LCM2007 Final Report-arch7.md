# Final Report for LCM2007 - the new UK land cover map

- Purpose and scope
  - Introduces LCM2007: the UK-wide, parcel-based land cover map aligned with Broad Habitats for GIS-based analysis and policy support.
  - Provides coast-to-coast UK coverage with a generalised spatial framework suitable for change detection and multi-scale analyses.

- Data framework and spatial structure
  - Continuous UK vector product with NI maintained separately due to different spatial references; nine GB/Northern Ireland chunks enable seamless boundaries.
  - MMU of 0.5 ha and minimum feature width of 20 m; OS MasterMap-based GB framework (NI uses NI Large-scale Vector with image segments).
  - Outputs include a 25 m raster (23 LCM2007 classes) and 1 km summary products; a linked, rich vector product with 10 processing/interface attributes.

- Data sources and preprocessing
  - Multi-temporal satellite data primarily 20–30 m: Landsat-TM5, IRS-LISS3, SPOT-4/5; AWIFS as backup.
  - Ground reference: CEH field points for validation; extensive external datasets (cartography, boundaries, urban areas, elevation, soils).
  - Preprocessing chain: cloud masking, atmospheric/topographic correction, geo-registration, composite creation, hole-filling.

- Segmentation, classification, and KBEs
  - Image segmentation from 3-band composites (winter NIR, summer red, summer MIR); integration with OSMM boundaries and agricultural vectors.
  - Parcel-based supervised classification (Maximum Likelihood) across 37 composites and 21 single-date images to 23 LCM2007 classes (representing 17 Broad Habitats).
  - Knowledge-Based Enhancements (KBEs): seven automated algorithms applying context/ancillary data (urban proximity, terrain, soils, etc.), influencing ~20% of parcels.
  - KBEs help resolve spectral confusion; some Broad Habitats remain spectrally indistinguishable, so KBEs are used with documented uncertainties and manual overrides when needed.

- LCM2007 data products and metadata
  - Vector product: parcels with 10 attributes (including processing steps, KBE history, probabilities).
  - Raster products: 25 m resolution (23 classes) and 1 km summaries (percent cover and dominant class) for UK-wide analyses.
  - Broad Habitat-aligned structure with Aggregate classes for analysis/display; extensive metadata supports traceability and QA.

- Validation and quality assurance
  - Ground reference validation: 9127 CEH points; overall accuracy around 83% with class-specific variations.
  - Producer’s vs User’s accuracy reported per class to illustrate error patterns (e.g., upland vs lowland classes, conifer woodland, grasslands).
  - Country-level and habitat-specific comparisons with Countryside Survey (CS 2007) to assess agreement and identify systematic differences.

- Countryside Survey (CS) comparison: key findings
  - Broad Habitat correspondence GB: ~62%; Broad Habitat Association: ~76%.
  - Grassland categories show notable discrepancies due to one-to-many mapping between land cover and habitat types; BHA (Broad Habitat Association) provides a nuanced linkage.
  - Arable and Horticulture area in CS 2007 aligns with UK CS-derived totals, but LCM2007 often higher for this class due to temporal image range and inclusion of boundary/linear features.
  - Fen, Marsh and Swamp areas show large UK-scale differences driven by mosaic nature and small patches; some CS records map to Rough Grassland or other grassland classes in LCM2007.
  - Nine country-level analyses reveal spatially varying correspondences, influenced by landscape patterns and survey methodology.

- UK land cover distribution and cross-country context
  - Summary: over half of UK land cover is intensive agriculture or built-up; woodlands ~12% (split between Broadleaved and Coniferous).
  - England shows highest intensive land use; Scotland has substantial Coniferous Woodland and Montane/ upland diversity; NI/Wales show different regional patterns.
  - Long-term context: LCM2007 builds on LCM2000 methods and provides improved spatial coherence via a unified cartographic framework, aiding cross-country comparisons and policy evaluation.

- Applications and access for GIS specialists
  - Primary uses: habitat monitoring, biodiversity policy support, ecosystem services, landscape planning, catchment management, and environmental policy analysis.
  - Access options
    - 1 km raster: CEH Information Gateway.
    - Full vector and 25 m raster: licensing on request from CEH (possible fees).
  - GIS considerations
    - MMU/MFW design supports robust GIS workflows and change detection.
    - KBEs enable scenario testing and post-classification corrections; vector attributes support inspection of processing history.
    - Data at multiple scales (25 m raster, 1 km summaries, vector) supports integration with other GIS layers and modelling.

- Practical guidance for GIS practice
  - Use Broad Habitat-aligned outputs for policy-informed analyses while leveraging 1 km aggregates for large-scale modelling.
  Use the 0.5 ha MMU and boundary-informed classification to improve change detection accuracy.
  Inspect KBEs via vector metadata to understand classification decisions and conduct targeted reclassification if needed.
  Combine with other GIS data (e.g., CORINE, LUCAS, soil/climate layers) for richer habitat/network analyses.

- Change detection, interpretation, and future monitoring
  - Change detection is valuable but complex due to differing spatial/thematic structures among CEH maps; direct one-to-one change mapping is challenging.
  - A practical path: reorganise earlier CEH maps into a common real-world spatial framework and use aggregated classes or trajectory analyses to infer change trends.
  - The generalised, static spatial framework of LCM2007 provides a robust basis for repeat mapping and future monitoring.

- Broad Habitat Association (BHA) framework (summary)
  - Connects spectral classes to CS Broad Habitats, addressing ecological continua and mosaic contexts.
  - Rules link Montane, Bog, Dwarf Shrub Heath, and other habitats with their CS counterparts to improve cross-product interpretation.
  - Recognises non-reciprocal mappings in some edge cases (e.g., Built-up Areas vs grassland/woodland within urban boundaries).

- Limitations and caveats
  - Spectral confusion and temporal range can affect class boundaries (e.g., arable vs temporary grass; fen misclassification by spectral signatures).
  - Boundary and linear features often fall below MMU and may be merged into adjacent polygons in LCM2007.
  - Some habitat classes (e.g., Fen, Marsh and Swamp) show substantial area discrepancies with CS due to mosaic composition and patch size.

- Appendices: notable elements
  - Bespoke validation approach emphasizes parcel-level QA and the use of high-resolution imagery to validate LCM2007 at relevant locations.
  - Appendix outlines detailed KBEs, BH sub-classes, and extensive metadata design, illustrating how classification decisions are tracked and audited.

- Takeaway for GIS practitioners
  - LCM2007 provides UK-wide, map-based land cover aligned with Broad Habitats, with robust multi-scale data products and rich provenance metadata.
  - It supports policy-relevant spatial analysis, change monitoring, and integration with other environmental data, while acknowledging class-specific uncertainties and cross-product differences.