# Summary

- Purpose and scope
  - A data set and Google Earth Engine (GEE) workflow to assess active river channel change (planform adjustments) in a user-defined region of interest (ROI) using Landsat 5, 7 and 8 imagery.
  - Used by Boothroyd et al. (2020a) to investigate decadal river migration near critical bridge infrastructure in the Philippines.
  - Produces binary active channel masks, width/centreline statistics via RivWidthCloud, and similarity metrics to quantify planform change.

- Data inputs and ROI design
  - ROI defined as a circular buffer around each bridge point (4.5 km radius in the cited workflow); buffers extended upstream and downstream to capture migration channels.
  - Time periods: two-year intervals to maximize cloud-free imagery in persistent-cloud regions; decadal comparisons 1988-89, 1998-99, 2008-09, 2018-19.
  - Landsat 5, 7 and 8 imagery processed with cloud/shadow masking (CFmask).

- Processing workflow (three main steps)
  - Cloud masking, temporal compositing
    - Create time-specific image collections (two-year windows) and apply CFmask.
    - Generate a single composite image per period using median reduction of non-cloud pixels.
  - Active river channel classification
    - Classify wetted channel and alluvial deposits using multi-spectral indices (MNDWI, NDVI, EVI).
    - Active channel mask = water/open-water/open-channel pixels (MNDWI ≥ -0.4) and non-vegetated (NDVI ≤ 0.2); fuse wetted channel and alluvial deposits.
  - Cleaning and export
    - Remove small isolated areas (<100 pixels); apply one pass of morphological closing to smooth edges.
    - Outputs: binary active river channel masks exported as GeoTIFFs to Google Drive for each time period.
  - Active channel width and centreline computation
    - Apply RivWidthCloud to the binary active channel masks to derive centreline positions and width statistics.
    - Parameters tuned for the study (see below).

- Similarity analytics for planform change
  - Compute binary similarity between successive time periods using presence-absence contingency tables.
  - Preferred metric: Jaccard index (range 0–1; closer to 1 indicates less planform adjustment). Dice and other coefficients are discussed but Jaccard is reported here.
  - Outputs include Jaccard (T1–T2, T2–T3, T3–T4, T1–T4) and related statistics as part of RivWidthCloud outputs.

- RivWidthCloud outputs and metadata
  - Active channel widths and centreline statistics produced for centerline points; outputs include mean, min, max, and standard deviation of widths per interval.
  - Centreline attributes exported as CSV, including:
    - CRS, image_id, latitude, longitude, orthogonalDirection, width, endsInWater, endsOverEdge, flag_elevation, endsInWater, endsOverEdge, and image metadata (e.g., EPSG code, elevation).
  - Outputs also include per-interval area (km²), number of active-channel pixels, and centerline point counts.

- Parameterization and scope limitations
  - ROI and thresholds are calibrated for Philippine rivers; parameter sets may not be universally applicable to different hydro-geomorphic settings.
  - RivWidthCloud settings used: maximum search distance 50 km, maximum island size 10 pixels, maximum branch length 500 pixels.
  - User-defined inputs are clearly commented in the code to support adaptation.

- Outputs and data management
  - Binary active river channel masks exported to Google Drive (.tiff) for T1–T4.
  - RivWidthCloud summary statistics and similarity coefficients appear in the GEE console for further analysis.
  - Centreline point attributes exported to Google Drive as .csv; includes detailed metadata to support discoverability and reuse.

- Acknowledgements and references
  - Acknowledges data sources (Philippines DPWH bridge inventory and related agencies) and funding (NERC-DOST Newton Fund).
  - References foundational methods and prior applications (e.g., Jaccard/Dice coefficients, RivWidthCloud, cloud masking, and morphological operations).

- Data governance and reuse considerations for data leaders
  - Emphasizes end-to-end data processing, from ROIs and time windows to binary masks and width/centerline outputs, enabling traceability and auditability.
  - Outputs are designed for discoverability via GIS tools and GEE console, with metadata-rich CSVs to facilitate integration into broader data ecosystems.
  - Highlights the need to verify applicability to other regions due to region-specific calibration and thresholds; encourages documenting input assumptions, parameters, and update cadence for governance and collaboration.