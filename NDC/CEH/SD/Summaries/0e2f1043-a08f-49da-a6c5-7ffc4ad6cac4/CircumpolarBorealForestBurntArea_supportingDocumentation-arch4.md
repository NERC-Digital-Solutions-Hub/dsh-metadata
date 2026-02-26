# Burnt area product for the boreal forest zone derived from MODIS imagery

- Purpose
  - Describes a burnt area product for the circumpolar boreal forest zone derived from MODIS imagery.
  - Provides daily burn date at 500 m resolution for each year 2001–2011; output is 11 TIFF files with pixel values representing the Julian day of first burn for that year.
  - Validation against Landsat (ETM+) reference images yielded a Kappa coefficient of 0.60.

- Study area and data sources
  - Area: circumpolar boreal forest (FAO Global Ecological Zones: Boreal tundra woodland, Boreal coniferous forest, Boreal mountain system); about 47 million km2, latitudinal range 40–70°N.
  - Countries: Russia, Canada, USA (Alaska), Norway, Sweden, Finland, and part of China.
  - Forested areas identified using MODIS Land Cover Type (MOD12Q1) IGBP classes 1–8.
  - Primary data inputs:
    - 16-day MODIS Nadir BRDF-Adjusted Reflectance (N-BAR) MCD43A4 for spectral information (NIR and SWIR) at ~500 m.
    - MODIS Thermal Anomalies product (MOD14A1) to identify burn dates.
  - Each granule covers 2400 × 2400 pixels (~500 m per pixel).

- Burnt area detection methodology
  - Index: Normalised Difference SWIR (NDSWIR) using NIR (MODIS band 2) and SWIR (band 6) as a proxy for canopy water content and biomass.
  - Pre-processing: exclude snow pixels (MODIS BRDF-Albedo Quality) and fill values.
  - Change detection: compute inter-annual differences in NDSWIR for a defined snow-free window (early June to late August, Julian days 161–241) by subtracting the previous year's 16-day NDSWIR values; average these differences across the period to obtain a single annual difference value per pixel (Eq. 2).
  - Variability reduction: divide imagery into 16 windows of 600 × 600 pixels to minimize lat/topography-induced variability.
  - Thresholding: within each window, set threshold at 60% of the difference between the window-mean of known burnt pixels (from TA) and the window mean; apply to create a binary burnt/unburnt layer.
  - Post-processing: remove burnt patches smaller than 4 pixels.
  - Burn confirmation and dating: use TA locations to identify known burnt pixels; discard areas without TA; assign Julian Day from TA to burnt pixels; undated pixels are interpolated bi-linearly from nearby dated pixels.
  - Output: yearly 500 m raster of burnt areas with pixel values equal to the Julian day of first burn.

- Validation and accuracy
  - Reference data: manual interpretation of annual Landsat ETM images (~30 m) at 10 random, continent-stratified locations; period 2001–2007; 2000 used as baseline for pre-burn.
  - Process: geo-correct, reproject to equal-area projection, resample to match 500 m grid; pixel-by-pixel comparison excluding unclassified areas.
  - Results:
    - 504 burnt areas identified in ETM imagery; 316 (62%) overlapped with CEH-BA product.
    - Per-pixel: 65,120 ETM-burnt pixels; 45,807 (70%) overlapped with CEH-BA.
    - Commission errors: 41,719 (47%) of CEH-BA burnt pixels had no corresponding ETM-burnt pixel; about half of these overlapped with ETM-burnt areas.
    - Overall Kappa: 0.60.

- Outputs and integration
  - 11 TIFF files (2001–2011) with burnt-area maps; pixel values indicate Julian day of first burn.
  - Binary burnt mask plus burn-date information suitable for disturbance and fire regime analyses in boreal forests.
  - Relies on integration of multiple MODIS products (N-BAR, TA, land cover) to produce the dated burnt area product.

- Implications for data leadership and data management
  - Data richness and utility: provides a consistent, long-term, regional dataset for monitoring boreal forest disturbance and fire dynamics.
  - Data quality considerations: moderate agreement (Kappa 0.60) with high-resolution references; notable commission errors require careful interpretation and potential cross-validation with higher-resolution sources.
  - Metadata and provenance: clear documentation of thresholds, windowing, QA/QC steps, and date-dating rules is essential for reproducibility and governance.
  - Data accessibility and governance: circumpolar scope involves multi-jurisdictional data coordination; model and processing steps should be standardized for integration into broader data ecosystems.
  - Gaps and limitations: dated pixels may remain undated in cloudy conditions; some errors persist due to commission/ambiguity in fire signals; analysis restricted to 2001–2011 window (extension would require updated inputs and re-validation).