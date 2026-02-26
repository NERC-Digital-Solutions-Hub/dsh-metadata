Land Cover Map 2007 Dataset Documentation

- Purpose and scope
  - Parcel-based UK land cover classification (23 classes) aligned with UK Biodiversity Action Plan Broad Habitats.
  - Maps land cover (not strictly land use) from summer-winter satellite composites (20–30 m pixels).
  - Updates LCM2000 with a framework based on OS MasterMap/Large-scale Vector and image segmentation for object-based polygons.
  - Recommends consulting the Final Report for full methodology and limitations (Morton et al., 2011).

- Data products and structure
  - Vector data set
    - 8.6 million polygons (Great Britain) and 0.9 million (Northern Ireland).
    - Each polygon has 10 attributes (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
    - Contains unique Parcel_ID for unambiguous communication; BHSub provides Broad Habitat subclass; FieldCode is a non-validated code; INTCODE is a display-friendly class code (1–23).
    - Heavy files; 100 km x 100 km shapefile examples: GB ~4.13 GB; NI ~433 MB.
  - Raster data sets
    - 25 m and 1 km resolutions derived from the vector data.
    - 23-class 25 m raster; 1 km rasters provide dominant class, and percentage cover for both 23 classes and Aggregate classes.
    - Northern Ireland and Great Britain provided in separate projections.
  - Aggregation
    - 1 km rasters use Aggregate classes (merged LCM2007 classes) for broad-scale analyses.
  - Colour mapping (Appendix 3)
    - Standard RGB values mapped to each LCM2007 class (used in Final Report).

- Classification system and metadata
  - 23 LCM2007 classes based on Broad Habitats; some Broad Habitats are subdivided (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland).
  - Appendix 2 details relationships between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses.
  - Rich metadata for vectors:
    - Processing history, source images, KBE history, and a ProbList showing the top 5 spectral class matches per polygon.
  - Accuracy and validation
    - Ground reference validation against 9127 polygons; average accuracy ~83% (noting local variation).
    - QA validates LCM2007 at the 23-class level; Broad Habitat subclasses are not QA-validated and should be used with caution.

- Data quality, limitations, and considerations
  - LCM2007 maps land cover rather than land use; interpretation should consider spectral similarities and context.
  - Minimum mapping unit (MMU) > 0.5 ha; parcels < 0.5 ha or lines < 20 m dissolved into surrounding landscape.
  - Some grassland, bog, and other habitats may be misclassified relative to ground truth; users needing sub-class distinctions should perform their own validation.
  - Broad Habitat subclasses (BHSub) provide additional context but are not consistently guaranteed in terms of accuracy.

- Access, licensing, and distribution
  - 1 km raster products accessible via CEH Information Gateway (gateway.ceh.ac.uk).
  - Full vector product and 25 m raster product available under licence on request from CEH; licensing fees may apply.
  - Route to access: online CEH data portal or direct contact to spatialdata@ceh.ac.uk.

- Technical specifications
  - Projections and coordinate systems
    - Great Britain: British National Grid (OSGB 1936).
    - Northern Ireland: Irish National Grid (Ireland 1965); NI moving toward ITM (conversion supported in GIS workflows).
  - Spatial resolution and extent
    - Vector: polygon-based, 10 attributes per polygon; 23 LCM2007 classes with additional BHSub and FieldCode data.
    - Raster: 25 m and 1 km products; GB and NI datasets with appropriate projections.
  - Data size considerations
    - Vector datasets are large; plan storage and processing accordingly.
    - Raster datasets offer more manageable options for certain applications, with 1 km products suitable for national-scale analyses.

- Practical guidance for data leaders
  - Assess data operability within your data system: format, metadata richness, and linkage to other datasets (e.g., habitat classifications, environmental layers).
  - Leverage metadata and Parcel_ID for traceability and communication across teams and partners.
  - Consider data access constraints and licensing when budgeting for data costs and governance.
  - Use 1 km raster products for broad national modelling and 25 m/Vector data for detailed site-level work, with QA validation for sub-class analyses.
  - Be mindful of MMU and potential misclassifications; plan validation steps if precise grassland or peatland distinctions are critical.
  - Reference the Final Report (Morton et al., 2011) for methodology, limitations, and a detailed description of Broad Habitat classifications.

- Appendices and further information
  - Appendix 1: LCM2007 class descriptions and interpretive notes for Broad Habitats.
  - Appendix 2: Relationship mapping between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Appendix 3: Colour mapping recipe for standard LCM2007 visualization.
  - Further information: Morton et al. 2011 Final Report; Jackson 2000 guidance on Broad Habitat classifications; and Countryside Survey context.

- References and acknowledgments
  - Data derived from Landsat, SPOT, AWIFS and other imagery sources; extensive attribution to Ordnance Survey, CEH, and partner organisations.
  - Copyright and licensing notes across agencies; Crown Copyright and OS datasets referenced.