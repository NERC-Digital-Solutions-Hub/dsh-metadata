# Above-ground carbon density derived from LiDAR data over oil palm plantations in Malaysian Borneo, 2014

- Objective
  - Estimate aboveground carbon density (ACD) in oil palm plantations using LiDAR-derived canopy metrics.
  - Compare three analytical approaches (area-based with top-of-canopy height, canopy-cover based, and tree-centric individual crowns) and validate against field data.

- Study area and context
  - SAFE Degradation Landscape, Sabah, Malaysian Borneo; lowland tropical forest region heavily impacted by forest-to-palm conversions.
  - Study plots: 27 vegetation plots (25 m × 25 m) across three oil palm plantation blocks with two ages (OP1 and OP2 at ~8 years; OP3 at ~14 years).

- Field data
  - Within-plot measurements of oil palm height (2013–2015; average height per 0.0625 ha plot used).
  - Palm diameter not used due to palm growth biology (no secondary thickening with height).
  - 1-ha calibration plots centered on each 0.0625-ha plot; Pléiades imagery used to count tree density within each 1-ha plot (0.5 m panchromatic, 2 m multispectral data, resampled to 2 m).

- LiDAR data and processing
  - Airborne LiDAR (Leica LiDAR50-II) collected 5 Nov 2014; ~1850 m altitude, 7.3 returns per m²; 40 cm footprint.
  - Data processed to produce a digital elevation model (DEM; 1 m resolution) and a canopy height model (CHM; 0.5 m resolution) from normalized point clouds.
  - Ground and non-ground classification; holes in CHM filled by neighborhood averaging.

- Biomass and carbon estimation (palm-based)
  - Aboveground biomass per palm: AGB_palm = 37.47 × H + 3.6334 (H = height in metres).
  - Palm diameter not used; total AGB per 1-ha plot obtained by multiplying plot-mean AGB_palm by palm counts from Pléiades data.
  - Carbon content: convert AGB to carbon with a factor of 0.47.

- Area-based ACD estimation (TCH-based)
  - Model: ACD = a × (TCH)^b, where TCH is the mean canopy height within each 1-ha plot.
  - Calibration/validation: fitted to 27 1-ha plots; leave-one-out cross-validation (LOOCV) used to assess predictive performance.
  - TCH extracted from CHM via raster operations; comparison with alternative predictor (CC).

- Canopy-cover (CC) approach
  - CC defined as the proportion of CHM pixels beneath a horizontal plane at height h (1–23 m).
  - Model: ACD = a × (CC)^b.
  - Assessed across a range of height thresholds to identify predictive power relative to TCH.

- Tree-centric approach (ITCSeg)
  - Delineation of individual tree crowns (ITCs) using itcSegment in R (adapted for oil palm stands).
  - Steps: Gaussian smoothing of CHM, local maxima detection (tree tops), region-growing constrained by crown dimensions.
  - Height corrections: adjust LiDAR-derived crown heights to account for frond arching beyond trunk top; nonlinear regression used to derive correction (factor ~1.02× with height-based parameters).
  - Individual biomass estimation: convert ITC heights to AGB using calibrated relationships, sum across crowns, then convert to ACD with 0.47 carbon factor.
  - Validation: compare number of delineated trees with field observations and ACD predicted from summed ITC biomasses.

- Data and tools
  - Field and LiDAR data processed with LAStools; CHM derived from normalized LiDAR returns.
  - Pléiades imagery used for tree-count calibration; ITC segmentation implemented in R (itcSegment package).
  - Analytical framework aligns with standard approaches for calibrating LiDAR metrics to forest carbon density.

- Key implications for environmental monitoring
  - Demonstrates multiple LiDAR-based pathways (area-based, CC-based, and tree-centric) to estimate ACD in uniform oil palm landscapes.
  - Provides a calibration/validation workflow that can be replicated to monitor carbon stocks and policy-relevant environmental health over time.
  - Highlights the value of integrating field plots, high-resolution LiDAR, and satellite imagery to improve carbon-density assessments in managed plantation ecosystems.

- Limitations and considerations
  - Spatial autocorrelation potential in 1-ha calibration plots; plots are homogeneous but may affect model independence.
  - Oil palm architecture (frond height) requires correction factors in ITC-based biomass estimates.
  - Homogeneity of plantation management assumed; results may differ in more heterogeneous landscapes.