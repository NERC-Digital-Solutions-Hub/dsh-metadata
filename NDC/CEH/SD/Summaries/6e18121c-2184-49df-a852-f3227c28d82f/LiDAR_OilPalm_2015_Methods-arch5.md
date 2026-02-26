# Above-ground carbon density derived from LiDAR data over oil palm plantations in Malaysian Borneo, 2014

## Overview
- Study within the SAFE Degradation Landscape in Sabah, Malaysian Borneo, examining land-use change from forest to oil palm plantations.
- Focus on estimating aboveground carbon density (ACD) using LiDAR-derived canopy height and supporting field and satellite data.
- Data span field plots, airborne LiDAR, and Pléiades satellite imagery to calibrate and validate carbon estimates.

## Data and study context
- Location: Stability of Altered Forest Ecosystem (SAFE) landscape, East Sabah, tropical lowland forest region.
- Field sampling: 27 vegetation plots (25 m × 25 m; 0.0625 ha) laid out with a triangular design; plots across three plantation blocks with two ages (OP1 and OP2: 8 years; OP3: 14 years).
- Plantation context: Oil palm grown on flat terrain; consistent management across sites, enabling homogeneous canopy assumptions for calibration.
- Plot centers: 1-ha plots created around each 0.0625-ha plot for calibration and validation of LiDAR-based estimates.
- Data sources: 2014 airborne LiDAR, 2016 Pléiades satellite imagery, and field height measurements from 2013–2015.

## Data collection and processing
- LiDAR data
  - Acquisition: 5 November 2014, Leica LiDAR50-II, at 1850 m, 135 knots, ~7.3 returns/m2.
  - Processing: LAS format; ground/non-ground classification; digital elevation model (DEM) at 1 m; normalized point cloud; canopy height model (CHM) at 0.5 m; hole filling by neighborhood averaging.
- Satellite data
  - Pléiades (June 2016): 0.5 m panchromatic, 2.8 m multi-spectral (resampled to 2 m); used for tree density counts within 1-ha plots.
- Field measurements
  - Palm height (H) used to estimate individual aboveground biomass (AGB_palm) with the equation AGB_palm = 37.47 × H + 3.6334 (dry mass, kg).
  - Carbon content: 0.47 conversion factor applied to biomass to yield ACD.

## Methods for estimating aboveground carbon density
- Area-based approach
  - Model: ACD = a × TCH^b, relating ACD to mean top-of-canopy height (TCH) from the CHM within each 1-ha plot.
  - Calibration: Fitted using least-squares regression with data from the 27 1-ha plots; validation via leave-one-out cross-validation.
  - Canopy cover (CC) alternative: ACD = a × CC^b, where CC is the fraction of the plot occupied by canopy at a height above ground; CC calculated via CHM planes at varying heights.
- Tree-centric approach
  - ITC segmentation: Used itcSegment (R) to delineate individual tree crowns from the CHM, adapted for oil palm monocultures.
  - Delineation steps: Gaussian smoothing; local maxima detection for crown tops; region-growing constrained by crown width/depth; weighting exponent added to improve segmentation in oil palm stands.
  - Height correction: Because oil palm fronds elevate crown tops beyond the meristem, a nonlinear correction factor was derived to align LiDAR-derived heights (H_ITC) with field-estimated heights (H_CMC), yielding corrected tree heights (H_c).
  - Biomass and carbon: Convert segmented tree heights to AGB using the same height-based biomass relationship, sum across crowns, and multiply by 0.47 to obtain ACD estimates.
  - Validation: Compared ITC-derived counts with field counts and ACD predicted from summed biomass; corrections and model parameters estimated via nonlinear least-squares with LOOCV validation.
- Data provenance and reproducibility
  - Datasets generated: LiDAR-derived CHM and TCH, CC metrics, ITC delineations, per-plot ACD estimates, and per-tree biomass estimates.
  - Tools: LAStools for LiDAR processing; R packages for canopy metrics and ITC segmentation; open-source itcSegment for individual tree crown delineation.
  - Reference data: Field measurements, Pléiades-derived tree density counts, published allometric relationships and carbon conversion factors.

## Key findings and approaches
- Compared three estimation pathways: area-based (TCH), area-based (CC), and tree-centric (ITC) approaches.
- ITC approach required height correction to align LiDAR-derived heights with ground measurements, improving accuracy for oil palm plantations.
- The area-based approach (TCH) provided a robust calibration path when field measurements were aligned with LiDAR-derived canopy metrics.
- CC-based approach offered an alternative LiDAR metric but was less emphasized than TCH and ITC in final ACD estimation.
- All methods relied on a consistent carbon conversion factor (0.47) to translate biomass to carbon stock.

## Data management considerations for Data Stewards
- Data standards and formats
  - LiDAR: LAS format with ground/non-ground classifications; CHM and DEM rasters at 0.5–1 m resolutions.
  - Satellite data: Pléiades imagery with high-resolution counts for plot-level calibration.
  - Field data: plot-level measurements (heights, counts) and derived biomass estimates.
- Metadata and provenance
  - Document data sources, acquisition dates, sensors, processing steps, calibration/validation procedures, and model parameters.
  - Capture allometric relationships and carbon conversion factors used.
- Data quality and governance
  - Acknowledge potential biases: spatial autocorrelation within 1-ha calibration plots; homogeneity of plantation stands; temporal offsets between LiDAR (2014) and Pléiades (2016).
  - Record limitations and uncertainties from model fits (e.g., parameters a, b in ACD = a × TCH^b; CC model parameters).
- Reproducibility and sharing
  - Provide access to processing scripts (R code for CHM extraction, TCH calculations, CC computation, ITC segmentation, and nonlinear calibration).
  - Share processed datasets (per-plot ACD, per-tree biomass estimates, corrected heights) and the underlying raw data where permissible.
  - Align with data governance and sharing policies of the SAFE project and Malaysian Borneo datasets.

## Practical implications for reuse
- The study demonstrates robust methods for deriving carbon density from LiDAR in oil palm landscapes, with explicit calibration to field measurements and cross-validation.
- The combination of area-based and tree-centric methods, plus explicit height corrections, offers a framework adaptable to other monoculture plantation contexts.
- Results support landscape-scale carbon accounting and monitoring within degraded-forest and plantation conversion settings, informing governance and certification efforts.

## Endnotes and references
- Core methodological sources include Asner & Mascaro (2014) for LiDAR-based ACD estimation, Dalponte et al. for tree crown delineation, and foundational LiDAR data processing references.
- Data processing tools cited: LAStools, itcSegment (R), and supporting R packages for canopy metrics and validation.
- Relevant context and calibration references span field measurements, allometric biomass relationships, and carbon content factors used in converting biomass to carbon stock.