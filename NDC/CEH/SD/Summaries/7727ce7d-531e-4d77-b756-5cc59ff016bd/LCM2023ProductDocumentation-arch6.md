# The UKCEH Land Cover Map for 2023

- A comprehensive user guide for LCM2023, detailing data production, validation, accuracy, and how to use the seven datasets that comprise the product suite.
- Datasets cover Great Britain and Northern Ireland with both high-resolution classifications and parcel-based representations, plus 1 km summary rasters for cross-scale analysis.
- Emphasis on data quality, interpretability, and guidance for informed decision-making across environmental and policy applications.

## Product suite and data structure

- 10 m Classified Pixel datasets (GB and NI)
  - Pixels classified into UKCEH Land Cover Classes with a corresponding confidence/probability band.
  - First band: most likely UKCEH Land Cover Class; second band: class membership probability.
  - Not generalised by the UKCEH Land Parcel Spatial Framework to preserve detail such as narrow features.
- 25 m Rasterised Land Parcel datasets (GB and NI)
  - Rasterised versions of Land Parcel data (0.5 ha minimum parcel size, MMU).
  - Three-band rasters: dominant land cover mode, conf, and purity.
- Land Parcel Product (Vector)
  - Land parcel geometries with attributes (gid, hist, mode, conf, purity, stdev, agg, n, ogc_fid) for parcel-level analysis and change detection.
- 1 km Summary Raster products (GB and NI)
  - Summary rasters derived from 25 m data, including dominant cover (1 band), dominant aggregate (1 band), and percentage cover (21 bands for classes; 10 bands for aggregates).
  - Percentage values are integers; totals may not sum to exactly 100 due to rounding, especially near coastlines.
- Dataset coordinate systems and extents
  - Great Britain: British National Grid (EPSG: 27700)
  - Northern Ireland: Irish TM75 Grid (EPSG: 29903)
  - Extents defined for GB and NI datasets; per-parcel product extents and pixel resolutions detailed in the documentation.

## Methods: production, inputs, and classification

- Seasonal Composite Images
  - Derived from Google Earth Engine using Sentinel-2 surface reflectance, resampled to 10 m with four seasonal composites (Jan–Mar, Apr–Jun, Jul–Sep, Oct–Dec).
  - Ten Sentinel-2 bands used; occasional data gaps due to cloud are handled by the classifier.
- Context Rasters
  - 10 m context rasters to reduce spectral confusion, including terrain (Height, Aspect, Slope) and proximity masks (distance to buildings/roads/tidal water/freshwater, foreshore, woodland, saltmarsh).
  - Separate context rasters for GB and NI with region-specific layers.
- Classification Scenes and Bootstrapped Training
  - GB classified in 32 tiles (Classification Scenes); NI classified in a single Scene due to smaller area.
  - Bootstrap Training: uses historic LCMs (LCM2020–LCM2022) to automatically generate training observations; pixels with >80% probability and consistent classification across three years are used for training.
  - Random Forest classifier trained with balanced sampling (10,000 samples per bag) to avoid dominance by common classes.
- Validation and accuracy
  - Formal validation using 33,107 reference points across all 21 classes.
  - Overall accuracy reported at 83%.
- Data provenance and updates
  - Annual production approach with continuous improvements; potential methodological changes acknowledged in the disclaimer.

## Output details and data quality

- 10 m Classified Pixels
  - High detail preserving small features; validation against 25 m parcel datasets rather than 10 m pixels.
- 25 m Rasterised Land Parcels
  - Used for formal validation; aligned to the Land Parcel Spatial Framework MMU of ~0.5 ha.
- Land Parcel Product (Vector)
  - Includes per-parcel statistics (hist, mode, conf, purity, n, agg) for detailed parcel-level analysis.
- 1 km Summary Rasters
  - Useful for broad-scale change assessment and multi-scale comparisons; rounding may cause minor sum discrepancies.
- Known issues and caveats
  - A small number of polygons missing in vector land parcel products; negligible impact on 1 km outputs.
  - Land Parcel identifiers (gid) differ from LCM2015; direct parcel-id-based crosswalking may not be possible.
  - Some interclass confusion remains (notably among related habitat classes); ability to detect change relies on annual data and robust context layers.
  - Coastal and intertidal zones prioritized for land cover mapping; some saltwater/freshwater separation challenges near tidal areas.

## Data use, access, and citation

- DOIs and citations are provided for each dataset (10 m classified pixels GB/NI, 25 m rasterised land parcels GB/NI, land parcels vector, and 1 km summary rasters).
- Users should cite the corresponding Marston et al. papers and DOIs as listed in Table 5 of the document.
- Documentation notes that methods have evolved across annual maps; users should consider possible methodological changes when comparing across years.

## Dataset schemas and key attributes

- 10 m Classified Pixels
  - Band 1: integer class identifier (UKCEH Land Cover Class)
  - Band 2: conf or probability score for the classified class
- 25 m Rasterised Land Parcels
  - Band 1: dominant land cover class (mode)
  - Band 2: classification confidence (conf)
  - Band 3: parcel-level purity (purity)
- Land Parcel Vector (Land Parcel Product)
  - gid: unique parcel identifier
  - hist: frequency descriptor
  - mode: most frequent class within the parcel
  - conf: mean class membership probability
  - purity: parcel-level confidence measure
  - stdev: standard deviation of conf
  - agg: aggregate class mapping (see Appendix 1–3)
  - n: number of 10 m pixels intersecting the parcel
  - ogc_fid: vector dataset identifier for production workflows
- 1 km Summary Rasters
  - Dominant cover (1 band) and Dominant aggregate (1 band)
  - Percentage cover per class (21 bands) and per aggregate (10 bands)

## Visualization and colour representation

- Appendix 5 and Appendix 6 provide recommended colour recipes for displaying UKCEH Land Cover Classes, including color-blind friendly options.
- A QGIS symbology file (lcm_raster.qml) and a color-blind friendly version (lcm_raster_cb_friendly.qml) accompany the data products to facilitate consistent visualization.

## Appendices: supplementary context for data interpretation

- Appendix 1: Notes on UKCEH Land Cover Classes (class-specific considerations and training data caveats)
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats (definitions and mappings to UKCEH classes)
- Appendix 3: Full list of datasets and DOIs for UKCEH LCM2023
- Appendix 4: Correspondence matrices (classification accuracy by class)
- Appendix 5–6: Colour recipes for standard and color-blind friendly displays

## Practical implications for data support and reuse

- LCM2023 provides a multi-resolution, highly detailed baseline for UK land cover with robust validation and explicit caveats.
- Useful for policy analysis, environmental monitoring, and change detection when integrated with parcel-level and 1 km products.
- Bootstrap Training and annual updates help distinguish real change from classification noise, supporting time-series analyses and trend detection.
- Users should be mindful of differences in parcel identifiers across years and varying class definitions when performing longitudinal comparisons.