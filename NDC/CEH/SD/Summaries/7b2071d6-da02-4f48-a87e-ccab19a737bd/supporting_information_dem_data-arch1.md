# Digital elevation model of the Evoflood experiments, elevation data of the experimental river: supporting information

## Overview
- Contains two data types: XYZ elevation files and an experimental_parameters.csv file.
- Collected in a 10 m long, 2.5 m wide flume (Total Environment Simulator, University of Hull, UK).
- Purpose: study morphological evolution of an experimental alluvial river under varying flood discharges.
- Data collection period: September–December 2021.
- Scans performed at intervals tied to discharge conditions: base flow (1 h), medium flow (45 min), high flow (30 min); exact timings per the experimental_parameters file.
- Scans are reoriented using seven known targets; reorientation error must be below 0.5 mm, otherwise the scan is redone.
  
## Data contents

- XYZ_i.csv files (i = 0 to 137): elevation data for each scan.
  - Columns: X, Y (pixel coordinates); Z (elevation in meters).
  - Z = 999999 indicates no data for that pixel; missing data handling noted.
  - Data describe the morphological evolution of the river floodplain during multiple flood events.
  - Dry requirement: if the surface is not dry, scans return -999999 values.
  - Point cloud errors are about ±1 mm (vertical and horizontal).

- Experimental_parameters.csv: associated per-scan parameters and derived metrics.
  - Columns include: Time_(min), Qw_(L/min), DEM_name, Slope, dS, Width_(pixel), D_w, Depth_(m), D_d, Conveyance_(pixel.m), D_cc.
  - Time and discharge relate to the previous scan, and morphological characteristics are extracted from the corresponding DEM.
  - Units: width in pixels, depth in meters, conveyance capacity in pixel.meters, with corresponding error terms.

## Experimental setup and data acquisition

- Flume: 10 m length, 2.5 m width.
- Equipment: Faro Focus X330 3D terrestrial laser scanner; fixed position above the area.
- Scanning protocol:
  - Seven targets used for reorientation; scans accepted if reorientation error < 0.5 mm.
  - Scan duration ~10 minutes; time between scans detailed in experimental_parameters.csv.
- Pre-processing: CloudCompare used to crop to the experimental area (remove wall/instrument), then convert to TIFF for analysis in Python.
- Data readiness: to analyze with Python, DEMs are derived from the processed TIFFs.

## Data processing and quality control

- DEM construction: cloud points are sub-sampled to an evenly spaced raster grid (0.5 x 0.5 cm cells) using CloudCompare (2.13, 2023), resulting in a grid of 2100 rows x 477 columns.
- DEM analysis workflow:
  - Calculate average slope of the channel; detrend the DEM using this slope.
  - Define active floodplain as areas with elevation below zero after detrending.
  - Floodplain width (W): average number of below-zero pixels per row across the channel length.
  - Floodplain depth (D): average elevation of the area below zero.
  - Conveyance capacity (CC): CC = W * D (in pixel.m units), with associated error D_cc.
- Data quality notes:
  - Dry surface requirement prevents erroneous data; non-dry surfaces produce -999999 in the DEM.
  - Laser/point cloud errors are approximately ±1 mm.
  - Reorientation fails if error exceeds threshold, triggering a re-scan.

## Data structure and metadata

- XYZ_i.csv: series of DEMs for i = 0, 1, ..., 137 (138 scans total).
- experimental_parameters.csv: per-scan metadata and derived morphological metrics, including:
  - Time_(min): time since experiment start
  - Qw_(L/min): inlet water discharge
  - DEM_name: corresponding DEM file name
  - Slope, dS: average channel slope and its error
  - Width_(pixel), D_w: floodplain width and its error (in pixels)
  - Depth_(m), D_d: floodplain depth and its error (in meters)
  - Conveyance_(pixel.m), D_cc: conveyance capacity and its error (pixel.m)

## How to use for analysis and modeling

- Purpose-built to analyze how river morphology evolves under different flood discharges.
- Potential analyses:
  - Correlate Qw with conveyance capacity (CC) and with floodplain width (W) and depth (D) across time.
  - Investigate how slope changes relate to morphological adjustments and floodplain evolution.
  - Track temporal evolution of DEM-derived metrics (slope, W, D, CC) across different discharge regimes.
  - Build predictive models linking discharge, morphology, and conveyance capacity using the experimental_parameters time series.
- Key derived metrics provided in the dataset facilitate quick computation of floodplain accessibility and flood management implications.

## Limitations and considerations

- Data is from a single experimental setup (specific flume, geometry, and roughness); caution when generalizing to natural rivers.
- Data gaps or artifacts may occur if scans are not dry or if reorientation accuracy criteria are not met.
- Spatial resolution (0.5 cm grid cells) and processing steps (CloudCompare sub-sampling) influence small-scale feature interpretation.
- Consistency between missing-data codes (999999 vs -999999) should be handled carefully during analysis.