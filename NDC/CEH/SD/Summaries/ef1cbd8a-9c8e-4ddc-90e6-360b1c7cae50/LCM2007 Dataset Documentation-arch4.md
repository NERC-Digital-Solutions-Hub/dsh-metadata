# Land Cover Map 2007 Dataset Documentation

- Overview and purpose
  - Parcel-based classification of UK land cover using 23 classes based on UK Biodiversity Action Plan Broad Habitats.
  - Based on summer-winter composite satellite imagery with 20–30m pixels.
  - Upgrades LCM2000; aligns with OS cartographic frameworks for GB and NI.
  - Maps land cover (not strictly land use); minimum mappable unit >0.5 ha; parcels <0.5 ha or lines dissolved into surroundings.
  - Aimed at supporting diverse data users with rich metadata and traceable data lineage; consult the Final Report for comprehensive assessment.

- Data products and structure
  - Vector Data Set
    - 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
    - 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
    - Parcel_ID provides unique communication key; BH/Sub-classes offer hierarchical classification.
    - KBE (Knowledge-Based Enhancements) records processing history and reclassifications.
    - ProbList lists top 5 spectral class candidates for each polygon.
  - Raster Data Sets
    - 25m and 1km resolutions; Great Britain and Northern Ireland provided in separate projections.
    - 25m rasters carry 23 LCM2007 classes; 1km rasters provide dominant and percentage cover for both LCM2007 classes and aggregates.
    - File characteristics summarized in Table 3 (extents, pixel sizes, data types, coordinate systems, and projections).
  - Classifications and mapping
    - 23 LCM2007 classes derived from Broad Habitats; some Broad Habitats subdivided (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland).
    - Appendix 1 lists LCM2007 class definitions; Appendix 2 describes crosswalk between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
    - Appendix 3 outlines standard LCM2007 colour mapping for visualization.

- Data quality, validation, and limitations
  - Ground-reference validation against 9127 polygons; average accuracy around 83%; local discrepancies possible.
  - Broad Habitat sub-classes (BHSub) may be less robust than primary LCM2007 classes; users should validate before using sub-class level data.
  - Grassland and certain habitat boundaries (e.g., Neutral vs Calcareous vs Acid Grassland) can be challenging; guidance provided in Morton et al. Final Report (2011) and Jackson (2000) notes.
  - LCM2007 is designed to be used at its highest thematic resolution (23 classes) but also supports aggregated 1km products for broader-scale applications.

- Data formats, scale, and spatial details
  - Vector: polygon-based with detailed metadata; 10 attributes per polygon; high data granularity.
  - Raster: 25m and 1km products; 1km products include dominant class and percentage cover; supports UK-wide modelling when aggregating.
  - Spatial coverage: GB and NI separately; GB uses British National Grid; NI uses Irish National Grid (with NI transitioning to ITM in the future).
  - Minimum mapping unit: 0.5 ha; smaller parcels dissolved to surrounding landscape.
  - Data size considerations: vector data ≈ GB 4.13 GB (GB shapefile), NI ≈ 433 MB; 25m rasters GB ≈ 1.36 GB, NI ≈ 46 MB; 1km rasters range 21 MB to 49 KB.

- Access, licensing, and usage
  - 1km raster data accessible via the CEH Information Gateway.
  - Full vector product and 25m raster product available on request under licence; online CEH data portal application process; licensing fees may apply.
  - Usage guidance encourages consulting Morton et al. (2011) Final Report for detailed methodology, metadata, and limitations.
  - Data provenance includes imagery sources (Landsat, SPOT, AWIFS, etc.) and cartographic data from Ordnance Survey and partner organisations.

- Practical guidance for Data Leaders
  - Consider data system-wide: LCM2007 provides a rich, object-based spatial dataset with extensive metadata that supports traceability and re-use across partners.
  - Maintain Parcel_ID and other metadata for clear communication and interoperability; leverage KBE history for understanding polygon edits.
  - Use 1km rasters for broad-scale analyses and 25m/Vector products for detailed, site-specific work; validate Broad Habitat sub-classes when high accuracy is required.
  - Be aware of access barriers and licensing where applicable; plan data governance and access rights accordingly.
  - Reference frameworks: Final Report for LCM2007 (Morton et al., 2011) and the JNCC Broad Habitat classification guidance (Jackson, 2000) for interpretation and cross-walks.

- Further information and references
  - Morton, D. et al. (2011) Final Report for LCM2007 – the new UK Land Cover Map; Countryside Survey Technical Report No. 11/07.
  - Jackson, D.L. (2000) Guidance on interpretation of Biodiversity Broad Habitat Classification.
  - Data access via CEH gateway and CEH data portal; contact spatialdata@ceh.ac.uk for licensing details.
  - Acknowledgements to data sources (Landsat, SPOT, AWIFS, Ordnance Survey, etc.) and partner organisations.

- Summary of key considerations for implementation
  - Choose the appropriate data product (vector, 25m, or 1km rasters) based on application scale and metadata needs.
  - Use the 23-class LCM2007 schema as the primary thematic resolution; aggregate when necessary for coarser analyses.
  - Validate Broad Habitat sub-classes for critical decisions; rely primarily on INTCODE and QA-validated classes for display and decision-making.
  - Consider the geographic projection differences and ensure reprojection is handled correctly for NI and GB datasets.