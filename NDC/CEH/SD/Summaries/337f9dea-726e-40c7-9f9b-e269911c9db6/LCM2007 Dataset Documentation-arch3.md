# LAND COVER MAP 2007 DATASET DOCUMENTATION

- Land Cover Map 2007 (LCM2007) is a parcel-based UK land cover classification using 23 classes aligned to UK Broad Habitats, derived from summer-winter satellite composites at 20–30 m pixels.
- It is an upgrade from LCM2000 with improved spatial framework (OSMM in GB, L&S Lands for NI) and segmentation, producing polygons that represent real-world objects (fields, woodland blocks) to improve GIS compatibility.
- LCM2007 maps land cover (not strictly land use) and applies a minimum mapping unit of greater than 0.5 ha; parcels smaller than 0.5 ha or lines under 20 m are dissolved into surrounding landscape.

- Final reference: Morton et al., 2011 (Final Report for LCM2007) recommended for comprehensive description; this document covers LCM2007 products only (not LCM2000 or LCM1990).

## Data products and overview

- Ellipse of products: vector (23 LCM2007 classes with metadata), 25 m raster, and 1 km raster products; GB and NI datasets provided with their respective projections.
- 23 LCM2007 classes are based on Broad Habitats; some are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- LCM2007 is validated at the thematic resolution of the 23 classes; higher-level use may require caution for sub-classes.

- Parcel_ID: unique identifier for each polygon, including the satellite image source; this should be retained for unambiguous communication.
- Rich metadata: polygon-level metadata includes processing lineage, knowledge-based enhancements (KBE), and a top-5 ProbList of spectral class candidates.
- Ground-reference validation: 9,127 polygons used for QA; average accuracy around 83%, with local variations.

## Vector Data Set details

- Structure: vector polygons with 10 attributes per polygon (e.g., Parcel_ID, BH, BHSub, FieldCode, INTCODE, KBE, ProbList, CorePixels, Construct, TotPixels).
- Attributes:
  - BH: Broad Habitat (dominant class at Broad Habitat level)
  - BHSub: Broad Habitat sub-class
  - FieldCode: short codes used in LCM2007 construction; not QA-validated
  - INTCODE: integer class code (1–23) recommended for display and QA
  - KBE: knowledge-based enhancements applied
  - ProbList: top 5 spectral-class probabilities
  - CorePixels / TotPixels: pixel counts used in classification
  - Construct: method of polygon construction (OSMM-derived, segmentation details)
- Data scale: approximately 10 million polygons (GB) and 0.9 million polygons (NI); 10 attributes per polygon.
- Sub-class data: BHSub and FieldCode present; use with caution and validate if sub-class level is necessary since QA coverage focuses on LCM2007 class level.

## Raster Data Sets

- 25 m raster: 23 LCM2007 classes; GB and NI have separate datasets with appropriate projections.
- 1 km raster: derived by summarizing the 25 m raster; provides dominance and percentage cover for both 23 classes and aggregated classes.
- Metadata: includes grid dimensions, geographic extents, pixel size, data type (Unsigned 8-bit), and projections (GB: OSGB36; NI: Ireland 1965/Irish National Grid, with NI transitioning to ITM).
- Data size and format: large vector and raster files; 1 km rasters are smaller and suitable for national-scale modelling.

## Projections, coverage, and data access

- Projections:
  - Great Britain: British National Grid (Transverse Mercator, OSGB36)
  - Northern Ireland: Irish National Grid (Transverse Mercator/transition to ITM)
- Northern Ireland is transitioning to the Ireland Transverse Mercator projection; GIS tools should reproject to required projection if needed.
- Data access:
  - 1 km raster data via CEH Information Gateway
  - Full vector product and 25 m raster product available on request; license may apply
  - Application process via CEH data portal or via SPATIALDATA contact

## Data sizes and management

- Vector: nearly 10 million polygons; 10 attributes per polygon; large file sizes.
  - Example sizes (for planning): Vector shapefile at 100 km x 100 km: GB ~ 4.13 GB; NI ~ 433 MB
  - Raster (25 m): GB ~ 1.36 GB; NI ~ 46 MB
  - Raster (1 km) products: range from 21 MB to 49 KB, depending on product type
- Metadata richness facilitates traceability, reproducibility, and governance.

## Quality, caveats, and usage guidance

- LCM2007 maps land cover (spectral-based) rather than direct land use; users should consider this distinction when interpreting results.
- Accuracy: overall average ~83% against ground reference data; individual polygons may deviate; cross-check against local ground-truth data when applying at fine scales or subclass level.
- Sub-class (BHSub) information is provided but not QA-standard; users should validate when using Broad Habitat sub-classes.
- The Suburban vs Urban distinction and other subclass efforts should be validated for specific use cases.
- The “ProbList” and KBE history are helpful for validation and traceability of classification decisions; users should verify uncertain classifications with local data.
- The Final Report Morton et al. (2011) should be consulted for detailed methodologies, known limitations, and calibration specifics.

## Appendices overview

- Appendix 1: LCM2007 Classes – detailed descriptions of each Broad Habitat class (e.g., Broadleaved woodland, Coniferous woodland, Arable and Horticulture, Improved Grassland, Semi-natural Grassland, etc.) and key nuances (e.g., distinctions among grassland types, bog vs heath, Montane Habitats, Inland Rock, etc.).
- Appendix 2: Relationship between Broad Habitats, LCM2007 classes and Broad Habitat sub-classes – mapping between Level 1 Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (with FieldCode descriptors).
- Appendix 3: Colour mapping – standard LCM2007 color palette for visualization, detailing Red/Green/Blue values for each LCM2007 class.

## Additional information and references

- Data sources include Landsat-TM5, SPOT-4/5, IRS-LISS3, and other satellite data; cartographic data from Ordnance Survey and related authorities; cross-institutional contributions via Countryside Survey Partnership.
- Acknowledgements and licensing notes emphasize Crown copyright, OS data restrictions, and CEH licensing arrangements.
- For more detail on Broad Habitat classification and relationships, consult Jackson (2000) and Morton et al. (2011) Final Report.