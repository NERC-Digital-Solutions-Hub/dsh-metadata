# Land Cover Map 2007 Dataset Documentation

- Parcel-based UK land cover classification using 23 classes based on UK Biodiversity Action Plan Broad Habitats
- Created from 20–30 m satellite imagery; updates LCM2000; uses OS MasterMap/OSMM for GB and Large-scale Vector for NI; polygons correspond to real-world objects
- Maps land cover (not strictly land use); minimum mappable unit >0.5 ha; parcels <0.5 ha or linear features <20 m dissolved

## Introduction and Background
- LCM2007 provides a range of data products to support diverse user needs; consult final Morton et al. (2011) report for comprehensive assessment
- Designed to be compatible with other GIS data; used to upgrade LCM2000 with a more precise spatial framework
- 23 classes are aligned with Broad Habitats; some subclasses offer finer discrimination (e.g., Urban vs Suburban, Heather vs Heather grassland, Littoral sediment vs Saltmarsh)
- Validated against ground reference data: 9,127 polygons; average accuracy ~83% (local variability possible)

## LCM2007 Product Overview and Classes
- 23 LCM2007 classes derived from Broad Habitats; Appendix 1 lists class definitions
- Broad Habitat subclasses (BHSub) provide additional descriptors; used in probability lists (ProbList) but may require user validation for certain analyses
- Each parcel has a unique Parcel_ID (e.g., 11853977:c20); 10 attributes per polygon (Table 1)
- Attributes include: BH (Broad Habitat level), BHSub (sub-class), FieldCode, INTCODE (class code for display), KBE (knowledge-based enhancements), ProbList (top 5 spectral matches), CorePixels, TotPixels, Construct, etc.
- Appendix 2 maps Broad Habitats and LCM2007 classes to Broad Habitat sub-classes; Appendix 3 provides colour mapping for display

## Data Formats and Resolution
- Vector Data Set: polygons with attached metadata (8.6 million GB polygons; 0.9 million NI polygons); 10 attributes per polygon
- Raster Data Sets: derived from vector data; 25 m and 1 km resolutions
  - 25 m raster: 23 LCM2007 classes; pixel values correspond to LCM2007 classes (Table 2)
  - 1 km raster: aggregates by summarising 25 m data to produce
    - Dominant cover (per pixel) for LCM2007 classes
    - Dominant cover for Aggregate classes
    - Percentage cover for LCM2007 classes
    - Percentage cover for Aggregate classes
- Spatial extents are split GB and NI with separate products and projections

## Data Access and Usage
- 1 km raster data available via CEH Information Gateway (gateway.ceh.ac.uk)
- Full vector product and 25 m raster product licensed on request from CEH (data@ceh.ac.uk)
- Licences may apply; large file sizes reflect high thematic and attribute detail

## Map Projection and File Size
- GB vector data: British National Grid (OSGB 1936)
- NI vector data: Irish National Grid (Ireland 1965; NI moving toward ITM)
- 25 m raster: GB and NI in separate geographies; pixel size 25 m
- 1 km raster: GB and NI separate with 1,000 m pixels
- Typical file sizes (illustrative):
  - Vector (100 km x 100 km shapefile): GB ~4.13 GB; NI ~433 MB
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB
  - Raster 1 km: 21 MB to 49 KB (GB/NI mix depending on product)

## Validation and Quality
- Ground reference validation conducted; average accuracy of 83% across 9,127 polygons
- Accuracy is an average; local discrepancies may occur
- Broad Habitat subclass information (BHSub) can provide additional nuance but may require independent validation for high-accuracy subclass analysis

## Appendices (Key Details)
- Appendix 1: LCM2007 Classes — detailed descriptions of each Broad Habitat class (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Semi-natural grasslands, Wetlands, Montane/Habitat classes, Inland Rock, Coastal/Littoral classes, Built-up areas, etc.), including distinguishing notes, common misclassifications, and field considerations
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (BHSub) with FieldCode mappings
- Appendix 3: Standard LCM2007 colour mapping for display (class-specific RGB values)
- Acknowledgements: datasets from Landsat, SPOT, AWIFS, OS datasets, soils, elevation, and policy bodies; copyright and licensing notes

## Further Information
- Final Report for LCM2007: Morton et al. 2011 (Countryside Survey Technical Report No. 11/07)
- Broad Habitat Classification reference: Jackson 2000 (JNCC)
- Access details and contact information provided for licensing and data requests