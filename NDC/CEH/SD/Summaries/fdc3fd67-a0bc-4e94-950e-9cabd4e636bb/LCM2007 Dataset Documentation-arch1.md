# Land Cover Map 2007 Dataset Documentation

- A parcel-based classification of UK land cover using 23 classes aligned with UK Biodiversity Action Plan Broad Habitats.
- Uses 20–30 m resolution satellite imagery to map land cover (not land use); updated from LCM2000 with a more GIS-friendly, object-based framework.
- Provides a range of data products (vector and raster) to support diverse applications and users.

## Data Products and Resolutions

- Vector Data Set
  - 8.6 million polygons for Great Britain; 0.9 million for Northern Ireland
  - 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels)
  - Contains unique Parcel_ID labels for unambiguous communication
  - Rich metadata including processing history and top 5 spectral class probabilities (ProbList)
- Raster Data Sets
  - 25 m raster: 23 LCM2007 classes
  - 1 km raster: aggregates for UK-wide modelling (dominant class and percentage cover)
  - GB and NI provided separately with respective projections
- Example data formats
  - Vector products are detailed but larger; 25 m rasters provide similar detail with less metadata
  - 1 km rasters summarized from 25 m data (dominant and percentage cover)

## Class Structure and Relationships

- 23 LCM2007 classes based on Broad Habitats; some subdivisions exist (e.g., Suburban vs Urban, Heather vs Heather grassland, Littoral sediment vs Saltmarsh)
- Appendix 2 details relationships between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses
- Appendix 3 provides standard colour mapping for display of classes
- Users encouraged to perform their own validation when using Broad Habitat subclasses, as QA is at the 23-class level

## Key Classification Details

- Minimum mappable area: >0.5 ha; parcels smaller than 0.5 ha and linear features under 20 m are dissolved into surrounding landscape
- Data derived from summer-winter composite images; OS MasterMap for GB and Land & Property Services vector data for NI to build polygons
- Class labels include a unique FieldCode with descriptive BHSub subclass, enabling detailed interpretation
- Ground reference validation: 9,127 polygons tested; average accuracy around 83% (local variations possible)

## Data Access and Licensing

- 1 km raster data: available via the CEH Information Gateway
- Full vector product and 25 m raster product: available on request under license from CEH (licence fees may apply)
- Contact: spatialdata@ceh.ac.uk or CEH data portal for access details

## Projections and Geography

- Great Britain: British National Grid (OSGB 1936)
- Northern Ireland: Irish National Grid (moving toward Ireland Transverse Mercator)
- Users may reproject NI data to ITM as needed

## File Size and Storage

- Vector (100 km x 100 km shapefile example)
  - GB: ~4.13 GB
  - NI: ~433 MB
- Raster 25 m
  - GB: ~1.36 GB
  - NI: ~46 MB
- 1 km rasters (various products)
  - Ranging from ~21 MB to ~49 KB depending on product
- Note: Large file sizes reflect ~10 million polygons with 10 attributes each

## Usage Considerations for Analysis

- Data maps land cover, not land use; interpretation requires context for each class
- The 23-class resolution provides detailed land-cover distinctions; aggregated 1 km rasters enable UK-wide analysis
- Broad Habitat sub-classes can offer additional signals but may require local validation due to QA differences
- Parcel_ID and detailed metadata support reproducibility and data provenance in analyses and modelling

## Appendices (Reference)

- Appendix 1: LCM2007 Classes (descriptions and examples)
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes, and Broad Habitat subclasses
- Appendix 3: Colour mapping recipe used in the Final Report

## Further Information and References

- Morton et al., Final Report for LCM2007 – the new UK Land Cover Map (2011)
- Jackson, D.L., Guidance on the interpretation of Biodiversity Broad Habitat Classification (JNCC, 2000)
- Acknowledgements for satellite imagery sources and data providers