# The data set contains code to assess active river channel change (i.e. planform adjustments) for a userdefined region of interest (ROI) using Landsat 5, 7 and 8 products in Google Earth Engine (GEE)

## Overview
- Codebase used to assess active river channel change within a user-defined ROI using Landsat 5, 7 and 8 in Google Earth Engine (GEE).
- Applied by Boothroyd et al. (2020a) to investigate decadal river migration at critical bridge infrastructure in the Philippines.
- Outputs include binary active channel masks, centreline and width data, and similarity metrics to quantify planform change.
- Parameter sets are tailored for Philippine rivers and may not generalize to other hydro-geomorphic settings.

## Data inputs and ROI
- Imagery: Landsat 5, 7 and 8.
- Region of Interest (ROI): circular buffer around each bridge point with a radius of 4.5 km; buffers edited to exclude large water bodies near outlets where appropriate.
- Time periods: two-year windows for cloud-free composites; decadal comparisons (e.g., 1988–89, 1998–99, 2008–09, 2018–19) to assess planform change over different timescales.
- Bridge inventory: used to define ROIs; data includes publicly available bridge locations in the Philippines.

## Processing workflow (three main steps)
- Step 1: Cloud masking and temporal compositing
  - Use CFmask for cloud/shadow masking.
  - Create temporal composites (median) for each two-year period to generate cloud-free, multi-spectral imagery.
- Step 2: Active river channel classification
  - Compute multi-spectral indices (NDVI, EVI, MNDWI) to distinguish wetted channel and alluvial deposits.
  - Classify active channel as water/open water and non-vegetated alluvial area; apply thresholds (e.g., MNDWI ≥ -0.4 and NDVI ≤ 0.2).
  - Combine wetted channel and alluvial masks to form an intermediate binary active river channel mask.
- Step 3: cleaning and export
  - Remove small misclassifications by dropping disconnected areas < 100 pixels.
  - Apply morphological closing (three-pixel radius) to smooth edges and produce a continuous channel representation.
  - Export binary active channel masks per time interval to Google Drive as GeoTIFF.

## Similarity analysis and outputs
- Similarity coefficients
  - Calculate binary presence-absence based similarities between successive masks to quantify planform change.
  - Primary metric: Jaccard index (range 0–1); excludes negative matches to focus on presence-presence changes.
  - Also reference Dice (F1) and other indices but present results for Jaccard due to correlation.
- Active river channel widths and centrelines
  - Apply RivWidthCloud (Yang et al., 2019) to binary active channel masks to derive centreline positions and active widths.
  - Parameter settings (from sensitivity tests): maximum search distance 50 km, maximum island size 10 pixels, maximum branch length 500 pixels.
  - Outputs include width estimates and centreline data.
- Outputs (per time interval)
  - Binary active river channel mask: exported as GeoTIFF (T1=1988–89, T2=1998–99, T3=2008–09, T4=2018–19).
  - RivWidthCloud statistics: summary metrics (area in km^2, number of centreline points, min/max/mean/std width) available in GEE console.
  - Similarity statistics: Jaccard, Kulczynski, Dice, Ochiai for intervals T1–T2, T2–T3, T3–T4, and T1–T4; available in GEE console.
  - Centreline point attributes (CSV): includes crs, image_id, latitude, longitude, orthogonalDirection, width, and quality flags (e.g., endsInWater, endsOverEdge, flag_elevation, etc.).
  - Additional metadata: per-interval pixel counts and area totals for active channel masks.

## Accessibility and reuse
- Outputs are available via Google Drive (GeoTIFFs) and GEE console (statistics and attributes).
- Code annotated with sections where user-defined inputs can be modified, enabling adaptation to other study areas or ROIs.
- Limitations noted: Philippines-specific parameterization; careful consideration needed before applying to different hydro-geomorphic settings.

## Practical considerations for data support
- Data quality and compatibility: patchy data and multiple formats across platforms; ensure consistent ROI definitions and time period selections when reusing.
- Documentation and provenance: outputs are tied to specific bridge inventories and time intervals; reproduce steps by following the described processing pipeline.

## Acknowledgements and references
- Acknowledges Philippines DPWH bridge inventory data and related agencies; funded by NERC and DOST-PCIEERD Newton Fund.
- Key references for methods and tools include Boothroyd et al. (2020a, 2020b), RivWidthCloud (Yang et al. 2019), and foundational works on Jaccard/Dice similarities and image processing techniques.