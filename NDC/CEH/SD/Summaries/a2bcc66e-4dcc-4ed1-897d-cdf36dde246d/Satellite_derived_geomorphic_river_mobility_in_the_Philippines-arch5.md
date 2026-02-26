# Supporting documentation for 'Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019'

## Overview
- Satellite-derived dataset describing geomorphic river mobility for ten catchments in the Philippines, using locational probability to map how often the active river channel occupies a given location.
- Quantifies locational probabilities for approximately 600 km² of riverbed to support prediction and resilience planning for river-related hazards in dynamic landscapes.
- Includes examples and outputs to support reproducibility: Google Earth Engine (GEE) and MATLAB codes to replicate analyses, plus processed outputs for the ten catchments.
- Funded by Natural Environment Research Council (NERC) and DOST-PCIEERD Newton Fund (grant NE/S003312/1).
- Fully described in Boothroyd et al. (2025) Nature Communications.

## Data content and structure
- Datasets included:
  - Example GEE codes to run satellite imagery analyses.
  - Example MATLAB codes and data to generate locational probabilities and to produce longitudinal analyses.
  - Processed locational probability outputs for the ten catchments.
- Supporting files comprise README documents detailing data structure and processing steps (GEE code, processed probabilities, and MATLAB processing/visualization scripts).
- Outputs produced per catchment include binary active-channel masks derived from Landsat imagery and the corresponding locational probability rasters.

## Processing workflow and reproducibility
- Active channel extraction:
  - Define trunk channel with a 3 km buffer; analyze Landsat 5, 7, and 8 imagery in two-year time-windows between 1988 and 2019.
  - Time-windows: 16 blocks (e.g., 1988–1989, 1990–1991, etc.) to maximize cloud-free data.
  - Cloud masking via CFmask; cloud-free pixels retained; bicubic resampling to smooth channel representation.
  - Indices used for classification: NDVI and MNDWI. Thresholds: MNDWI ≥ -0.4 and NDVI ≤ 0.2; pixels rescaled to [0,1].
  - Output per time-window: a single image (10th percentile) representing the active channel; binary masks created with an AND operation between NDVI- and MNDWI-derived masks; exported as GeoTIFFs to Google Drive.
- Code versions:
  - Original GEE code for Landsat Collection 1 (1989–2019) and updated code migrated to Landsat Collection 2 (processing Landsat 9 data); Ensures reproducibility with current Landsat data.
- Quality checks and cleaning:
  - Artefacts (e.g., built-up areas, agriculture) removed in MATLAB through:
    - Discarding disconnected areas < 500 pixels.
    - Morphological closing with a 2-pixel disk element.
    - Removing large, disconnected features > 2500 pixels away from the trunk channel.
  - Manual GIS sense-check and editing to ensure active channel alignment with the trunk channel.
  - Some time-windows are data-poor due to variable imagery availability; data quality varies by location (e.g., Mindanao catchments showed fewer usable images).
- Locational probabilities:
  - Computed from binary active-channel masks across time-windows.
  - p = sum(Wn * Fn), where Fn is 1 if the pixel is part of the active channel in time-window n, else 0; Wn = 1.0 / x (x = total number of time-windows for the catchment).
  - Equal weighting across time-windows, interpreting each window as an independent morphologic condition after a bankfull event.
  - Locational probability lp ranges 0–1; higher values indicate channel stability, lower values indicate mobility.
- Data products and units:
  - Spatial reference: EPSG:32651 (WGS 84 / UTM zone 51N); resolution ~10 m x 10 m.
  - Outputs include georeferenced rasters and accompanying documentation describing units (as noted in the codes).

## Data governance, metadata, and documentation
- Documentation provided via multiple README files specifying:
  - General data overview.
  - Subfolder-specific data structures (GEE code, GEE outputs, locational probabilities, and TopoToolbox processing outputs).
  - Example and migrated code versions to support reproducibility.
- Data provenance and versioning:
  - Clear distinction between Landsat Collection 1 and Collection 2 processing streams.
  - Codes and outputs aligned with current Landsat data availability (including Landsat 9).
- Quality control statements emphasize visual agreement with satellite imagery (Landsat, Google Earth) and documented data quality considerations.

## Data access, sharing, and stewardship considerations
- Primary data exports are delivered to Google Drive as GeoTIFFs; accompanying code and readme documentation enable reuse and reproduction.
- Data sharing practices emphasize:
  - Providing usable, documented code and processed outputs to enable adoption by others studying river mobility.
  - Clear notes about data limitations (e.g., data-poor windows, geographic variability in imagery availability).
- Potential governance considerations for custodians:
  - Include versioned updates when re-running with newer Landsat data or extended catchments.
  - Maintain metadata alignment with repository standards to ensure discoverability and interoperability.

## Challenges and limitations (as relevant to data stewardship)
- Incomplete or uneven user needs could arise from varying applicability of locational probabilities across rivers and time periods.
- Data availability limitations due to cloud cover and sensor availability, leading to data-poor time-windows in some catchments (notably Mindanao).
- The need for manual edits in GIS to ensure binary masks accurately reflect the trunk channel.

## Reference materials
- Core methodology and context are documented in Boothroyd et al. (2025) Nature Communications: Big data show idiosyncratic patterns and rates of geomorphic river mobility.
- Foundational references underpinning locational probability methodology and remote sensing techniques cited within the dataset documentation.