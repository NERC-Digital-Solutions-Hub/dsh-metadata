# Land Cover Map 2007 Dataset Documentation

## Overview
- UK parcel-based land cover classification using 23 classes based on Broad Habitats.
- Derived from summer-winter satellite composites at 20–30 m resolution.
- Vector products: polygons with rich metadata; raster products: 25 m and 1 km.
- Distinguishes land cover (not strictly land use); minimum mappable parcel size > 0.5 ha; small parcels and short linear features dissolve into surrounding landscape.
- Builds on LCM2000 with a spatial framework using OSMM in GB and Land & Property Services vector for NI; polygons correspond to real-world objects (fields, woodland blocks).

## Data structure and classes
- Vector Data Set
  - About 8.6 million polygons (GB) and 0.9 million (NI); 10 attributes per polygon.
  - Key attributes: Parcel_ID, BH (Broad Habitat), BHSub (Broad Habitat sub-class), FieldCode, INTCODE (recommended display class, 1–23), KBE (processing history), ProbList (top 5 spectral class probabilities), CorePixels, TotPixels, Construct.
  - Broad Habitat sub-classes (BHSub) provide additional detail but are not as rigorously QA’d as LCM2007 classes; used mainly for ProbList and potential validation.
  - Parcel_ID should be retained to maintain unambiguous communication among users.
  - 23 LCM2007 classes linked to Broad Habitats (see Appendix 2 for relationships).
- Raster Data Sets
  - 25 m and 1 km products derived from the vector data.
  - 1 km rasters: dominant cover by class and percentage cover by class; also available for Aggregate classes.
  - 25 m rasters: 23 LCM2007 classes; pixel values correspond to class mapping in Table 2.
- Class mapping
  - Appendix 1 provides detailed class descriptions.
  - Appendix 2 shows the relationship between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes.
  - Appendix 3 contains the standard colour mapping for display.

## Data formats, resolutions, and access
- Vector Data Set: polygon-based with extensive metadata for each polygon; 10 attributes per polygon.
- Raster Data Sets: 25 m (GB and NI, separate projections) and 1 km (GB and NI, separate projections).
- Projections
  - GB: British National Grid (OSGB36).
  - NI: Irish National Grid (to Ireland 1965) with NI gradually transitioning to ITM.
- File sizes (illustrative)
  - Vector (GB shapefile, 100 km x 100 km): ~4.13 GB; NI ~433 MB.
  - Raster 25 m: GB ~1.36 GB; NI ~46 MB.
  - Raster 1 km: 21 MB–49 KB depending on product (dominant vs. percentage).
- Data access
  - 1 km raster data via CEH Information Gateway.
  - Full vector and 25 m products licensed on request from CEH (online form or spacialdata@ceh.ac.uk). License fees may apply.

## Data quality and usage guidance
- Ground-reference validation
  - 9,127 ground reference polygons; average accuracy ~83% (variable across areas; local discrepancies possible).
- Data interpretation cautions
  - LCM2007 maps land cover, not always directly inferable land use.
  - Broad Habitat sub-classes (BHSub) are informative but not as robust as primary LCM2007 classes; use with validation if working at subclass level.
  - KBE history and ProbList provide processing history and spectral class probabilities; use for expert interpretation and validation.
- Recommended use
  - Use LCM2007 at its validated thematic resolution (23 classes) for analyses; aggregate into broader categories if necessary (via Table 2 mappings or Appendix 1/2 guidance).
  - For national-scale modelling, 1 km raster products are valuable; for detailed mapping and GIS integration, vector and 25 m raster provide richer detail but larger sizes.

## Practical considerations for GIS workflows
- Data richness vs. size
  - Vector provides rich metadata per polygon but larger file sizes and more complex processing; 25 m rasters offer the same land cover detail with less attribute data.
- Integration with GIS datasets
  - The generalised OS Master Map (GB) and NI vector data underpin polygon construction; segmentation ensures polygons map to real-world objects (fields, woodland blocks).
- Display and classification
  - Use INTCODE for display of the standard LCM2007 class; refer to Appendix 3 for colour mapping.
  - Retain Parcel_ID for traceability and communicating results across projects and teams.

## Potential uses by GIS Specialists
- Create map-based data products showing UK land cover distribution by Broad Habitat class.
- Analyze spatial patterns and fragmentation of habitats at 20–30 m resolution.
- Cross-walk LCM2007 classes to national habitat classifications or to ecological datasets (e.g., biodiversity considerations).
- Develop applications that combine 25 m raster detail with vector metadata for robust GIS analyses.
- Validate Broad Habitat subclass results independently when higher-resolution interpretation is required.

## Further information and references
- Morton, D., Rowland, C., Wood, C., et al. (2011). Final Report for LCM2007 – the new UK Land Cover Map. Countryside Survey Technical Report No. 11/07.
- Jackson, D.L. (2000). Guidance on the interpretation of Biodiversity Broad Habitat Classification (JNCC Report 307).
- For full methodological details and data descriptions, consult the Final Report and related appendices (Morton et al., 2011).