# Land Cover Map 2007 Dataset Documentation

## Overview
- Parcel-based UK land cover classification using 23 classes aligned with UK Biodiversity Action Plan Broad Habitats.
- Built from satellite imagery (20–30 m pixels) with a spatial framework enhanced by OS MasterMap and related vector data.
- Maps land cover (not strictly land use); minimum mappable area is >0.5 ha; small parcels and very short linear features are dissolved.
- Data products span vector and raster formats to support diverse applications; recommended to consult the Final Report for comprehensive methodology and limitations (Morton et al., 2011).

## Data Products and Structure
- LCM2007 products support a range of thematic and spatial resolutions to suit different uses.
- Vector Data Set:
  - Approximately 8.6 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Each polygon has 10 attributes, including Parcel_ID, Broad Habitat (BH), Broad Habitat sub-class (BHSub), FieldCode, INTCODE, KBE (processing history), ProbList (top five spectral classes), CorePixels, Construct, TotPixels.
  - Unique Parcel_ID aids communication and data tracking.
  - Contains Broad Habitat sub-classes and FieldCodes primarily for display and in-probability listings; use of subclass details requires independent validation.
  - Validation: ground-reference data yield average accuracy around 83% (subject to local variation).
- Raster Data Sets:
  - 25 m and 1 km products derived from the vector data.
  - Great Britain and Northern Ireland provided in separate projections (GB: British National Grid; NI: Irish National Grid).
  - 23-class 25 m raster; 1 km rasters provide dominant class and percentage cover (both for 23 classes and for aggregated classes).
  - 1 km products suitable for national-scale modelling and integration with other datasets (e.g., meteorology, species distribution).

## Classification and Metadata
- LCM2007 classes are tied to Broad Habitats; some Broad Habitats have sub-classes to enhance detail (not all sub-classes are QA-validated).
- Appendix 1 lists the 23 LCM2007 classes with descriptive notes.
- Appendix 2 provides the relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode mappings).
- Appendix 3 documents the standard colour mapping used in the Final Report (Morton et al., 2011).

## Data Access and Licensing
- Data Access:
  - 1 km raster data available via the CEH Information Gateway.
  - Full vector product (and 25 m raster product) available on request under licence from CEH; some applications may incur licence fees.
- Licensing considerations: clarify terms with CEH when applying for access; data usage subject to permissions.

## Technical Details
- Coordinate Systems and Projections:
  - GB data: British National Grid (OSGB 1936).
  - NI data: Irish National Grid (moving toward Ireland Transverse Mercator ITM).
- File sizes (illustrative guidance):
  - Vector (shapefile, 100 km x 100 km): GB ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: sizes range from tens of MB to a few tens of KB depending on product.
- Scale and QA:
  - Data are validated at 23-class thematic resolution.
  - Sub-class information (BHSub, FieldCode) exists but is not as rigorously QA’d as the main LCM2007 classes; users should perform their own validation for sub-class usage.
- Data quality caveats:
  - Grassland, wetland, and some habitat boundaries can be difficult to separate spectrally; certain grassland classifications (Neutral/Calcareous) may be mis-classified as Improved Grassland in some instances.
  - Montane and coastal classifications rely on combinations of altitude, spectral data, and soil/terrain context; consider these nuances in analyses.

## End-User Guidance for Data Leaders
- Leverage the 23-class LCM2007 vector and raster products to support broad-scale data governance, planning, and environmental reporting.
- Use the 1 km rasters for national-scale analyses and when integrating with other large-scale datasets; use 25 m rasters for finer detail with richer metadata (at the cost of larger file sizes).
- Prioritize the QA’d INTCODE (display) class for consistent reporting, while validating Broad Habitat sub-classes if used for policy or stakeholder communications.
- Plan for data access logistics and licensing with CEH; anticipate substantial storage needs for vector data and 25 m rasters.
- Incorporate Final Report (Morton et al., 2011) and Appendix materials to understand class definitions, cross-walks to Broad Habitats, and color mappings; conduct local validation for sub-class usage and any aggregated analyses.

## Appendices ( Highlights )
- Appendix 1: LCM2007 Classes – detailed definitions and note on Broad Habitat interpretations.
- Appendix 2: Crosswalk between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCode mappings).
- Appendix 3: Colour mapping for LCM2007 classes (as used in official outputs).

## Acknowledgements and Copyright
- Acknowledges data sources (Landsat, SPOT, AVNIR, Cartographic data, elevation, soils, etc.) and OS licensing.
- Reproduced with permissions from organisations; subject to Crown Copyright and related rights.
- Publication: © NERC (CEH) 2011; dataset releases tied to Countryside Survey partnership and CEH data portals.