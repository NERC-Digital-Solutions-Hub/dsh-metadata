# Above-ground carbon density derived from LiDAR data over oil palm plantations in Malaysian Borneo, 2014

- Study area and context
  - SAFE Degradation Landscape: oil palm plantations within the Stability of Altered Forest Ecosystem (SAFE) project in Sabah, Malaysian Borneo; region characterized by forest-to-palm conversion and industrial harvesting.
  - Climate and topography: tropical with >2000 mm/year rainfall; plots below 800 m altitude; mixed sedimentary geology.
  - Plantation blocks: three oil palm blocks (OP1 and OP2 planted in 2006; OP3 planted in 2000), with 8-year-old (OP1, OP2) and 14-year-old (OP3) plots.

- Field data collection
  - 27 vegetation plots (25 m × 25 m; 0.0625 ha) laid in 2010, North–South orientation, hierarchical sampling around a triangular design.
  - Palm measurements: stem height (H) for all oil palms within each 0.0625 ha plot, measured in 2013 and 2015; average heights across years used.
  - Palm growth characteristics: palms do not increase trunk diameter with height; no diameter measurements included.
  - Calibration framework: a 1-ha plot centered on each 0.0625-ha plot used to scale up to aboveground carbon density (ACD) calculations; Pléiades imagery used for tree density within each 1-ha plot.

- Remote sensing data and processing
  - LiDAR data: airborne LiDAR collected on 5 November 2014 using a Leica LiDAR50-II (1850 m altitude, 83.1 Hz, 12° FOV, ~40 cm footprint, ~7.3 returns per m²); data pre-processed to LAS format; ground and non-ground classes identified; digital elevation model (DEM) at 1 m; canopy height model (CHM) at 0.5 m; holes filled with neighborhood averaging.
  - Pléiades imagery: acquired June 2016; panchromatic 0.5 m resolution and multispectral 2 m resolution (resampled to 2 m); used to visually count tree density within 1-ha plots.
  - Data processing tools: LAStools for LiDAR processing; R (CHM rasters, plotting, and analyses); itcSegment package for individual tree crown segmentation.

- Aboveground carbon density (ACD) estimation approaches
  - Palm aboveground biomass (AGB palm): estimated from palm height using AGB_palm = 37.47 × H + 3.6334 (kg per palm); carbon content assumed as 0.47 (conversion to carbon density).
  - Area-based approaches
    - Top-of-canopy height (TCH) method: ACD = a × TCH^b, where TCH is the mean height of CHM pixels within each 1-ha plot; model parameters a and b estimated by nonlinear least squares; fitted using 27 1-ha plots; validated with leave-one-out cross-validation (LOOCV).
    - Canopy cover (CC) method: CC calculated by selecting a height threshold h and computing the proportion of CHM pixels below that plane; ACD = a × CC^b (parameters a, b similarly estimated and validated).
  - Tree-centric approach (ITC)
    - Delineation: used itcSegment to identify individual crowns from the CHM; involves smoothing the CHM, detecting local maxima as crown tops, and region-growing constrained by predefined crown width/depth.
    - Height correction: correction factor applied because LiDAR-derived ITC heights overestimate field heights due to fronds arching beyond trunk tops; a nonlinear regression model (parameters a and b) derived via LOOCV to align ITC heights with field measurements.
    - Biomass and ACD: biomass per ITC computed from corrected heights; sum across all ITCs within a plot, then convert to ACD using 0.47 carbon fraction.
    - Accuracy assessment: ITC delineation performance evaluated by comparing delineated tree counts to field counts and ACD predicted from summed ITC biomasses.

- Calibration, validation, and interpretation
  - Calibration data: 27 1-ha plots with field-measured heights and corresponding LiDAR-derived metrics (TCH and CC) used to calibrate area-based ACD models.
  - Validation approach: leave-one-out cross-validation to assess predictive performance of area-based and ITC methods.
  - Output and use
    - Generates plot-level ACD estimates and supports scaling to landscape-level carbon density in oil palm plantations.
    - Demonstrates complementary data streams (field measurements, LiDAR-derived metrics, and high-resolution imagery) to enable self-contained, repeatable ACD assessments.
    - Provides methodological framework for comparing area-based and tree-centric approaches in uniform agroforestry canopies, with explicit corrections for palm morphology.