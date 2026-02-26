# National-scale assessment of decadal river migration at critical bridge infrastructure in the Philippines

## Objective and scope
- Assess active river channel change (planform adjustments) around critical bridge infrastructure within a user-defined region of interest (ROI) using Landsat 5, 7 and 8 in Google Earth Engine (GEE).
- Analyze decadal changes over 30 years and quantify planform adjustment with similarity coefficients (Jaccard index and Dice coefficient) between time periods.
- Produce active river channel masks and width/centreline statistics to support infrastructure risk assessment and geomorphology research.

## Data, tools and processing workflow
- Data and software
  - Landsat 5, 7 and 8 imagery in Google Earth Engine (GEE).
  - RivWidthCloud (Yang et al., 2019) for active river width and centreline extraction.
- ROI and temporal framing
  - Circular ROI around each bridge point (radius 4.5 km), with upstream/downstream extension around the bridge reach.
  - Time periods: two-year windows to maximize cloud-free imagery (per period).
  - Decadal intervals: T1 (1988–89), T2 (1998–99), T3 (2008–09), T4 (2018–19).
- Cloud masking and compositing
  - CFmask to mask clouds/shadows.
  - Median reducer to create a single composite image per time period.
- Active channel classification
  - Multi-spectral indices: NDVI, EVI, MNDWI used to separate wetted channel and alluvial deposits.
  - Classification rule for active channel: MNDWI ≥ -0.4 and NDVI ≤ 0.2 (with NDVI threshold informed by literature for riparian vegetation).
  - Binary masks: wetted channel and alluvial deposits combined to form an intermediate binary active channel mask.
- Cleaning and export
  - Remove disconnected areas < 100 pixels.
  - Morphological closing (3-pixel structuring element) to produce a continuous active channel representation.
  - Outputs per time period: binary active river channel mask exported as GeoTIFF to Google Drive.
- Outputs and model inputs
  - Centralized workflow diagram (Figure 1) illustrating cloud masking, temporal compositing, classification, and export steps.

## Active river channel widths and centrelines
- RivWidthCloud analysis
  - Applies to binary active channel masks around bridge infrastructure to estimate active river widths and determine centreline positions.
  - Parameter settings (based on sensitivity tests):
    - Maximum search distance: 50 km
    - Maximum island size: 10 pixels
    - Maximum branch length to remove: 500 pixels
- Outputs
  - Centreline points and width estimates for each time period.
  - Summary statistics: area (km^2), count of centreline points, minimum/maximum/mean/standard deviation of active channel width.
  - Data exported to GEE console for further analysis.

## Similarity analysis for planform change
- Similarity metrics
  - Jaccard index (and related Dice coefficient) calculated from binary active channel masks to indicate planform adjustment.
  - Negative matches (d) excluded to focus on presence-absence matches of river pixels.
  - Jaccard index prioritized (range 0–1; higher values indicate less planform change).
- Time intervals used for comparisons
  - T1–T4 for decadal-scale change, and T1–T2, T2–T3, T3–T4 for decadal-scale change assessments.

## Outputs and data products
- Spatial products
  - Binary active river channel masks for each time interval (1988–89, 1998–99, 2008–09, 2018–19) exported as GeoTIFFs (location-specific around bridge ROIs).
- Analytical outputs
  - RivWidthCloud summary statistics and similarity coefficients (T1–T4; T1–T2; T2–T3; T3–T4; T1–T4) available in the GEE console.
  - Centreline point attributes (CSV) exported to Google Drive, including:
    - crs, image_id, latitude, longitude, orthogonalDirection, width (active river width), elevation metrics (mean MERIT DEM), and various quality/edge flags (endsInWater, endsOverEdge, flag_elevation).
    - Additional fields such as width statistics (min/max/mean/std dev) and metadata about the centerline segmentation.
- Documentation and metadata
  - Outputs are designed to be generically usable in GIS and can be reinterpreted along other river systems with appropriate parameter tuning.

## Data sources and provenance
- Bridge inventory
  - Philippines Department of Public Works and Highways bridge inventory data, provided via the Detailed Bridge Inventory Application, with contributions from the Philippines Statistics Division and DPWH.
- Funding and collaboration
  - Part of NERC and DOST-PCIEERD Newton Fund grant (NE/S003312).

## Applicability, limitations, and considerations
- Philippines-specific parameterization
  - Parameter sets were developed for Philippine rivers and may not directly transfer to rivers with different hydro-geomorphic settings without recalibration.
- Temporal and spatial scope
  - Two-year windows improve cloud-free composites but may not capture shorter-term fluctuations.
  - ROI centered on bridges provides focused insight near critical infrastructure but is not a full-river analysis.
- Methodological choices
  - NDVI threshold (≤ 0.2) and MNDWI threshold (-0.4) are empirical and could affect sensitivity to vegetation and open-water detection.
  - Morphological cleaning choices (disallowing areas < 100 pixels; three-pixel closing) influence the resultant channel continuity.
- Data accessibility and reuse
  - Outputs are designed to be discoverable and usable with standard GIS tools, though the workflow relies on GEE and Google Drive exports.
  - Users should ensure appropriate data protection and context when reusing bridge-related datasets.

## Reproducibility and openness
- The codebase is annotated to indicate where user-defined inputs can be modified, supporting adaptation to other regions or datasets.
- Outputs (GeoTIFFs and CSVs) and GEE-based computations are designed for transparent replication and downstream analysis.