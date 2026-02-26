# Above-ground carbon density derived from LiDAR data over oil palm plantations in Malaysian Borneo, 2014

## Overview
- Investigates LiDAR-based estimation of aboveground carbon density (ACD) in oil palm plantations within Sabah, Malaysian Borneo, using the SAFE Degradation Landscape context.
- Compares three approaches to derive ACD from LiDAR and field data: area-based, canopy cover–based, and tree-centric crown delineation.
- Aims to inform monitoring frameworks by linking remote-sensing metrics to biomass and carbon stock estimates, with validation against ground measurements.

## Study Area and Field Data
- Location: SAFE landscape in East Sabah, Malaysian Borneo; focus on oil palm expansion in lowland dipterocarp forests.
- Plot design: 27 vegetation plots (25 m × 25 m) established in 2010 for regional forest attributes; plots arranged across three oil palm blocks of different ages (OP1 and OP2 planted 2006; OP3 planted 2000).
- Field measurements: In each 0.0625 ha plot, palm stems tallied and heights measured in 2013 and 2015; average height used for analyses.
- Calibration/validation extension: 1-ha plots centered on each 0.0625-ha subplot to interpolate between field plots and LiDAR data; tree density visually counted from Pléiades imagery (0.5 m panchromatic, 2 m multispectral) acquired June 2016.
- Palm-specific considerations: Palm trunks do not thicken with height, so biomass equations rely on height alone; homogeneous plantation management assumed for calibration.

## LiDAR Data Acquisition and Processing
- Data collection: Airborne LiDAR (Leica LiDAR50-II) on 5 November 2014; altitude ~1850 m; 83.1 Hz, 12° FOV, ~40 cm footprint; average pulse density ~7.3/m^2.
- Processing workflow: Data stored in LAS format; ground vs non-ground classification; digital elevation model (DEM) at 1 m; canopy height model (CHM) at 0.5 m; holes filled by neighborhood averaging.
- Data integration: Pléiades imagery used to estimate tree density within 1-ha calibration plots; average height for 1-ha plots assumed from center 0.0625-ha plots.

## Estimation Approaches

### Area-Based ACD Using Top-of-Canopy Height (TCH)
- Model: ACD = a × (TCH)^b, where TCH is the mean canopy height within a 1-ha plot.
- Calibration: Fitted with least-squares regression using field AGB-derived biomass scaled to carbon (factor 0.47) and validated via leave-one-out cross-validation.
- Purpose: Leverages LiDAR-derived height as a scalable proxy for aboveground carbon in plantation mosaics.

### Canopy Cover (CC)–Based ACD
- Model: ACD = a × (CC)^b, where CC is the proportion of CHM cells above a height threshold (h) in the plot.
- CC calculation: Create a horizontal plane at height h and compute the fraction of CHM cells above the plane.
- Comparison: Assesses whether CC provides complementary or alternative predictive power to TCH for ACD estimation.

### Tree-Centric Crown Delineation (ITC) Approach
- Crown delineation: Use itcSegment in R to identify individual tree crowns from CHM, after smoothing with a Gaussian low-pass filter; locate local maxima representing crown tops; region-growing to define crowns with height- and width-constrained parameters.
- Height correction: Since oil palm fronds can elevate apparent tree height, apply a nonlinear correction to align LiDAR-based crown heights with field measurements; parameters estimated via nonlinear least-squares using a leave-one-out scheme.
- Biomass estimation: Compute AGB for each delineated crown from corrected heights; sum across crowns and multiply by 0.47 to obtain ACD.
- Validation: Compare the number of delineated trees to field counts and assess how summed ITC biomass predicts plot-level ACD.

## Calibration, Validation, and Uncertainty
- Cross-validation: Leave-one-out approach used to validate area-based ACD and ITC-derived biomass.
- Validation data sources: Field-measured heights and counts, Pléiades-derived tree density, and LiDAR-derived CHM.
- Uncertainty considerations: Palm-specific allometry (height-only model), potential autocorrelation in 1-ha calibration plots, and homogeneity assumptions in plantations; dimorphism between palm fronds and trunk metrics addressed via height corrections.

## Data, Tools, and Reproducibility
- Data sources: Field plots (2010–2015), airborne LiDAR (2014), Pléiades imagery (2016).
- Processing tools: LAStools for LiDAR processing; R packages for CHM computations and ITC crown segmentation; open-source methods (e.g., itcSegment) adapted for oil palm canopies.
- Biomass and carbon conversion: AGB palm equation based on height; carbon conversion factor of 0.47.

## Implications for Monitoring Frameworks
- Demonstrates feasible integration of ground measurements, LiDAR-derived canopy metrics, and high-resolution imagery to monitor carbon stocks in oil palm landscapes.
- Provides three complementary methods (area-based, CC-based, and tree-centric) to estimate ACD, enabling flexible monitoring at different scales and data availability.
- Highlights the importance of calibration with field plots and careful handling of species-specific allometry (palm height-centric biomass estimation) for policy-relevant carbon accounting.
- Indicates potential data and methodological considerations for governance: data accessibility, metadata quality, and harmonization across datasets to support transparent reporting and decision-making.

## Key Considerations for Practitioners
- When applying similar monitoring frameworks, ensure robust ground-truth data for calibration and validate LiDAR-derived metrics against field measurements.
- Consider multiple LiDAR-derived predictors (TCH, CC) and alternative methods (ITC-based) to triangulate ACD estimates.
- Account for crop-specific growth forms (e.g., oil palm frond geometry) that affect height-based biomass estimates.
- Be mindful of data governance barriers, such as data sharing and metadata completeness, which can influence the transparency and reuse of monitoring outputs.