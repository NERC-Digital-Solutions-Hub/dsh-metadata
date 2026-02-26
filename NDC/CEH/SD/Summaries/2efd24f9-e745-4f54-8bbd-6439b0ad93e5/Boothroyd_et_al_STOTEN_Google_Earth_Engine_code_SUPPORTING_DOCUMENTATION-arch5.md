# Code to assess active river channel change using Landsat imagery in Google Earth Engine

- Purpose and scope
  - Provides code to assess active river channel change (planform adjustments) for a user-defined region of interest (ROI) around bridges in the Philippines.
  - Uses Landsat 5, 7 and 8 in Google Earth Engine (GEE) to generate binary active river channel masks and to quantify decadal and decadal-like changes.
  - Outputs include active channel masks, centreline widths, and similarity metrics to evaluate planform change over time.

- Data and inputs
  - Satellite data: Landsat 5, 7 and 8 imagery; cloud/cloud-shadow masking using CFmask.
  - Spatial domain: circular ROI around each bridge, extending upstream and downstream; manual edits to exclude large water bodies near outlets when needed.
  - Bridge and infrastructure data: publicly available bridge inventory data for the Philippines (DPWH), enabling a bridge-centric analysis around each site.
  - Spectral indices: multi-spectral classification using NDVI, MNDWI and EVI thresholds to separate wetted channel and alluvial deposits.

- Processing workflow
  - Step 1: Cloud masking and temporal compositing
    - Build time-specific image collections for two-year windows around each ROI.
    - Apply CFmask; create a temporal median composite for each spectral band to reduce cloud contamination.
  - Step 2: Active river channel classification
    - Classify water and open-channel features using MNDWI and NDVI thresholds; isolate non-vegetated active channel areas.
    - Combine wetted channel and alluvial deposits to produce an intermediate binary active river channel mask.
  - Step 3: Cleaning and export
    - Remove connected components smaller than 100 pixels.
    - Apply a three-pixel morphological closing to smooth edges and create a continuous channel representation.
    - Export binary active channel masks per time interval to Google Drive as GeoTIFFs.
  - Step 4: Widths and centrelines
    - Use RivWidthCloud (an App in GEE) on binary active masks to extract river centreline and active widths.
    - Apply parameters: maximum search distance 50 km, maximum island size 10 pixels, maximum branch length 500 pixels.
    - Produce summary statistics (mean width, min, max, std dev) and centreline point data.

- Similarity analysis (planform change)
  - Compute binary similarity coefficients between masks to indicate changes in channel extent over time.
  - Preferred metric: Jaccard index (also known as CSI or Threat Score) computed from presence-presence, presence-absence, and absence-presence contingency terms; range 0–1 with higher values indicating greater similarity (less planform change).
  - Additional metrics available: Dice (F1), Kulczynski, and Ochiai, but results emphasize Jaccard for consistency.
  - Comparisons of interest include decadal scales (T1–T4) and successive two-year to two-year intervals (T1–T2, T2–T3, T3–T4).

- Outputs and data products
  - Binary active river channel masks
    - Exported per time interval (1988–89, 1998–99, 2008–09, 2018–19) as GeoTIFFs.
    - Pixel-based binary encoding: 1 = active channel; 0 = non-channel.
  - RivWidthCloud outputs
    - Centreline points and active width estimates across the ROI vicinity, with associated statistics (mean, min, max, std dev) per time interval.
    - Summary fields and centreline attributes exported as CSV to Google Drive, including: crs, image_id, latitude, longitude, width, orthogonalDirection, endsInWater, endsOverEdge, flag_elevation, end-point metadata, and elevation (MERIT DEM).
  - Similarity and width statistics
    - GEE console outputs for final area (pixels and km^2), number of centreline points, min/max/mean/std of active channel width, and time-interval Jaccard (and other similarity) metrics for T1–T2, T2–T3, T3–T4, and T1–T4.
  - Documentation and provenance
    - Commented sections indicate where user-defined inputs can be modified, supporting reuse and adaptation.
    - Outputs include references to the original methodologies (e.g., Zou et al. 2018; RivWidthCloud 2019) and data sources.

- Temporal and spatial scope
  - Time periods used for assessment: two-year windows spanning 1988–89, 1998–99, 2008–09, and 2018–19 to reflect decadal-scale planform adjustment.
  - Planform change indicators computed both across the full 30-year span (T1 vs T4) and across consecutive two-year to two-year intervals (T1–T2, T2–T3, T3–T4).

- Generalisability and limitations
  - Parameter sets (e.g., ROI radius, classification thresholds) are developed for rivers in the Philippines and may not be universally applicable without adjustments to hydro-geomorphic settings.
  - While designed for bridge-adjacent analyses, the workflow can be adapted to other coastal or riverine contexts with appropriate tuning.

- Governance, data management, and stewardship considerations
  - Clear data provenance: inputs, processing steps, and outputs are described, enabling auditability and reproducibility.
  - Data products are stored in a centralized cloud workflow (Google Drive and GEE console), facilitating discovery and reuse by other researchers and practitioners.
  - Versioning and adaptability: code is annotated for user modifications, supporting updates as data sources or study objectives evolve.
  - Metadata and accessibility: outputs include comprehensive attributes (CRS, image IDs, coordinates, elevation flags, etc.) for downstream discovery and integration with GIS and hydrological models.

- Acknowledgements and references
  - Data sources include the Philippines DPWH bridge inventory and Philippine Statistics Division data.
  - The work builds on and cites supporting literature (e.g., Jaccard index, RivWidthCloud, Zou et al., 2018; Boothroyd et al., 2020a, 2020b).
  - Funding and collaboration noted via NERC and DOST-PCIEERD Newton Fund program.