# Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019

- Purpose: A satellite-derived dataset of geomorphic river mobility showing how often each location within river channels is occupied over time, to support prediction and resilience planning for river-related hazards in dynamic landscapes.

- Scope and outputs:
  - Ten catchments in the Philippines, with locational probabilities calculated for ~600 km2 of riverbed.
  - Binary active-channel masks and processed locational-probability outputs per catchment.
  - Example code and data to reproduce analyses in Google Earth Engine (GEE) and MATLAB, plus longitudinal analyses.
  - Spatial reference and resolution: EPSG: 32651 (WGS 84 / UTM zone 51N), ~10 m x 10 m.

- Core concept: Locational probability (lp) to quantify river mobility
  - Compute lp for each pixel as a weighted sum over time-windows, where each window represents a potential bankfull/morphodynamic event.
  - lp values range from 0 (never occupied) to 1 (always occupied).
  - Interpretation: low lp indicates high mobility; high lp indicates channel stability.

- Data and time frame
  - Time period: 1988–2019, using 16 two-year time-windows (e.g., 1988–1989, 1990–1991, etc.).
  - Each time-window represents a different morphological condition following a bankfull event.

- Methods in detail
  - Active channel extraction (binary masks)
    - Tools: Google Earth Engine (GEE) with Landsat imagery; trunk channel buffered by 3 km to define ROI.
    - Imagery: atmospherically corrected Landsat 5/7/8 within each two-year window.
    - Cloud masking: CFmask applied; cloud-free pixels retained; bicubic resampling to smooth channels.
    - Spectral indices: NDVI and MNDWI used to classify active channel.
    - Thresholds: MNDWI ≥ -0.4 and NDVI ≤ 0.2.
    - Output: per-window binary masks, rescaled to [0,1], reduced to a single image via the 10th percentile to best represent active-channel extents.
    - Final step: binary masks combined with logical AND to produce binary active-channel maps; exported as GeoTIFFs to Google Drive.
  - Versions for reproducibility
    - Version 1: Original GEE code (Landsat Collection 1; 1989–2019).
    - Version 2: Updated GEE code migrated to Landsat Collection 2 (supports Landsat 9; post-2022 processing).
  - Cleaning and quality control
    - Artefact removal in MATLAB:
      - Remove small disconnected areas (<500 pixels).
      - Morphological closing (disk radius 2 pixels) to smooth edges.
      - Remove large disconnected areas (<2500 pixels) distant from the trunk channel.
      - Manual GIS review to remove features not part of the main trunk channel.
    - Data quality notes: some time-windows are data-poor due to cloud cover or limited Landsat acquisitions; Mindanao catchments showed fewer usable images.
  - Locational-probability calculation
    - Equation-based approach aggregating binary masks across time-windows with equal weights.
    - Weighting: Wn = 1.0/x, where x is the total number of windows for the catchment.
    - Output: lp per pixel, with 0–1 scale, enabling interpretation of mobility vs. stability.

- Data structure and access
  - Includes README files, GEE code, MATLAB processing scripts, TopoToolbox workflows, and processed lp rasters for ten catchments.
  - Outputs prepared for replication and extension by the research community; scripts and data are organized by catchment and processing steps.
  - Data provenance and description linked to the methods section of Boothroyd et al. (2025) in Nature Communications; project funded by NERC and DOST-PCIEERD’s Newton Fund.

- Quality, limitations, and context
  - Validation: visual agreement between classified active channels and satellite/aerial imagery noted as good.
  - Limitations: variable data availability across time-windows and locations due to cloud cover and sensor availability; some catchments exhibit fewer usable images, affecting probability estimates in those areas.
  - Context: builds on established methodologies for measuring river-planform dynamics from remotely sensed imagery and contributes to large-scale assessments of decadal river mobility.

- Applications and relevance for analysts
  - Enables monitoring of environmental health and river-system dynamics over time to inform hazard resilience and infrastructure planning.
  - Provides standardized, reproducible datasets and code to support broader monitoring programs and inter-catchment comparisons.
  - Facilitates data-driven policy performance assessments related to river mobility and stability in dynamic tropical landscapes.