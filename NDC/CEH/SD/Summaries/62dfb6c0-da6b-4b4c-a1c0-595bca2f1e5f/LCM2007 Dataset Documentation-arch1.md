# LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- Land Cover Map 2007 (LCM2007) is a parcel-based UK land cover classification using 23 classes aligned with UK Biodiversity Action Plan Broad Habitats.
- Created from summer-winter satellite imagery with 20–30 m pixels; updated from LCM2000 and integrated with OS MasterMap (GB) and L&S Large-scale Vector (NI).
- Maps land cover (not strictly land use) and uses a minimum mappable unit (>0.5 ha); parcels smaller than 0.5 ha or lines under 20 m are dissolved into surrounding areas.
- Some Broad Habitats are subdivided (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Littoral sediment/Saltmarsh).

## Data structure and content
- Each produced parcel has a unique Parcel_ID for clear communication.
- Rich metadata accompany each polygon, including processing history (KBE), and a probability list (ProbList) of the top five spectral matches.
- 10 attributes per polygon (Table 1 in the document) include: BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (display class, 1–23), KBE, ProbList, CorePixels, Construct, TotPixels, and related metadata.
- Sub-classes (BHSub) provide additional information but are not guaranteed to have the same QA level as LCM2007 classes; users should validate if using Sub-classes.

## Product formats and resolutions
- Vector data set
  - Polygons with attached attributes; GB ~8.6 million polygons; NI ~0.9 million.
  - 10 attributes per polygon (including Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
- Raster data sets
  - 25 m raster: 23 LCM2007 classes; GB and NI in separate projections.
  - 1 km raster: aggregates for GB/NI; provides dominant cover and percentage cover for both LCM2007 classes and their aggregates.
  - 1 km products are typically used for UK-scale modelling; 25 m and vector products offer greater detail with richer metadata.
- Data size (guidance)
  - Vector (100 km × 100 km shapefile): GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 21 MB to 49 KB depending on product.

## Classes and mapping
- LCM2007 uses 23 classes tied to Broad Habitats; some classes incorporate sub-class distinctions and detailed field codes.
- Appendix 1 outlines each Broad Habitat concept (e.g., Broadleaved woodland, Coniferous woodland, Arable, Various Grasslands, Wetlands, Coastal/Littoral types, Built-up, etc.).
- Appendix 2 describes relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (BHSub) with detailed crosswalks.
- Appendix 3 provides standard RGB colour mappings for visualization of each LCM2007 class.

## Validation and accuracy
- Ground reference data used to validate LCM2007 against polygons at the same spatial/thematic resolution.
- Validation against 9,127 ground reference polygons yielded an average accuracy of 83%.
- Local discrepancies can occur; Broad Habitat sub-classes may have lower or less consistent QA compared to the main LCM2007 classes.

## Data access and licensing
- 1 km raster data sets available via the CEH Information Gateway.
- Full vector product and 25 m raster product available on request from CEH; licensing may apply.
- Online application or contact: spatialdata@ceh.ac.uk.

## Projections and geographic coverage
- Great Britain vector and raster datasets: British National Grid (OSGB 1936-based).
- Northern Ireland datasets: Irish National Grid; NI is transitioning to Ireland Transverse Mercator (ITM) in some GIS environments.
- Data are designed to be compatible with other UK datasets using OS MasterMap/topographic frameworks.

## Methodology and caveats
- LC M2007 is produced from segmented image data and OS-based basemaps; polygons reflect real-world objects.
- The dataset is designed to support a wide range of applications, with a broad thematic resolution (23 classes) suitable for national to regional analyses.
- Important caveats:
  - LCM2007 maps land cover, not necessarily land use; spectral similarity can blur distinctions (e.g., grassland types).
  - MMU excludes small patches (<0.5 ha) and very small linear features.
  - Sub-class details (BHSub) require independent validation for rigorous use.
  - Grassland, bog, and other complex habitats can be misclassified or difficult to separate spectrally; cross-walks and field validation recommended for specialist analyses.

## Usage guidance and further information
- For a comprehensive description and assessment, consult the Final Report for LCM2007 (Morton et al., 2011).
- Broad Habitat crosswalks (Appendix 2) and colour mappings (Appendix 3) aid interpretation and visualization.
- The documentation emphasizes preserving Parcel_ID and the rich metadata to enable transparent communication among users and to facilitate downstream analyses.

## Acknowledgements and rights
- Acknowledges multiple satellite and cartography data sources; data are provided under Crown Copyright and other licences.
- Encourages appropriate attribution and compliance with data usage rights.