# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a parcel-based UK land cover classification using 23 classes aligned to UK Biodiversity Action Plan Broad Habitats.
- Created from summer-winter satellite composites at 20–30 m resolution; updates LCM2000 with improved spatial framework (OSMM/Large-scale Vector) for better GIS compatibility.
- Purpose: support diverse LCM user needs with a range of data products; maps land cover (not land use).

## Data Products

- Vector Data Set
  - Approximately 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Each polygon has 10 attributes including Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (display class), KBE (knowledge-based enhancements), ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, Construct.
  - Unique Parcel_ID retained for unambiguous communication; includes source image and processing history.
  - 23 LCM2007 classes derived from Broad Habitats; some subclasses exist (e.g., Urban vs Suburban, Heather vs Heather grassland).
- Raster Data Sets
  - 25 m and 1 km raster products derived from the vector data.
  - Great Britain and Northern Ireland provided separately due to different projections.
  - 1 km rasters show Dominant cover, Percentage cover for LCM2007 classes and Aggregate classes.
  - 25 m rasters provide full 23-class detail; 1 km rasters use Aggregate class mappings for broader-scale applications.

## Classification and Classes

- 23 LCM2007 classes based on Broad Habitats; some Broad Habitats subdivided for spectral distinctions:
  - Subdivisions include Built-up Areas and Gardens (Urban and Suburban), Dwarf Shrub Heath (Heather vs Heather grassland), Littoral Sediment (Saltmarsh) and related coastal distinctions.
- Class relationships and crosswalks:
  - Appendix 2 provides the mapping between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses.
  - Table 2 shows how aggregate (1 km) classes relate to LCM2007 classes, used for 1 km raster products.
- Attributes and labelling:
  - Parcel_ID identifies each polygon; BH denotes dominant Broad Habitat; BHSub provides sub-class description; FieldCode is a short field-code descriptor.
  - INTCODE is the recommended display class (1–23) for communication and QA.
  - ProbList lists the top five spectral-class matches for each polygon; users should validate at subclass level if used.
  - KBE captures the processing history and applied enhancements.

## Data Quality and Validation

- Ground reference validation used 9,127 polygons; average thematic accuracy around 83%.
- Local discrepancies may occur; accuracy figures reflect an average of higher and lower local performance.
- Broad Habitat subclasses (BHSub) are provided but not validated to the same QA level as LCM2007 classes; use caution and perform your own validation if using subclass information.

## Spatial and Technical Details

- Map projections:
  - Great Britain: British National Grid (OSGB 1936)
  - Northern Ireland: Irish National Grid (with NI transitioning to Ireland Transverse Mercator in some workflows)
- MMU and data resolution:
  - Minimum mappable unit: > 0.5 ha; parcels < 0.5 ha and linear features < 20 m dissolved into surrounding landscape.
- File sizes (guidance):
  - Vector (GB 100 km x 100 km shapefiles): ~4.13 GB
  - Vector (NI 100 km x 100 km shapefiles): ~433 MB
  - Raster 25 m:
    - GB: ~1.36 GB
    - NI: ~46 MB
  - 1 km data: dominant cover and percentage cover products range from ~21 MB to ~49 KB
- Data access:
  - 1 km raster data available via CEH Information Gateway.
  - Full vector and 25 m raster products available on request from CEH; licensing may apply.
  - Application process and contact: CEH data portal or spatialdata@ceh.ac.uk.

## Access, Licensing and Information Resources

- Final report and detailed methodology: Morton et al., 2011 (Final Report for LCM2007).
- Broad Habitat crosswalk guidance: Jackson, 2000 (JNCC Report 307).
- Acknowledgements cover satellite, cartographic, soil, and other data sources; CEH hosts and distributes LCM2007 data.

## Appendix Highlights

- Appendix 1: LCM2007 Classes
  - Provides descriptive notes for each of the 23 classes (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Neutral/Calcareous/Acid Grassland, Fen/Marsh/Swamp, Bog, Montane Habitats, Inland Rock, Urban, Suburban, etc.).
  - Details sensitivities, field-level distinctions, and common classification caveats (e.g., grassland misclassifications, peat depth considerations, Montane vs vegetation-based definitions).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes and Broad Habitat subclasses
  - Provides mappings between Broad Habitat categories, LCM2007 classes, and FieldCode/sub-class designations.
- Appendix 3: Colour mapping (as used in the Final Report)
  - Standard RGB triplets for each LCM2007 class to support visualization and QA, including examples for Broadleaved woodland, Coniferous woodland, Arable and Horticulture, and others.

## Usage Considerations and Best Practices

- LCM2007 maps land cover, not necessarily land use; interpret many classes with caution where land use cannot be inferred from spectral data alone.
- Use 1 km raster products for UK-scale modelling or when integrating with other large-scale datasets (e.g., meteorological or species distribution data).
- For applications requiring detailed class information, prefer vector or 25 m raster products, while acknowledging larger file sizes and metadata overhead.
- Retain Parcel_ID and other metadata for traceability and reproducibility; validate Broad Habitat subclasses if used for downstream analyses.

## Acknowledgements

- Datasets derived from Landsat-TM5, SPOT, AWIFS and other satellite data; cartographic data from Ordnance Survey and other agencies; provenance and rights maintained as described.
- Publication and data distribution via CEH and the Countryside Survey Partnership.