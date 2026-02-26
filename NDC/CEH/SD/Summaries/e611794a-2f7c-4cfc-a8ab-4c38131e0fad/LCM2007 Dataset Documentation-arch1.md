# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) provides a range of data products to support diverse user needs, focusing on UK land cover with 23 classes based on Broad Habitats.
- Uses summer-winter composite satellite imagery at 20–30 m pixels; updates LCM2000 with a more object-based, GIS-friendly framework (OSMM in GB, L&PS in NI).
- Maps land cover (not land use) and applies a minimum mappable unit of >0.5 ha; parcels <0.5 ha or <20 m lines are dissolved into surrounding landscape.

## Introduction and Background

- LCM2007 is parcel-based, 23-class classification of the UK, aligned with UK Biodiversity Action Plan (BAP) Broad Habitats.
- Classifications are based on image spectra and refined with a generalised cartography framework and image segments.
- Distinguishes land cover from land use; several classes are subdivided for spectral reasons (e.g., Built-up Areas, Dwarf Shrub Heath, Littoral Sediment).
- Validated at the 23-class thematic resolution; ground-reference data yield an average accuracy of ~83% across 9,127 polygons, with local variation.

## LCM2007 Product Overview

- Provides multiple data formats and resolutions to support varied applications, including vector (polygons) and raster products at 25 m and 1 km.
- Raster products include 25 m and 1 km resolutions; GB and NI datasets are provided separately due to different projections.
- 1 km rasters summarize 25 m data by class percentage or dominant class per 1 km pixel; 25 m rasters retain full 23-class detail; vector data retain rich metadata per polygon.

## Example Datasets

- Vector vs 25 m raster vs 1 km raster offer trade-offs:
  - Vector: detailed polygons with extensive metadata; larger file sizes.
  - 25 m raster: same land cover detail without polygon boundaries or attached metadata; easier processing for some apps.
  - 1 km raster: suitable for national-scale modelling and for integration with other large-scale datasets (e.g., meteorology, species data).

## Vector Data Set

- GB: ~8.6 million polygons; NI: ~0.9 million polygons.
- Each polygon has 10 attributes including Parcel_ID, Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, INTCODE, KBE (processing history), ProbList (top 5 spectral matches), CorePixels, TotPixels, and Construct history.
- Parcel_ID provides a unique identifier for communication and traceability; BHSub offers additional detail but should be validated for accuracy.
- Includes a rich metadata trail for polygon construction, spectral classification, and knowledge-based enhancements (KBE).
- BHSub and FieldCode provide additional, non- QA-validated detail; users are advised to validate Broad Habitat sub-classes if used.

## Raster Data Sets

- 25 m raster: 23 LCM2007 classes; 25 m pixel values correspond to LCM2007 classes (per Class Table 2).
- 1 km raster: derived by summarising 25 m data to produce dominant class and percentage cover per 1 km pixel; also includes aggregate classes (based on merging 23 classes).
- Metadata specify dataset extents, resolutions, coordinate systems, and data types for GB and NI.

## Map Projection and Coordinate Details

- GB vector and raster data use the British National Grid (OSGB 1936).
- NI vector and raster data use the Irish National Grid (Ireland 1965).
- NI is transitioning toward the new Ireland Transverse Mercator (ITM); GIS software should reproject NI data as needed.

## File Size and Data Access

- Vector data (100 km x 100 km shapefile): GB ~4.13 GB; NI ~433 MB.
- Raster data (geotiff): 25 m GB ~1.36 GB; NI ~46 MB.
- 1 km rasters: smaller files; 21 MB to 49 KB depending on product.
- Data Access:
  - 1 km rasters available via CEH Information Gateway.
  - Full vector and 25 m products available on request under license from CEH; application via CEH website or contact.
  - Licensing fees may apply; some uses restricted.

## Further Information and Documentation

- Primary reference: Morton et al. 2011 Final Report for LCM2007; Countryside Survey Technical Report No. 11/07.
- For Broad Habitat classification details: Jackson 2000 guidance document (JNCC).
- Detailed mapping relationships (Appendix 2) and colour mappings (Appendix 3) accompany the dataset.

## Appendix 1: LCM2007 Classes (Overview)

- 23 Broad Habitat-based classes, with subdivisions where spectral data allow:
  - Broadleaved woodland; Coniferous woodland; Arable and Horticulture; Improved Grassland; Semi-natural grassland (Neutral, Calcareous, Acid); Fen/Marsh/Swamp; Bog; Montane Habitats; Inland Rock; Saltwater; Freshwater; Supra-littoral Rock; Supra-littoral Sediment; Littoral Rock; Littoral Sediment (Saltmarsh); Urban; Suburban.
- Some subdivisions include Heather vs Heather grassland; Urban vs Suburban; Salient distinctions such as Montane, Bog vs Dwarf Shrub Heath, etc.
- Grassland subclasses were refined with knowledge-based enhancement (KBE) rules; results may misclassify Neutral/Calcareous/Acid grasslands relative to Improved Grassland in some cases.

## Appendix 2: Relationship Between Broad Habitats, LCM2007 Classes and Sub-classes (Crosswalk)

- Provides mapping between Broad Habitats, LCM2007 class numbers, and Broad Habitat sub-classes (FieldCode) for the 23 LCM2007 classes.
- Includes notes on how sub-classes (BHSub) relate to broader habitat classifications and subsequent aggregation to LCM2007 classes.
- Helpful for interpreting sub-class information and for validating or aggregating classes according to project needs.

## Appendix 3: Colour Mapping (LCM2007 Colour Coding)

- Standard RGB mappings for each LCM2007 class are defined (e.g., Broadleaved Woodland: Red=255, Green=0, Blue=0; Coniferous Woodland: Red=0, Green=102, Blue=0; etc.).
- Used in the Final Report colour scheme to visualize classes consistently across products.

## Acknowledgements

- Data derived from Landsat-TM5, SPOT-4/5, AWIFS, and Ordnance Survey cartographic data, among others.
- Reproductions and permissions noted for Crown Copyright data and other datasets used in developing LCM2007 products.
- The publication is produced by CEH with input from the Countryside Survey Partnership.