# National-scale assessment of decadal river migration at critical bridge infrastructure in the Philippines

- Purpose and scope
  - Provides code and workflow to assess active river channel change (planform adjustments) for a user-defined region of interest (ROI) using Landsat 5, 7, and 8 in Google Earth Engine (GEE).
  - Demonstrated by Boothroyd et al. (2020a) for decadal river migration around critical bridge infrastructure in the Philippines.
  - Notes that parameter sets are Philippines-specific and may not transfer to other river systems with different hydro-geomorphic settings.

- Region of interest and temporal framework
  - ROI defined as a circular buffer around each bridge point, with radius extending upstream and downstream (4.5 km demonstrated).
  - Time periods for analysis: two-year temporal composites at T1 (1988-89), T2 (1998-99), T3 (2008-09), and T4 (2018-19).
  - Decadal comparison: Jaccard index between T1 and T4; decadal comparisons via mean Jaccard between adjacent periods (T1–T2, T2–T3, T3–T4).

- Data and processing workflow
  - Data sources: Landsat 5, 7, 8 imagery; cloud/shadow masking using CFmask; temporal compositing via median reducer to create cloud-free composites for each period.
  - ROI handling: circular buffer around bridges; manual edits near outlets to exclude large water bodies when needed.
  - Active channel classification (water and alluvial deposits)
    - Multi-spectral indices: MNDWI, NDVI, and NDVI thresholding to separate wetted channel and unvegetated alluvial deposits.
    - Binary active channel mask created by combining wetted channel and alluvial deposits; vegetation excluded from active channel boundaries.
    - Thresholds used: MNDWI ≥ -0.4 and NDVI ≤ 0.2; NDVI threshold of 0.2 aligns with dense riparian vegetation literature.
  - Cleaning and refinement
    - Remove small disconnected areas (<100 pixels).
    - Apply a 3-pixel morphological closing to produce a smooth, continuous active channel representation.

- Active channel width and centreline extraction
  - RivWidthCloud (GEE) used to derive active river centreline and widths from binary active channel masks (inputs are masks around bridge reaches, not full tiles).
  - Parameterization (based on sensitivity tests): maximum search distance 50 km; maximum island size 10 pixels; maximum branch length 500 pixels.
  - Outputs include spatially continuous width estimates and centreline positions; summary statistics (mean, std, min, max) for active channel width.

- Outputs and data products
  - Binary active river channel masks exported per time interval as GeoTIFFs to Google Drive (T1–T4).
  - RivWidthCloud summary statistics and similarity coefficients available in the GEE console for each time interval.
  - Centreline point attributes exported as CSV to Google Drive (including CRS, image ID, latitude, longitude, orthogonalDirection, width, and other quality flags such as endsInWater, endsOverEdge, flag_elevation).
  - Outputs include per-interval metrics:
    - Pixel count and area (km^2) of active channel mask per T1–T4.
    - Active channel width statistics: min, max, mean, std dev (in meters).
    - Similarity metrics across intervals: Jaccard index (primary), plus Dice and other similarity coefficients for analysis (Kalnczynski, Ochiai, etc., as outputs in RivWidthCloud).
    - Centreline point data: projection (EPSG), coordinates, direction, and measured width.

- Outputs and dissemination considerations
  - Outputs are shared publicly via Google Drive and accessible analysis via the GEE console.
  - The workflow is explicitly scripted, with commented sections indicating where user-defined inputs can be modified.
  - Acknowledges data sources (Philippines DPWH bridge inventory) and funding support (NERC-DOST Newton Fund).

- Relevance for monitoring framework authors
  - Provides a concrete, repeatable monitoring workflow to quantify planform change over multi-decadal periods in a policy-relevant setting (bridge infrastructure risk assessment).
  - Demonstrates integration of remote sensing data, standardized processing (cloud masking, temporal compositing, index-based classification), and quantitative change metrics (Jaccard, RivWidthCloud widths).
  - Emphasizes data provenance, openness, and governance considerations (public sharing of inputs/outputs, metadata considerations, and explicit data quality criteria).
  - Highlights practical challenges relevant to monitoring frameworks:
    - Data availability and quality: reliance on Landsat with cloud contamination; requires robust cloud masking and two-year composites to secure sufficient imagery.
    - Access and sharing: outputs are shared via Google Drive; potential barriers related to dataset accessibility and metadata completeness.
    - Data silos and interoperability: integration of multiple data types (imagery, bridge inventories, GIS outputs) requires careful coordination and documentation.
    - Generalizability: Philippines-specific parameter sets; caution when transferring methodology to different hydro-geomorphic environments.
    - Data governance and metadata: need for clear metadata around thresholds, ROI definitions, and processing steps to enable auditability and reuse.

- Acknowledgements and references
  - Data sources include the Philippines Department of Public Works and Highways bridge inventory.
  - Funded under NERC-DOST Newton Fund grant NE/S003312.
  - Key methodological references for cloud masking, hydrological and geomorphological analysis, and RivWidthCloud.

- Limitations to consider for policy evaluation
  - Parameter sensitivity to regional hydro-geomorphic settings may limit cross-region comparability.
  - Temporal window choices (two-year composites) balance cloud coverage against short-term variability; different regimes may require alternative temporal schemes.
  - Public data sharing requirements can constrain the use of certain datasets; explicit data governance measures are needed to ensure reproducibility.