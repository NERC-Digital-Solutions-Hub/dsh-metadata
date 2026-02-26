Land Cover Map 2007 Dataset documentation

- Purpose and scope
  - Parcel-based classification of UK land cover using 23 classes based on UK Broad Habitats.
  - Maps land cover (not land use) at 20–30 m resolution; aims to support environmental monitoring and policy analysis.
  - Minimum mappable unit: 0.5 ha; parcels smaller than 0.5 ha or lines shorter than 20 m are dissolved into the surrounding landscape.
  - Version notes: LCM2007 updates from LCM2000 with a framework aligned to OS mapping layers and image segments; final report Morton et al. 2011 provides comprehensive production methodology and limitations.

- Data products and structure
  - Vector Data Set
    - ~8.6 million polygons for GB; ~0.9 million for NI.
    - 10 attributes per polygon, including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (LCM2007 class number 1–23), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, and Construct history.
    - Parcel_ID provides a unique label per parcel; recommended to retain for communication.
    - Rich metadata on polygon construction, spectral classification, and KBE history; Broad Habitat sub-classes are included primarily for ProbList and display but are not as robust as main LCM2007 classes.
    - 25 m raster and 1 km raster products derived from the vector data.

  - Raster Data Sets
    - 25 m raster: 23 LCM2007 classes; GB and NI provided separately with appropriate projections.
    - 1 km raster: aggregates of the 25 m data; includes:
      - Dominant cover at 1 km (for LCM2007 classes and for Aggregate classes)
      - Percentage cover at 1 km (for LCM2007 classes and Aggregate classes)
    - Spatial resolution and extent designed to support national-scale modelling and integration with other datasets (e.g., meteorology, species distributions).

- Classes, relationships, and mapping
  - LCM2007 uses 23 classes tied to Broad Habitats; some classes are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Saltmarsh and other coastal sediments).
  - Appendix 2 outlines relationship between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses.
  - Appendix 3 provides colour mapping (for visualization) according to LCM2007 class numbers.

- Quality, validation, and limitations
  - Ground reference validation: average accuracy around 83% against reference polygons (9127 polygons); local accuracy can vary.
  - LCM2007 maps land cover, not land use; some spectral signatures may not uniquely resolve certain habitat types.
  - Sub-class level (Broad Habitat sub-classes) should be used with caution and validated independently if used for analysis beyond the main LCM2007 classes.
  - KBE and ProbList provide a processing history and spectral alternatives; users should validate field-level interpretations when using sub-classes or probabilities.

- Data access, licensing, and sizes
  - 1 km raster data are accessible via the CEH Information Gateway.
  - Full vector product and 25 m raster product are available on request under licence; fees may apply.
  - Example file sizes (indicative):
    - Vector 100 km x 100 km shapefile (GB): ~4.13 GB; NI: ~433 MB.
    - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
    - 1 km products: 21 MB to 49 KB (depending on product type).
  - Projections: GB products use British National Grid; NI products use Irish National Grid (with NI transitioning toward ITM in the future).
  - Data is large and best suited for environments with robust GIS capabilities.

- Practical considerations for analysts monitoring the environment
  - Use LCM2007 to support standardized, auditable assessments of environmental condition over time; align with the Final Report (Morton et al., 2011) for detailed methodology and limitations.
  - Suitable for integration with other datasets, keeping in mind the MMU and the difference between land cover and land use.
  - For national-scale modelling, 1 km raster aggregates offer compact data with percentage/dominant class outputs; for detailed local analyses, 25 m vector or raster data provide higher thematic detail but larger file sizes.
  - Retain Parcel_ID and metadata to ensure traceability of classifications and to facilitate communication among stakeholders.

- Appendix highlights (high-level)
  - Appendix 1: LCM2007 23 classes with brief habitat descriptions and how they are distinguished spectrally.
  - Appendix 2: Detailed mapping relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Appendix 3: Standard colour mapping for visualization of LCM2007 classes.

- References and further information
  - Morton et al. 2011: Final Report for LCM2007 – the new UK Land Cover Map (Countryside Survey Technical Report No. 11/07).
  - Jackson 2000: Guidance on interpretation of the Biodiversity Broad Habitat Classification.
  - Acknowledgements note dataset sources (Landsat, SPOT, AWIFS, OS data, etc.) and copyright/license information.