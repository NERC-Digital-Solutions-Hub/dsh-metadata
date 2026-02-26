LAND COVER MAP 2007 DATASET DOCUMENTATION

## Overview
- UK-wide parcel-based land cover classification (LCM2007) with 23 classes based on UK Broad Habitats; produced from summer-winter composite satellite imagery at 20–30 m resolution.
- Maps land cover (not strictly land use) and updates LCM2000 using OS MasterMap/large-scale vector baselines refined with image segmentation.
- Highly metadata-rich dataset intended for diverse applications; consult the Final Report (Morton et al., 2011) for comprehensive methodology and limitations.

## Data Products and Coverage
- Vector Data Set: polygons with 10 attributes; contains ~8.6 million polygons (GB) and ~0.9 million (NI).
- Raster Data Sets:
  - 25 m raster: 23 LCM2007 classes.
  - 1 km raster: aggregated products (dominant class, and percentage cover) for both LCM2007 classes and Aggregate classes.
- Coverage: Great Britain and Northern Ireland are provided separately with respective projections.

## Key Classes and Sub-Classes
- 23 LCM2007 classes (based on Broad Habitats); some Broad Habitats are subdivided (e.g., Built-up Areas and Gardens into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland).
- Appendix 1 provides brief class definitions; Appendix 2 details relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes; Appendix 3 covers standard colour mappings.

## Vector Data Details
- Parcel_ID: unique id for each parcel (includes source image).
- BH: Broad Habitat level dominant class (e.g., Broadleaved woodland, Arable and Horticulture).
- BHSub: Broad Habitat sub-class (via FieldCode; for internal/validation use).
- FieldCode: short strings used in production; accuracy not formally QA’d at this level.
- INTCODE: numeric LCM2007 class (1–23) recommended for display and QA.
- KBE: Knowledge-Based Enhancements history (processing notes).
- ProbList: top 5 spectral-class probabilities (for each polygon).
- CorePixels/TotPixels: pixel counts used in classification and polygon size.
- Construct: origin of polygon (OSMM-derived; segmentation details).

## Raster Data Details
- 25 m raster: derived from vector; 23 LCM2007 classes; pixel values correspond to class mapping.
- 1 km raster: created by summarising 25 m data to compute dominant class and percentage cover per 1 km cell; supports UK-wide or regional analyses.

## Data Access and Licensing
- 1 km raster data: available via CEH Information Gateway.
- Full vector product and 25 m raster product: licensing on request from CEH; online application or direct contact provided; fees may apply.

## Spatial and Projections
- GB data: British National Grid (OSGB 1936).
- NI data: Irish National Grid (or transitioning to ITM for NI; reprojecting supported by GIS tools).

## Quality, Validation, and Limitations
- Ground-reference validation used to assess thematic accuracy; average accuracy reported at 83% across 9,127 polygons.
- Broad Habitat sub-classes and FieldCodes may be less consistent or validated; users should perform their own validation for sub-class level usage.
- LCM2007 maps land cover (spectral signatures) rather than exact land use; interpretation should consider context, especially for grasslands and other spectrally similar classes.
- MMU: minimum mappable area >0.5 ha; parcels <0.5 ha and linear features <20 m are dissolved into surrounding landscape during production.

## Practical Considerations for Data Support
- Large file sizes, especially the vector dataset; plan storage and processing capacity accordingly.
- Choose data representation based on workflow:
  - Vector: rich metadata and precise polygon boundaries but larger files.
  - 25 m raster: simpler processing, no per-polygon metadata, suitable for some modelling tasks.
  - 1 km raster: suitable for national-scale analyses or models requiring coarse resolution.
- For cross-walker analyses or integration with other datasets, use the Parcel_ID and related attributes; be mindful of Sub-class information and ProbList if sub-class usage is intended.
- When using Broad Habitat sub-classes, validate against field data or higher-resolution references due to potential accuracy limitations.

## Usage Notes and Recommendations
- Refer to the Final Report (Morton et al., 2011) for detailed production methodology and limitations.
- If detailed grassland classifications are critical, consider aggregating or validating Neutral/Calcareous/Acid Grassland as needed.
- For NI data, anticipate projection adjustments or ITM conversion as the NI dataset migrates.

## Appendices Highlights
- Appendix 1: LCM2007 class descriptions and definitions for 23 classes.
- Appendix 2: Mapping relationships between Broad Habitats, LCM2007 classes, and Broad Habitat sub-classes (FieldCodes and class numbers).
- Appendix 3: Colour mapping recipe for standard LCM2007 display (RGB values per class).

## Acknowledgements
- Data derived from multiple satellite sources (Landsat-TM5, SPOT-4/5, AWIFS, etc.) and Ordnance Survey cartographic data; CEH acknowledges partner organisations and license arrangements.