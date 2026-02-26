# Code to assess active river channel change using Landsat 5/7/8 in Google Earth Engine (GEE)

- Purpose
  - A dataset containing code to assess active river channel change (planform adjustments) within a user-defined region of interest (ROI) using Landsat 5, 7 and 8 in Google Earth Engine (GEE).
  - Used by Boothroyd et al. (2020a) to investigate decadal river migration at critical bridge infrastructure in the Philippines.
  - Produces binary active river channel masks, centreline and width estimates, and similarity coefficients to quantify planform change over time.
  - Parameter sets are tailored for rivers in the Philippines and may not generalize across different hydro-geomorphic settings.

- Key data processing steps (workflow)
  - ROI and timing
    - Draw a circular ROI around each bridge point with a radius of 4.5 km.
    - ROI extends upstream and downstream around the bridge reach to capture possible downstream migration.
    - For outlets near oceans or lakes, manually edit ROI to exclude large water bodies.
    - Use two-year time periods to compile Landsat imagery, ensuring enough cloud-free data in cloud-prone regions.
    - Decadal intervals used for planform assessment: 1988–89 (T1), 1998–99 (T2), 2008–09 (T3), 2018–19 (T4).
  - Cloud masking and temporal compositing
    - Apply CFmask to mask clouds and shadows for each image.
    - Create a single image per period using a median reducer to produce a temporal composite for each spectral band.
  - Active channel classification (binary mask)
    - Use Zou et al. (2018) method with NDVI, EVI, and MNDWI to classify water pixels and distinguish alluvial deposits.
    - Active channel mask formed by combining wetted channel and alluvial deposits (MNDWI ≥ -0.4 and NDVI ≤ 0.2).
    - Exclude vegetated pixels to enforce active channel boundaries.
  - Cleaning and export
    - Remove small disconnected areas (< 100 pixels).
    - Apply a 3-pixel morphological closing to smooth edges and produce a continuous active channel representation.
    - Export binary active channel masks for each time interval (1988–89, 1998–99, 2008–09, 2018–19) to Google Drive as GeoTIFF.
  - Visual workflow context
    - Processing steps are illustrated (cloud masking, temporal compositing, active channel classification, cleaning, and export) with a focus on ROI around bridges.

- Similarity analysis (planform change)
  - Compute similarity coefficients between binary active channel masks to quantify planform changes.
  - Concepts
    - Work with binary presence-absence comparisons using a contingency table (a, b, c, d) as in the schematic.
    - Exclude negative matches (d) to avoid measuring non-river pixel similarity.
  - Coefficients used
    - Jaccard index (SJ = a / (a + b + c)); preferred due to many presence-presence instances; ranges from 0 to 1.
    - Dice similarity coefficient (SD = 2a / (2a + b + c)); included for context, but results presented primarily for Jaccard.
  - Time interval calculations
    - Decadal changes: compute mean Jaccard between T1–T2, T2–T3, T3–T4.
    - 30-year scale: compute Jaccard between T1 and T4.
  - Outputs
    - Similarity coefficient data are output to the GEE console for subsequent analysis.

- River width and centreline extraction
  - RivWidthCloud (Yang et al., 2019) applied to the binary active channel masks to extract river centreline positions and widths.
  - Inputs
    - Binary active channel masks (not full Landsat tiles) around bridge infrastructure.
  - Parameters (based on sensitivity tests)
    - Maximum search distance: 50 km
    - Maximum island size: 10 pixels
    - Maximum branch length to remove: 500 pixels
  - Outputs
    - Spatially continuous active channel width estimates and centreline positions.
    - Summary statistics: area, width metrics, centreline counts, min/max/mean/std of widths, various similarity indices (Jaccard, Kulczynski, Dice, Ochiai) across specified time intervals.
  - Export and reporting
    - RivWidthCloud outputs and summary statistics are provided, with centreline point attributes exported as CSV to Google Drive.

- Outputs and data products
  - Binary active river channel masks
    - Exported per time interval to Google Drive as GeoTIFFs (T1: 1988–89, T2: 1998–99, T3: 2008–09, T4: 2018–19).
  - RivWidthCloud outputs
    - Summary statistics and similarity coefficients (to the GEE console) for each time interval (T1–T4) and inter-interval comparisons (e.g., T1–T2, T2–T3, T3–T4, T1–T4).
    - Metrics include: area (km^2), number of active-channel pixels, min/max/mean/std active channel width (m), and various similarity coefficients (Jaccard, Kulczynski, Dice, Ochiai).
  - Centreline attributes (CSV)
    - Attributes of centreline points, including projection (EPSG), endsInWater/endsOverEdge flags, mean elevation (MERIT DEM), image metadata (image_id), latitude, longitude, orthogonal direction, and width at each centreline point (m).

- Data accessibility and reuse
  - Outputs are stored in Google Drive and summarized in the GEE console for further analysis.
  - The code includes comments indicating where user-defined inputs can be modified.
  - Acknowledges data sources (e.g., Philippines bridge inventory) and funding support.

- Parameterization and transferability
  - Parameter sets are developed for rivers in the Philippines; applicability to other regions or hydro-geomorphic settings may be limited.
  - Users should re-tune thresholds (e.g., NDVI, MNDWI) and ROI design if applying to different river systems or climates.

- Case study and acknowledgement
  - Example context: Sarrat Bridge (Padsan River) used to illustrate workflow (coordinates provided in figure caption).
  - Acknowledges DPWH bridge inventory data and NERC/DOST-PCIEERD Newton Fund support.

- References (context for methods)
  - Key sources include Zou et al. (2018) for water and alluvial classification; RivWidthCloud (Yang et al., 2019) for width/centreline extraction; Boothroyd et al. (2020a, 2020b) for applications of GEE in fluvial geomorphology; foundational works on Jaccard, Dice, and related similarity measures.