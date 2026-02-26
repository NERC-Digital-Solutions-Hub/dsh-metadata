# A burnt area product for the boreal forest zone derived from MODIS imagery

## Objective and Scope
- Develop a daily-date burnt area product for the circumpolar boreal forest zone at 500 m resolution.
- Annual outputs: 11 TIFF files (one per year, 2001–2011); each pixel value is the Julian day of the first burn for that year.
- Validation against Landsat ETM reference imagery yielded a Kappa of 0.60.

## Study Area and Data Sources
- Circumpolar boreal forest defined by FAO Global Ecological Zones: Boreal tundra woodland, Boreal coniferous forest, Boreal mountain system; approx. 47 million km², latitudinal range 40°N–70°N.
- Countries included: Russia, Canada, USA (Alaska), Norway, Sweden, Finland, and a small area of China.
- Forest/woody areas identified using MODIS Land Cover Type (MOD12Q1) classes 1–8.
- MODIS Nadir BRDF-Adjusted Reflectance (N-BAR) 16-day product (MCD43A4) used for spectral data; 500 m resolution, 2400 × 2400 granules.
- Daily Thermal Anomalies product (MOD14A1) used to identify and date burning events.
- Quality control: Snow pixels identified by BRDF-Albedo Quality (MCD43A2) and fill values excluded.

## Burnt Area Detection and Dating Method
- Core index: Normalised Difference SWIR (NDSWIR) using NIR (MODIS band 2) and SWIR (MODIS band 6); sensitive to canopy water content as a biomass proxy.
- Snow/Fill exclusion to reduce error.
- Time-series approach: detect inter-annual changes in NDSWIR during the snow-free season (approximately early June to late August; Julian days 161–241). Yearly inter-annual difference calculated by subtracting the previous year’s 16-day NDSWIR values; results averaged over the season to yield a single annual difference value.
- Regional thresholding: image divided into 16 windows of 600 × 600 pixels; threshold set at 60% of the difference between the window mean and the mean of known burnt pixels (identified via TA).
- Binary burnt map: pixels classified as burnt (1) or unburnt (0); small pixel clusters (<4) are removed to reduce misclassifications.
- Burn date assignment: burn areas containing TA pixels are dated with the corresponding Julian Day of the TA; undated pixels are interpolated bi-linearly from nearby dated pixels.
- Output: a 500 m raster burnt area map per year, with pixel values representing the Julian Day of the first burn.

## Validation Procedure
- Reference data: manual interpretation of annual Landsat ETM time series (≈30 m) at 10 random locations (stratified by continent).
- Coverage: about 1.5% of the total area; from 2001–2007, eight ETM images per site plus a 2000 baseline.
- Process: geo-location corrections, re-projection to equal-area sinusoidal grid, resampling to match the 500 m burnt area map; pixel-by-pixel comparison excluding unclassified areas.
- Results:
  - 504 burnt areas identified by ETM; 316 (62%) also identified by the burnt area product (CEH-BA).
  - Per-pixel: 65,120 ETM burnt pixels; 45,807 (70%) matched CEH-BA.
  - Commission errors: 41,719 of 87,526 CEH-BA burnt pixels (47%) with no corresponding ETM burnt pixel; about half of these overlap partially with ETM-burnt areas.
  - Overall agreement: Kappa = 0.60.

## Outputs, Access, and Reproducibility
- Outputs: annual 500 m burnt area maps with Julian day dates for first burn; 11 TIFF files (2001–2011).
- Data handling: standardized processing workflow linked to established MODIS products (N-BAR, TA, land cover) to enable integration with other environmental datasets.
- Storage and portals: datasets stored and uploaded to appropriate data portals; results are designed for clear dissemination and reuse by monitoring organizations.

## Challenges and Considerations for Monitoring
- Time lag between fire event and visible biomass reduction (particularly in Siberia) affecting dating accuracy.
- Spatial and phenological variability mitigated by 16-window segmentation and window-size optimization (600 × 600).
- Cloud cover and snow conditions leading to undated pixels; reliance on TA data for dating where available.
- Disturbances other than burning are included in the initial disturbed-area layer and subsequently filtered using fire-specific TA signals.

## Relevance to the Analysts Monitoring the Environment Archetype
- Adheres to standard data verification, quality assurance, and transformation practices; uses established MODIS-derived data products to produce a consistent, repeatable monitoring output.
- Presents results in clear, policy-relevant formats (yearly burnt-area maps with burn dates) suitable for long-term environmental health assessment and policy performance monitoring.
- Emphasizes the value of linking underlying datasets (e.g., TA, N-BAR, land cover) to improve transparency and reuse; supports data sharing by providing per-year TIFFs and an auditable methodology.

## References
- C. George, C. Rowland, F. Gerard, and H. Balzter, "Retrospective mapping of burnt areas in Central Siberia using a modification of the normalised difference water index," Remote Sensing of Environment, 2006.