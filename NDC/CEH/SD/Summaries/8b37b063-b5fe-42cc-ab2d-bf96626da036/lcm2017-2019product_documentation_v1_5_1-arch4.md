# The UKCEH Land Cover Maps for 2017, 2018 and 2019

- Purpose of the document
  - User guide for three new UKCEH Land Cover Maps: LCM2017, LCM2018, and LCM2019.
  - Describes content, structure, data production, validation, and planned future plans to help users apply the data effectively.

- Key production approach
  - All three maps were produced automatically using Bootstrap Training combined with a Random Forest (RF) classifier.
  - Landsat/Sentinel-based inputs: Sentinel-2 Seasonal Composite Images (TOA reflectance) were generated per season and combined with 20m Context Rasters to create Classification Scenes.
  - Timeseries approach aims for annual map outputs; no manual corrections were applied in this release.
  - Validation shows maps are of similar quality to the latest predecessor (LCM2015), with formal checks and visual validation.

- Data, classes, and general structure
  - 21 UKCEH Land Cover Classes (same set used by LCM2015; not a direct one-to-one with UK BAP Broad Habitats).
  - For each year, datasets are provided in multiple spatial formats:
    - 20m Classified Pixels (GB and NI)
    - Land Parcels (GB and NI)
    - 25m Rasterised Land Parcels
    - 1km Percent Cover (21 bands)
    - 1km Percent Aggregate Cover (10 bands)
    - 1km Dominant Cover (1 band)
    - 1km Dominant Aggregate Cover (1 band)
  - A total of 42 datasets across the three years (GB and NI products per year).

- 20m Classified Pixels and RF output
  - New addition: 20m Classified Pixels provide per-pixel class membership probabilities (band 2 depicts confidence 0–100; band 1 is the top class).
  - These pixels are not generalized by the Land Parcel Spatial Framework to preserve fine detail (e.g., narrow features).

- Land Parcels and data attributes
  - Land Parcels summarise 20m Classified Pixels within a UKCEH Land Parcel Spatial Framework.
  - Attributes include:
    - gid: unique parcel identifier
    - _hist: histogram-like representation of class frequencies within the parcel
    - _mode: most frequent class within the parcel
    - _purity, _conf, _stdev: metrics of classification confidence and distribution
    - _n: number of 20m pixels intersecting the parcel
  - Some attribute names differ from LCM2015 to align with production software, but meaning is retained.

- 25m Rasterised Land Parcels and 1km grids
  - 25m parcels are derived by rasterising Land Parcels (3-band raster: band 1 = _mode, band 2 = _conf, band 3 = _purity).
  - 1km datasets aggregate parcel data to a 1km grid:
    - 1km Percent Cover (21 bands)
    - 1km Percent Aggregate Cover (10 bands)
    - 1km Dominant Cover (1 band)
    - 1km Dominant Aggregate Cover (1 band)

- Seasonal Composite Images and spectral inputs
  - Seasonal Composite Images are median TOA reflectance per season from Sentinel-2 (bands 2,3,4,5,6,7,8,11,12; 20m resolution).
  - Some seasonal gaps due to clouds are carried as nulls; the RF classifier tolerates partial spectral information.
  - Google Earth Engine provides the data as TOA; SR was considered but did not improve classification in this release.

- Context rasters and classification scenes
  - Context rasters (GB 20m, NI 20m) provide ancillary spatial information to reduce spectral confusion:
    - GB: terrain (Height, Aspect, Slope), proximity masks (buildings, roads, sea, freshwater), foreshore, tidal water, and a woodland mask
    - NI: similar terrain measures plus urban mask and distance-to-coast/freshwater/road
  - Great Britain uses overlapping 100x100 km Classification Scenes (36-band spectral + 10 contextual = 46-band GB scenes); Northern Ireland uses a single 43-band scene per year.

- UKCEH Land Parcel Spatial Framework
  - Framework unchanged in parcel geometry since LCM2015, but storage and indices were reorganised for faster processing.
  - gid values between LCM2015 and 2017–2019 do not match; comparisons should use gid across the newer framework.
  - Minimum mappable unit is ~0.5 hectares; parcels represent discrete real-world units (fields, parks, urban areas, etc.).
  - The framework is a recommended structure, but users can apply their own parcel schemes when using the 20m Classified Pixels dataset.

- Bootstrap Training and Random Forest classification
  - Bootstrap Training uses historical maps (LCM2015 bootstrap from LCM2015 data) to automatically generate spectral training observations for RF classification.
  - Training samples are drawn with replacement to balance class representation (10,000 samples per bag per year).
  - The approach relies on majority signal; new maps update using majority signals from prior maps (evolving bootstrap strategy: 2017–2019 from 2015; future years from 2017–2019 across the three-year window).

- Validation and accuracy
  - Validation conducted against GB countryside survey data (2019), National Forest Inventory, IACS, and bespoke LCM validation points (22,325 locations in total).
  - Reported overall accuracy at UK scale:
    - LCM2017: 78.6%
    - LCM2018: 79.6%
    - LCM2019: 79.4%
  - Validation results reflect the mapping of 21 UKCEH Land Cover Classes; some caveats apply due to class definition conversions and point sampling differences.

- Data access, metadata, and technical details
  - Coordinate systems:
    - Great Britain: British National Grid (EPSG: 27700)
    - Northern Ireland: Irish Grid TM75 (EPSG: 29903)
  - Dataset characteristics:
    - 20m Classified Pixels: 2-band rasters (dominant class and confidence)
    - 25m Rasterised Land Parcels: 3-band rasters (band 1 = mode, band 2 = conf, band 3 = purity)
    - 1km datasets: multiple 21-band or 10-band rasters as described above
  - Pixel sizes and extents:
    - 20m pixels for classified outputs
    - 25m parcels
    - 1km grids for percent cover and dominant classes
  - Appendix content provides relationships between class schemes, colour mappings, and validation confusion matrices.
  - Full dataset listing and production specifics are provided in Appendix 5.

- Important considerations for users
  - Gid values do not match LCM2015; cross-year parcel comparisons should use the updated gid framework.
  - UK BAP Broad Habitat labels are italicised where referenced; UKCEH Land Cover Classes are capitalised.
  - While aimed at consistency, some spectral/classification ambiguities exist (e.g., upland peatland classes, bracken vs acid grassland), and the appendix provides detailed notes.
  - The data represent automatic classifications with explicit notes on limitations; ongoing improvements and potential future enhancements (e.g., additional data sources, broader satellite inputs) are discussed.

- Future direction and availability
  - UKCEH intends to continue annual releases and to review inputs (e.g., potential use of Sentinel-1 SAR data to fill gaps).
  - The 2020 and 2021 releases are planned to leverage bootstrap strategies from multi-year signals (2017–2019 and 2018–2020, respectively).