LAND COVER MAP 2007 DATASET DOCUMENTATION

- Overview
  - UK-wide parcel-based land cover classification (LCM2007) using 23 Broad Habitat-based classes.
  - Based on summer-winter satellite composites at 20–30 m resolution; updates LCM2000 with a framework tied to generalised digital cartography (OSMM/large-scale vector) and segmentation.
  - Maps land cover (not strictly land use) and uses minimum mappable unit of >0.5 ha; parcels smaller than 0.5 ha or linear features <20 m are dissolved into surrounding areas.
  - Notable caveat: Broad Habitats may not map all fine-scale differences; LCM2007 classes are the primary, thematically validated product.

- Data products and structure
  - Vector data set
    - ~8.6 million polygons for Great Britain and ~0.9 million for Northern Ireland.
    - 10 attributes per polygon, including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE, KBE (Knowledge-Based Enhancements), ProbList (top 5 spectral class probabilities), CorePixels, Construct, TotPixels.
    - Parcel_ID provides a unique parcel identifier; BHSub and FieldCode provide sub-class detail; INTCODE is the recommended display class aligned with QA.
    - KBE records processing history; ProbList lists top spectral matches (with probabilities); Sub-classes included mainly for auxiliary analysis and validation.
  - Raster data sets
    - 25 m and 1 km products derived from the vector data; separate data sets for Great Britain and Northern Ireland.
    - 23-class 25 m raster; 1 km raster products aggregate to Dominant or Percentage cover for both 23 classes and Aggregate classes (for 1 km).
  - Data formats and attributes
    - 25 m raster values correspond to LCM2007 class numbers; 1 km rasters summarize percentage/dominant cover by class/aggregate.
    - The relation between Broad Habitat, LCM2007 class, and sub-classes is documented (Table 2 and Appendix 2).

- Classifications and interpretation
  - LCM2007 classes (23 total) map to Broad Habitats (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Semi-natural grassland, Montane Habitats, Inland Rock, Urban, Saltmarsh, etc.).
  - Some Broad Habitats are further subdivided (e.g., Built-up Areas into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment split into Saltmarsh and Littoral sediment).
  - Users should validate Broad Habitat sub-classes if used beyond the primary LCM2007 class level, as sub-classes have not undergone the same QA rigor as main classes.

- Data quality and validation
  - Ground reference validation used to assess alignment with thematic resolution (9127 polygons); average accuracy ~83% across the dataset.
  - Local discrepancies may occur; the 83% figure is an average over the validation set.

- Data access and licensing
  - 1 km raster products are openly accessible via the CEH Information Gateway.
  - Full vector product and 25 m raster product are available under license on request from CEH (licensing fees may apply).
  - Access details: online application at CEH data site or contact spatialdata@ceh.ac.uk.
  - Data sizes are large (see File Size section); vector ~ GB-scale, rasters likewise substantial.

- Map projection and coordinates
  - Great Britain data: British National Grid (BNG), Transverse Mercator; NI data: Irish National Grid.
  - Northern Ireland transitioning towards ITM; software should reproject NI data as needed.

- File size and data footprint
  - Vector 100 km × 100 km (Shapefile): GB ~ 4.13 GB; NI ~ 433 MB.
  - Raster 25 m: GB ~ 1.36 GB; NI ~ 46 MB.
  - 1 km raster products: 21 MB to 49 KB (depending on product type).

- Specifics for use in monitoring frameworks
  - LCM2007 provides a standardized, large-scale land cover baseline aligned with UK Broad Habitat classifications, useful for policy scrutiny, trend analysis, and decision support.
  - Rich metadata per polygon (including processing history, KBE, and ProbList) supports data provenance, quality assessment, and reproducibility.
  - The 1 km raster products enable UK-wide modelling with reduced data complexity; the 25 m vector/raster products support finer-scale analyses but come with larger data volumes and more complex data management needs.
  - Important caveats for policy work: data maps land cover (not direct land use), requires careful interpretation of sub-classes, and users should consult Morton et al. 2011 Final Report for detailed methodology and validation nuances.

- Appendix highlights
  - Appendix 1: LCM2007 classes with descriptive notes for each Broad Habitat (e.g., Broadleaved woodland, Arable and Horticulture, Calcareous Grassland, Fen, Marsh and Swamp, Urban, Inland Rock, etc.).
  - Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (crosswalks linking class numbers to Broad Habitat sub-classes and FieldCodes).
  - Appendix 3: Standard LCM2007 colour mapping (RGB values by LCM2007 class) used in the final report for visual interpretation.

- Further information and references
  - Morton et al., 2011: Final Report for LCM2007 – the new UK Land Cover Map (Countryside Survey Technical Report No. 11/07).
  - Jackson, 2000: Guidance on interpretation of the Biodiversity Broad Habitat Classification (JNCC Report 307).

- Important cautions for monitoring use
  - LCM2007 maps land cover, not necessarily precise land use.
  - Meta- and KS-based enhancements (KBE) exist but may require user validation for certain sub-classes.
  - Data governance, metadata completeness, and up-to-date status are crucial for robust monitoring and should be actively managed when using LCM2007 outputs.