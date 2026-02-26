# 1.1 Satellite imagery and Pre-processing

- Objective and approach
  - Use Sentinel 1A SAR data (C-band, VV and VH, Interferometric Wide Swath) to map water bodies over Shivamogga, Sindhudurg, and Wayanad.
  - Apply standardized pre-processing and thresholding workflow to generate monthly water-body maps (referred to as S1A maps).

- Data sources and acquisition
  - Sentinel-1A Level-1 Ground Range Detected (GRD) data from Alaska Satellite Facility (ASF) portal.
  - Ground control points collected during field visits.
  - Regions: Shivamogga, Sindhudurg, and Wayanad with defined CRS-WGS84 extents.

- Pre-processing workflow (Sentinel-1A in SNAP)
  - Apply orbit file to update trajectory information.
  - Thermal noise removal to reduce background energy and improve continuity across sub-swaths.
  - Calibration to convert to backscatter intensity using GRD metadata.
  - Speckle filtering with refined Lee filter to reduce grainy SAR noise.
  - Slice assembly and mosaicking when data spans multiple scenes; subset/crop to study area.
  - Output: pre-processed data ready for water-body extraction.

- Water-body extraction (threshold-based)
  - Water bodies extracted from backscatter thresholds: water = 1, non-water = 0.
  - Threshold values determined per study area and month via histogram analysis of backscatter (water appears dark in SAR).
  - Monsoon adjustments: thresholds largely similar across months, but during monsoon months area and number of water bodies increase, causing threshold shifts.
  - Decision: apply a common average threshold for all months except monsoon months (thresholds and statistics summarized in Tables 1 and 2).
  - Result: monthly water-body maps for each region; a pixel is labeled water if identified as water in either of the two co-registered images (maps mosaicked into a single monthly S1A water map).

- Ground control points and field data
  - Ground truth collected using Open Data Kit (ODK) for water and non-water classes in Shivamogga (Aug 2018), Sindhudurg (Dec 2017), and Wayanad (Nov 2018).
  - Reference classes include lakes, rivers, ponds, reservoirs, and inundated fields (water) and built-up, forest, grassland, etc. (non-water).

- Accuracy assessment (validation methodology)
  - Use a total of 3,202 reference points across regions: Shivamogga (890), Sindhudurg (705), and Wayanad (1,606).
  - Confusion-matrix-based accuracy assessment, following Stehman and Foody (2019).
  - Compute overall accuracy, producer accuracy (omission), and user accuracy (commission) with standard errors.
  - Cloud-affected reference points masked using JRC quality tags for Shivamogga; remaining regions fully assessed.

- Region-specific data and validation highlights
  - Shivamogga water map (August 2018): overall accuracy 98.64% (SE 0.34%); detailed matrix indicates high producer and user accuracies with some water misclassification risk in certain samples.
  - Sindhudurg water map (December 2017): overall accuracy 99.58% (SE 0.08%); strong performance with low error rates.
  - Wayanad water map (November 2018): overall accuracy 99.84% (SE 0.11%); highest observed accuracy among the three regions.

- Regional thresholds and data characteristics
  - Tables provide site- and date-specific backscatter thresholds (e.g., Shivamogga, Sindhudurg, Wayanad for multiple dates in 2017–2018).
  - Averages and standard deviations are reported across months/years per region, illustrating general threshold stability with monsoon-related variations.
  - When thresholds were similar across months, averages were used; monsoon months used region-specific adjustments.

- Additional references and methodological context
  - Thermal noise removal and water extraction methods referenced to Park et al. (2018) for thermal noise removal in Sentinel-1 TOPSAR cross-polarization.
  - Water-body monitoring context referenced to De Vries et al. (2020) for flood monitoring using Sentinel-1 and Landsat data.
  - Accuracy assessment methodology aligned with key issues discussed by Stehman & Foody (2019).

- Data management and accessibility
  - Processed water-body maps (S1A) created for monthly monitoring.
  - Ensured storage and uploading of created datasets to appropriate portals in alignment with standard monitoring practices.
  - Emphasis on enabling broader access to underlying data used to produce final outputs, addressing one of the stated challenges for environmental data analysts.