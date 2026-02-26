# Digital elevation model of the Evoflood experiments, elevation data of the experimental river: supporting information

- Overview
  - A data repository for two data types: XYZ elevation files and an experimental parameters file, generated from a 10 m long by 2.5 m wide flume to study how an alluvial river morphologies evolve under varying discharge.
  - Data collection occurred between September and December 2021 using a fixed-position 3D terrestrial laser scanner (Faro Focus X330); seven targets enabled re-orientation with high precision.

- Datasets Included
  - Digital Elevation Model (XYZ_i.csv) for i = 0 to 137, containing X and Y coordinates (pixels) and Z elevation (meters). Z = 999999 indicates no data for that pixel.
  - Experimental parameters file (experimental_parameters.csv) with time, water discharge, and extracted morphological characteristics for each DEM.

- Data Collection & Processing Workflow
  - Scanning protocol: scans captured at multiple flow regimes (base, medium, high) at intervals (roughly 1 hr, 45 min, 30 min), with a scan duration ~10 minutes each.
  - Re-orientation: each scan aligned using seven known targets; only scans with re-orientation error < 0.5 mm are accepted.
  - Pre-processing: CloudCompare used to isolate the experimental area (remove walls/instruments), then data converted to TIFF for analysis in Python.
  - Drying requirement: the surface must be dry for accurate scanning; wet surfaces yield -999999 values.
  - Rasterization: CloudCompare sub-sampled the point cloud to create a regularly spaced raster grid of 0.5 x 0.5 cm cells (2100 x 477 grid), enabling cross-DEM comparisons and analysis of floodplain evolution.

- Data Quality & Cleaning
  - Vertical/horizontal scanner errors are approximately ±1 mm; re-orientation error check ensures high positional accuracy.
  - Data under water are not visible by the scanner and are represented as -999999 in the DEMs.
  - The TIFF conversion and subsequent Python-based analysis rely on the regular 0.5 cm grid for consistent comparison.

- Data Structure & Key Fields
  - DEMs (XYZ_i.csv): i corresponds to the scan number; columns include X (pixel), Y (pixel), Z (elevation in meters); Z = 999999 means no data.
  - Experimental parameters (experimental_parameters.csv): fields include
    - i (index, matches DEM i)
    - Time_(min): time since experiment start (minutes)
    - Qw_(L/min): inlet water discharge (L/min)
    - DEM_name: associated DEM file name
    - Slope: average channel slope (m/m)
    - dS: error on slope (m/m)
    - Width_(pixel): river width in pixels (averaged along the length)
    - D_w: error on width (pixels)
    - Depth_(m): floodplain depth (meters, averaged)
    - D_d: error on depth (meters)
    - Conveyance_(pixel.m): conveyance capacity (width x depth) in pixel·meters
    - D_cc: error on conveyance capacity (pixel·meter)

- How to Use for GIS Purposes
  - Treat XYZ_i.csv as individual DEM rasters to analyze morphological changes over time, using the 0.5 cm grid resolution for high-detail spatial analysis.
  - Use the experimental_parameters.csv to link hydrological conditions (Qw) and morphological metrics (slope, width, depth, conveyance) with each DEM.
  - Define active floodplain as areas where elevation is below zero after detrending by the mean slope; areas above zero are inundated only when conveyance capacity is exceeded.
  - Create maps of:
    - Floodplain width and depth across the channel
    - Conveyance capacity (W x D) maps over time
    - Slope and detrended DEMs to assess morphological evolution
  - Use DEM_name to join spatial rasters with their corresponding parameter records for temporal GIS analyses and visualisation.

- Reproducibility & Tools
  - Tools used: Faro Scene for re-orientation, CloudCompare (v2.13, 2023) for rasterization and pre-processing, Python for DEM analysis, TIFF as the analysis-friendly raster format.
  - Data products are designed for map-based visualisation and spatial analysis, aligning with GIS workflows that integrate raster DEMs with attribute data from the experimental_parameters file.

- Limitations & Considerations
  - Data rely on adequate drying and precise scan alignment; any residual moisture can affect data validity.
  - The DEMs have missing data indicated by -999999, and units are in meters for elevation with pixel-based measurements for width and conveyance.
  - Coordinate reference system isn’t specified; users should verify alignment with their GIS environment before integrating with other spatial datasets.