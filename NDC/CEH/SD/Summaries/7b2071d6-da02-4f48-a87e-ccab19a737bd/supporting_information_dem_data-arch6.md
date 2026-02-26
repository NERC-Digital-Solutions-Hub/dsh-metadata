# Digital elevation model of the Evoflood experiments, elevation data of the experimental river: supporting information

## Overview
- A data repository with two data types: XYZ elevation files (DEMs) and the experimental parameters file.
- Purpose: study morphological evolution of a generic experimental alluvial river subjected to discharge variations in a 10 m long, 2.5 m wide flume at the Total Environment Simulator, University of Hull, UK.
- Data collected Sept–Dec 2021 using a fixed-position 3D laser scanner to monitor flood-induced morphological changes.

## Data contents
- DEM data: XYZ_i.csv files (i = 0 to 137) containing elevation data; X/Y are pixel coordinates, Z is elevation in meters; Z = 999999 indicates no data for that pixel.
- Experimental parameters: experimental_parameters.csv, listing time, water discharge, and morphological characteristics extracted from the DEMs.
- DEM processing: scans converted into TIFFs and analyzed with Python; the point cloud was subsampled onto a regular grid (0.5 × 0.5 cm cells) to enable comparison across DEMs.

## Data collection workflow
- Instrumentation: Faro Focus X330 terrestrial laser scanner, fixed above the experimental area; seven targets used for reorientation.
- Reorientation: scans reoriented in Faro Scene; only kept if reorientation error < 0.5 mm.
- Scanning cadence: base flow approximately every 1 hour, medium flow every 45 minutes, high flow every 30 minutes (exact timings in experimental_parameters.csv).
- Pre-processing: CloudCompare used to isolate the experimental area (remove wall/instrument), and to convert scans to TIFFs for analysis.
- Dryness requirement: surface must be dry for scanning; wet surfaces yield -999999 values.

## Data processing and analysis
- Point cloud processing: CloudCompare to create an evenly spaced raster grid (0.5 × 0.5 cm); grid structure: ~2100 rows × 477 columns.
- DEM generation: regular grid enables comparison of DEMs and tracking morphodynamic evolution.
- Analysis workflow (via Python):
  - Compute average channel slope and detrend the DEM.
  - Define active floodplain as areas with elevation below zero (after detrending).
  - Determine inundation: areas above zero are inundated only when floodplain conveyance capacity is exceeded.
- Outputs: DEMs and derived metrics stored in the dataset; XYZ files generated from the analysis.

## Experimental parameters and derived metrics
- Experimental parameters (experimental_parameters.csv) include:
  - Time (seconds) and water discharge (L/min) at the inlet.
  - Morphological characteristics extracted from the DEMs.
- Units:
  - Width: pixels
  - Depth: meters
  - Conveyance capacity: pixel·meter
- Derived metrics:
  - Slope (m/m) and its error (dS)
  - Floodplain width (Width_(pixel)) and its error (D_w)
  - Floodplain depth (Depth_(m)) and its error (D_d)
  - Conveyance capacity CC (in pixel·meter) and its error (D_cc)
- Floodplain analysis approach:
  - Active floodplain defined by negative elevation after slope detrending.
  - Conveyance capacity = average floodplain width × average floodplain depth along the channel.

## Data quality and notes
- Data quality checks include reorientation accuracy and ensuring the surface remains dry during scanning to avoid missing data.
- Missing data flagged as -999999 when scans cannot capture submerged areas.
- The dataset provides both raw XYZ DEMs and the associated experimental parameters for reproducibility and further analysis.

## Potential uses
- Time-resolved analysis of river morphodynamics under varying flood discharges.
- Comparative studies of DEMs across flood events to understand channel evolution.
- Development of self-contained data products (e.g., morphometric time series, conveyance capacity trends) for use by researchers and practitioners in fluvial geomorphology.