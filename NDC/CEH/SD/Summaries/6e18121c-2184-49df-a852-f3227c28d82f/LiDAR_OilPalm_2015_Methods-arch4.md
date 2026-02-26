# Above-ground carbon density derived from LiDAR data over oil palm plantations in Malaysian Borneo, 2014 Nunes, M.H, Ewers, R.M., Tuner, E.C., Coomes, D.A. (2017)

## Overview
- Objective: estimate aboveground carbon density (ACD) in oil palm plantations using airborne LiDAR, and compare area-based and tree-centric approaches calibrated with field data.
- Data sources: field plots within the SAFE Degradation Landscape; airborne LiDAR (2014) and Pléiades satellite imagery (2016) for calibration/validation.
- Approaches: area-based ACD modeling using top-of-canopy height (TCH) and canopy cover (CC); tree-centric crown delineation (ITC) to sum individual tree biomass.
- Key outputs: plot- and area-level ACD estimates; methodologies cross-validated to assess accuracy; data processing pipelines documented (LAStools, R).

## Study Area and Field Data
- Location: Stability of Altered Forest Ecosystems (SAFE) landscape, Sabah, Malaysian Borneo (lowland dipterocarp forests).
- Conditions: tropical climate with >2000 mm/year rainfall; plots below 800 m altitude; land-use change includes forest-to-palm conversions.
- Field plots: 27 vegetation plots (25 m × 25 m, 0.0625 ha) set in 2010 with 2013–2015 height measurements; three plantation blocks (OP1 and OP2 planted 2006, OP3 planted 2000) totaling 8-year and 14-year-old plots.
- Measurements: palm heights (no diameter due to palm trunk growth characteristics); palm density estimated from Pléiades imagery; 1-ha calibration plots centered on each 0.0625-ha plot.

## LiDAR Data Acquisition and Processing
- LiDAR: collected on 5 November 2014 using Leica LiDAR50-II; flight altitude ~1850 m, 135 knots, footprint ~40 cm, ~7.3 returns per m²; data stored in LAS format.
- Processing: ground-classified points to create a 1 m DEM; non-ground returns used to create canopy height model (CHM) at 0.5 m resolution; holes filled via neighborhood averaging.
- Georeferencing: ensured with concurrent Leica base station data.

## Data Used for ACD Estimation
- Palm biomass: AGB_palm = 37.47 × H + 3.6334 (H = palm height); carbon conversion factor = 0.47.
- Calibration/validation data: 27 one-hectare plots used to link field measurements with LiDAR-derived metrics; Pléiades imagery used to estimate tree density within each 1-ha plot.

## Area-Based ACD Approaches
- Canopy height method: ACD = a × (TCH)^b, where TCH is the mean height from the CHM within a 1-ha plot; parameters a and b estimated via nonlinear least squares; model fitted using leave-one-out cross-validation (LOOCV).
- Canopy cover method: ACD = a × (CC)^b, where CC is the proportion of canopy area above a height threshold; CC computed by slicing the CHM at height h and calculating the occupied fraction.
- Tree density context: both TCH and CC approaches rely on LiDAR-derived canopy characteristics to infer total ACD at the plot level.

## Tree-Centric ACD Estimation
- ITC segmentation: delineation of individual tree crowns using the itcSegment algorithm (R) with a Gaussian smoothing, local maxima detection, and region-growing constrained by crown size parameters.
- Height correction: adjust LiDAR-derived tree heights to better match field-height measurements, using a nonlinear regression to derive a correction factor that accounts for palm frond architecture.
- Biomass and carbon: biomass per tree estimated from corrected heights; summed across crowns per plot; converted to carbon with factor 0.47.
- Validation: accuracy assessed by comparing delineated tree counts with field counts and by comparing ITC-derived ACD with field-calibrated ACD.

## Validation and Quality
- LOOCV used to assess model performance for area-based relations (TCH and CC).
- ITC delineation accuracy checked against field-observed tree counts.
- Acknowledges potential spatial autocorrelation and homogeneous plantation conditions that may influence model performance.

## Data Management and Reusability
- Data and methods described to enable reproducibility: LAS-format LiDAR data, CHM rasters, 1-ha plot aggregation, R-based ITC segmentation, and reference pipelines (LAStools).
- Transparent documentation of calibration steps, model formulations, and validation procedures to support cross-site comparisons and data system coherence.

## Key Notes and Implications
- The study demonstrates multiple avenues to estimate ACD in oil palm landscapes using LiDAR for calibration, including area-based and tree-centric approaches.
- Palm-specific growth patterns (height-driven AGB without diameter increases) necessitate tailored biomass equations and height corrections.
- Integration of field data, high-resolution LiDAR, and Pléiades imagery provides a robust framework for assessing aboveground carbon in plantation-dominated landscapes.
- Data-centric emphasis on reproducibility and cross-method validation informs data leaders about practical workflows, data quality considerations, and the importance of metadata and standardization in complex, multi-source carbon accounting efforts.