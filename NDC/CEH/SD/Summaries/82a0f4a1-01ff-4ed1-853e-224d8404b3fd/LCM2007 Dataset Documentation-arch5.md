# Land Cover Map 2007 Dataset Documentation

- Purpose and scope: Lands cover classification for the UK, based on 23 Broad Habitat classes aligned with UK Biodiversity Action Plan; maps land cover (not strictly land use) using 20–30 m resolution satellite imagery; intended to support diverse user needs and GIS interoperability.
- Version and provenance: Version 1.0, published 2011; builds on LCM2000 with an OS-based spatial framework and image-segmentation; metadata-rich with provenance and processing history.

## Data scope, products and classes

- Coverage and resolution:
  - Parceled vector data and raster products (25 m and 1 km) for Great Britain and Northern Ireland; different projections (GB: British National Grid; NI: Irish National Grid; NI moving toward ITM).
- Data products:
  - Vector Data Set: polygons with 10 attributes per polygon; ~8.6 million GB polygons and ~0.9 million NI polygons.
  - Raster Data Sets: 25 m and 1 km resolutions; 1 km products include dominant and percentage cover by class/aggregate class.
- Classes:
  - 23 LCM2007 classes derived from Broad Habitats; some Broad Habitats subdivided into sub-classes (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
  - MMU: minimum mappable unit of >0.5 ha; parcels <0.5 ha and linear features <20 m dissolved into surrounding landscape.
- Class labeling and compatibility:
  - Each vector parcel has a unique Parcel_ID; 10 core attributes include BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (display-friendly class number 1–23), KBE history, ProbList (top 5 spectral class probabilities), and pixel counts.
  - Crosswalks and appendices describe relationships between LCM2007 classes, Broad Habitats, and sub-classes; detailed color mappings provided for display.

## Data model, metadata and documentation

- Rich metadata:
  - Per-polygon metadata includes source images, construction history (OSMM/SEG-based), spectral classification, KBE history, and probability list.
  - Knowledge-based enhancements (KBE) record processing changes, aiding traceability.
- Unique identifiers:
  - Parcel_ID enables unambiguous communication; recommended to retain for data provenance and future developments.
- Documentation references:
  - Final Report Morton et al. (2011) and Jackson (2000) for Broad Habitat definitions and interpretation guidance; Appendix 2/3 provide class mappings and standardized colour schemes.

## Quality assurance, validation and caveats

- Validation:
  - Ground reference validation used 9,127 polygons; average thematic accuracy around 83%, with anticipated local variations.
- Sub-class caution:
  - Broad Habitat sub-classes and some FieldCode labels are not all covered by QA at the LCM2007 class level; users should perform their own validation when using sub-classes.
- Use recommendations:
  - LCM2007 maps land cover; caution when inferring land use from cover, and be aware of potential misclassifications in complex or heterogeneous areas.
- Limitations and interpretation:
  - Fen, Marsh and Swamp and some coastal/littoral classes can be spectrally ambiguous; mangement and soil data can aid interpretation but are not definitive for every polygon.

## Data access, licensing and rights

- Access channels:
  - 1 km raster data available via CEH Information Gateway.
  - Full vector product and 25 m raster product available under licence on request from CEH; licensing may incur fees.
- Data licensing:
  - CEH/UK Crown Copyright and third-party data licenses apply; usage rights described in the documentation.
- Usage guidance:
  - Data can be used standalone or in combination with other datasets; the 1 km rasters are convenient for national-scale modelling, while the 25 m/Vector forms offer higher detail with richer metadata.

## Data formats, projection, size and management

- File sizes (guidance):
  - Vector (GB): ~4.13 GB; Vector (NI): ~433 MB (as Shapefile subsets).
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - 1 km rasters: 21 MB to 49 KB depending on product (dominant vs. percentage estimates).
- Projections:
  - GB: British National Grid (Transverse Mercator); NI: Irish National Grid (with NI moving toward ITM).
- Data structure considerations for stewards:
  - Vector data includes 10 attributes per polygon; large files require careful storage planning, indexing, and processing workflows.
  - 25 m rasters include the same thematic detail in a coordinate-friendly raster format, with fewer metadata overhead than vector.

## Practical guidance for Data Stewards

- Governance and stewardship:
  - Maintain provenance by preserving Parcel_ID and KBE/ProbList history to support reproducibility and traceability.
  - Retain the full metadata for each polygon or ensure metadata access through data portals to support user needs and QA.
- Data quality and usage:
  - Use the QA guidance and final report to validate sub-classes if used beyond the primary LCM2007 class level.
  - Prefer 1 km rasters for broad-scale analyses; use 25 m vector or 25 m rasters when higher thematic detail is required and metadata can be leveraged.
- Interoperability and integration:
  - Leverage Appendix 2/3 crosswalks for integrating LCM2007 with Broad Habitats and display colour mappings.
  - Be mindful of differences between land cover mapping and land use interpretation; supplement with ancillary data when needed.
- Access and legal:
  - Confirm licensing terms with CEH for vector and 25 m raster products; plan for potential licensing fees and data access timelines.

## Appendices and references (high-level)

- Appendix 1: Detailed LCM2007 class descriptions and Broad Habitat relationships.
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
- Appendix 3: Standard LCM2007 colour mapping for display.
- Further information: Morton et al. 2011 Final Report; Jackson 2000 Guidance on Broad Habitat classification.
- Acknowledgements and data sources (Landsat, SPOT, AWIFS, Ordnance Survey, etc.).