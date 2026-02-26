# Above-ground carbon density derived from LiDAR data over oil palm plantations in Malaysian Borneo, 2014

## Study Area and Objective
- Within the Stability of Altered Forest Ecosystem (SAFE) Project in Sabah, Malaysian Borneo, an area characterized by large-scale forest-to-palm conversions and tropical climate with high rainfall.
- Objective: estimate aboveground carbon density (ACD) in oil palm plantations using LiDAR data, calibrated and validated with field plots and satellite imagery.

## Field Data
- 27 vegetation plots (25 m × 25 m, 0.0625 ha each) with North-South orientation, established in 2010.
- Plots distributed among three oil palm blocks of two ages: OP1 and OP2 planted in 2006 (8-year-old) and OP3 planted in 2000 (14-year-old).
- In each 0.0625 ha plot, all oil palms measured for height in 2013 and 2015; average height used for analysis.
- Palm diameter not measured because oil palms do not thicken with height; trunks lack secondary thickening.
- To extend plot scale, a 1-ha plot was centered on each 0.0625-ha plot, used for calibration/validation of LiDAR-based estimates.
- Pléiades satellite imagery (June 2016) used to visually count tree density within each 1-ha plot; imagery provides 0.5 m panchromatic and 2 m multispectral data (resampled to 2 m).

## LiDAR Data Acquisition and Processing
- Airborne LiDAR data collected on 5 November 2014 using a Leica LiDAR50-II, flown at 1850 m, 135 knots; 83.1 Hz pulse rate, 12.0° FOV, ~40 cm footprint; mean pulse density 7.3/m².
- Data processed in LAS format; ground points classified to create a 1 m DEM; non-ground points used to build a canopy height model (CHM) at 0.5 m resolution; holes filled by neighboring cell averaging.
- Processing performed with LAStools.

## Estimating Tree- and Plot-Level Aboveground Carbon Density
- AGB palm estimated from height (H) using: AGB_palm = 37.47 × H + 3.6334 (kg dry mass); since palm diameter does not track height, diameter is excluded from biomass equations.
- Carbon content converted to ACD using a factor of 0.47 (Martin and Thomas, 2011).

## Area-Based Approach
- Calibrated a general LiDAR-based model relating mean top-of-canopy height (TCH) to ACD using least squares regression: ACD = a × (TCH)^b.
- Model fitted to the 27 1-ha plots; predictions obtained via leave-one-out cross-validation.
- TCH per 1-ha plot derived as the mean height of CHM pixels within the plot.
- Explored canopy cover (CC) as an alternative LiDAR metric: CC computed by counting CHM pixels below a height threshold h; model ACD = a × (CC)^b tested as well.

## Tree-Centric Approach
- Delineated individual tree crowns (ITCs) in each plot using the itcSegment algorithm (R, CRAN) with adaptations for oil palm plantations.
- Process: smoothing of CHM, iterative local maxima detection as crown tops, region-growing constrained by prior crown size assumptions.
- To correct for overestimated LiDAR-derived heights due to palm fronds arching beyond the meristem, applied a nonlinear height correction factor based on field-measured heights (Hc) and LiDAR heights (HITC) from surrounding plots; the correction factor was approximately 1.02 and validated with leave-one-out procedures.
- Individual crown biomass calculated from corrected heights, then summed and converted to ACD using the same 0.47 carbon factor.

## Validation and Comparisons
- Compared ITC-derived ACD (summed crown biomasses) with ACD from the area-based approach and with field biomass estimates.
- The 1-ha calibration plots and leave-one-out cross-validation used to assess model performance and reliability.
- Data and methods rely on publicly available tools and references, including the itcSegment package and prior LiDAR-based biomass calibration studies.

## Key Data Points and Tools
- Field height averages by plantation age: OP1 6.1 ± 2.3 m; OP2 5.4 ± 1.5 m; OP3 8.5 ± 2.0 m.
- Pléiades imagery used to calibrate tree density and extend plot-scale analyses.
- Carbon conversion factor: 0.47 for palm biomass to carbon.
- Methods include area-based LiDAR ACD modeling (TCH), CC-based modeling, and tree-centric crown segmentation with height corrections.

## Implications and Notes
- The study evaluates multiple LiDAR-based strategies to estimate ACD in homogeneous oil palm plantations, highlighting the trade-offs between area-based calibration and individual-tree approaches.
- Palm architecture (frond arching) necessitates corrections when using ITC heights for biomass estimation.
- Findings inform best practices for mapping plantation-level carbon stocks using LiDAR and supporting comparisons with field measurements and satellite-derived data.