# Above-ground carbon density derived from LiDAR data over oil palm plantations in Malaysian Borneo, 2014

- Purpose: Develop LiDAR-based estimates of aboveground carbon density (ACD) for oil palm plantations in Malaysian Borneo and compare different estimation approaches (area-based, canopy cover, and tree-centric) calibrated against field measurements.

## Study area and field data

- Location: Stability of Altered Forest Ecosystem (SAFE) landscape, East Sabah, Malaysian Borneo (approx. 4.63–4.77 N, 116.95–117.70 E).
- Environment: Lowland tropical forest region; high rainfall (>2000 mm/year); plots below 800 m altitude; mixed sedimentary geology; extensive forest-to-palm conversion.
- Field plots: 27 vegetation plots (25 m × 25 m; 0.0625 ha) with North–South orientation, established in 2010; oil palm blocks of two ages (OP1 and OP2 planted in 2006; OP3 planted in 2000; 8- and 14-year-old stands).
- Measurements: In each 0.0625 ha plot, palm height measured in 2013 and 2015; average height used for analysis; no tree diameter measurements due to palm trunk growth patterns; density counted visually from Pléiades imagery to create 1-ha calibration plots.
- Field data adoption: Aims to calibrate LiDAR-based models of aboveground carbon density; plots arranged around three plantation blocks to mitigate within-plot size effects.

## Remote sensing and LiDAR data

- Satellite imagery: Pléiades data (acquired June 2016) used for tree density within each 1-ha plot; spatial resolution 0.5 m (panchromatic) and 2.0 m (multispectral, resampled to 2 m).
- LiDAR data: Airborne LiDAR collected on 5 November 2014 with a Leica LiDAR50-II on a Dornier 228-201 at 1850 m; Pulse density ~7.3 per m2; full waveform captured but discretised for processing (up to four returns per pulse).
- Georeferencing: Ground control tied to a Leica base station; data delivered in LAS format and processed with LAStools.
- Outputs: Digital elevation model (DEM) at 1 m resolution; normalised point cloud; canopy height model (CHM) at 0.5 m resolution; holes in CHM filled by spatial averaging.

## Data processing workflow

- Software and tools: LAStools for LiDAR processing; R (raster package) for statistics; itcSegment package in R for tree crown segmentation; Pléiades imagery for calibration data.
- Preprocessing steps:
  - Classify LiDAR points into ground and non-ground; create DEM from ground returns.
  - Subtract DEM from non-ground elevations to create normalised point cloud.
  - Build CHM from first returns; resample/interpolate to 0.5 m; fill missing CHM values.
- Calibration plots: Use central 1-ha plots (surrounding the 0.0625-ha field plots) and field heights to calibrate LiDAR-derived metrics to ACD.

## Carbon density estimation methods

- Palm biomass model:
  - AGB_palm (dry mass per palm) = 37.47 × height + 3.6334 (height in metres).
  - Convert to carbon with a factor of 0.47 (ACD = total biomass × 0.47).
  - Note: Palm trunks do not thicken with age; diameter not used in the biomass equation.

- Area-based approach (top-of-canopy height):
  - TCH: mean height of CHM pixels within each 1-ha calibration plot.
  - Model: ACD = a × (TCH)^b (nonlinear least squares).
  - Calibration: fitted to the 27 1-ha plots; accuracy assessed with leave-one-out cross-validation (LOOCV).

- Canopy cover (CC) approach:
  - CC: fraction of area occupied by crowns above ground, computed by creating a horizontal plane at height h and measuring the proportion of CHM pixels below the plane.
  - Models: ACD = a × (CC)^b; tested across heights h from 1 m to the maximum canopy height (up to ~23 m).
  - Purpose: evaluate CC as an alternative LiDAR-derived predictor for ACD.

- Tree-centric (ITC) approach:
  - Crown delineation: use itcSegment to identify individual tree crowns (adjusted for oil palm plantation structure).
  - Processing steps in three stages: (1) Gaussian smoothing of CHM; (2) iterative detection of local maxima (tree tops) with variable window size; (3) region-growing around maxima with crown width/depth constraints and a weighting exponent to improve segmentation.
  - Height correction: account for overestimation of tree height by ITC due to palm fronds arching above meristem; nonlinear regression used to derive a correction factor relating field height (Hc) and LiDAR height (HITC); applied to obtain corrected crown heights for biomass estimation.
  - Biomass calculation: compute biomass per delineated crown using corrected heights; sum across crowns within plots; convert to ACD using the 0.47 carbon factor.
  - Validation: compare delineated crown counts with field observations; LOOCV used to assess ITC-derived ACD accuracy.

## Validation, assumptions, and limitations

- Calibration and validation:
  - LOOCV used for area-based model (ACD vs. TCH).
  - ITC approach validated by field crown counts and cross-plot height comparisons.
- Assumptions:
  - 1-ha calibration plots have homogeneous stand structure; average height from field plots is representative of the surrounding 1-ha area.
  - Oil palm plantations are managed uniformly; interrow spacing (~8 m) aids canopy discrimination in high-resolution LiDAR data.
- Limitations and considerations:
  - Spatial autocorrelation acknowledged in the 1-ha calibration plots for area-based approaches.
  - Data integration challenges typical for GIS-based carbon mapping: multiple sources (field plots, LiDAR, high-res imagery) require careful co-registration and calibration.
  - Focus on oil palm plantations implies results may differ in mixed tropical forests or non-uniform stands.

## Data products and outputs

- LiDAR-derived metrics:
  - CHM-based top-of-canopy height (TCH) per 1-ha plot.
  - Canopy cover (CC) metrics across height levels.
  - Individual tree crown (ITC) delineations and corrected crown heights for palm trees.
- Carbon density estimates:
  - Area-based ACD estimates per 1-ha calibration plots (and extrapolated to larger areas via the calibration model).
  - Tree-centric ACD estimates aggregated from ITC biomass sums.
  - Converts biomass to carbon using a fixed 0.47 factor.
- Data integration: calibration with Pléiades density data to anchor field-based counts and corroborate LiDAR-derived height metrics.

## Key takeaways for GIS practitioners

- A robust LiDAR-based workflow can estimate aboveground carbon density in managed tropical plantations by integrating high-resolution LiDAR metrics (CHM, TCH, CC) with field measurements.
- Area-based, canopy-cover, and tree-centric approaches offer complementary perspectives; LOOCV and field counts are essential for assessing accuracy.
- Accurate palm-specific biomass modeling necessitates height-based allometric equations and a correction step to account for palm frond geometry in LiDAR-derived heights.
- High-resolution imagery (Pléiades) can support calibration by providing tree density and computing calibration plots, but assumptions about homogeneity and stand structure should be documented.
- The workflow demonstrates an end-to-end GIS-ready pipeline: data acquisition (LiDAR and Pléiades), preprocessing (DEM/CHM creation), metric extraction (TCH, CC, ITC), model calibration, and generation of spatially explicit ACD products.