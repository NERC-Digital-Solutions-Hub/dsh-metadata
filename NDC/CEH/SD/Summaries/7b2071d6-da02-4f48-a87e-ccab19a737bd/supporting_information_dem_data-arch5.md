# Digital elevation model of the Evoflood experiments, elevation data of the experimental river: supporting information

## Overview
- The dataset repository contains two data types: XYZ DEM files (elevation data) and an experimental_parameters.csv file (experimental metadata).
- Collected from a 10 m long, 2.5 m wide flume (Total Environment Simulator, University of Hull) to study morphological evolution of an alluvial river under varying discharges.
- Data collection occurred between September and December 2021 using a fixed-position 3D terrestrial laser scanner (Faro Focus X330).

## Data contents and structure
- XYZ data (DEM_i.csv): DEMs with i ranging from 0 to 137, where X/Y are pixel coordinates and Z is elevation in meters; a value of 999999 indicates no data for a pixel.
- Experimental parameters file (experimental_parameters.csv): contains time (seconds), water discharge (L/min), and morphological characteristics extracted from the DEMs; units are raw (width in pixels, depth in meters, conveyance in pixel.meters).
- Data processing outputs:
  - Scans are reoriented using seven fixed targets; scans with reorientation error > 0.5 mm are redone.
  - Pre-processing with CloudCompare to isolate the experimental area (remove wall/instrument), then converted to TIFF for Python analysis.
  - A regularly spaced grid (0.5 x 0.5 cm cells) is created by subsampling the point cloud, producing a grid of 2100 rows x 477 columns to enable DEM comparison.
  - Python routines generate the XYZ files from the processed DEMs.

## Data collection and quality controls
- Acquisition: High-resolution scans conducted at intervals tied to discharge conditions (base flow ~1 hour, medium flow ~45 minutes, high flow ~30 minutes); scan duration ~10 minutes per capture.
- Spatial reference: Scans reoriented to a known seven-target framework; exact reorientation error tracked and kept below 0.5 mm.
- Data completeness and cleanliness: The experimental area is cropped to exclude walls and instruments; only dry surfaces are scanned (wet areas yield -999999 for missing data).
- Accuracy: Scanner positional and surface measurement errors are approximately ±1 mm for the point cloud; the regular grid ensures consistent comparability across DEMs.

## Metadata and derived metrics
- Slope and detrending: Average channel slope calculated and used to detrend DEMs.
- Active floodplain definition: Areas with elevation below zero are considered active; areas above zero require floodplain conveyance capacity to be exceeded to be inundated.
- Floodplain metrics:
  - Average depth: mean elevation of the area below zero.
  - Floodplain width: average number of below-zero pixels per row, across the channel length.
  - Conveyance capacity: CC = Width x Depth (expressed in pixel.m units, averaged along the channel).
- Described fields in the experimental_parameters context:
  - Index (i), Time_(min), Qw_(L/min), DEM_name, Slope, dS, Width_(pixel), D_w, Depth_(m), D_d, Conveyance_(pixel.m), D_cc.

## Governance, access, and reuse considerations
- Data are stored as two main components (DEM files and experimental parameters) with explicit file naming (DEM_i.csv, DEM_name) to support traceability and reproducibility.
- Quality assurance is baked into the workflow (target-based reorientation checks, dry-surface scanning, background removal, and standardized gridding) to ensure trustworthy sharing-ready data.
- Documentation of processing steps (CloudCompare workflows, TIFF conversion, Python analysis) supports reuse and auditing of methods.
- Users should consult the experimental_parameters.csv for context (timing, discharges) when interpreting DEM-derived metrics.

## Key notes and caveats for data stewards
- Wet conditions impede data capture, leading to placeholder -999999 values in affected pixels.
- Spatial reference is based on pixel coordinates within the produced grid; no explicit georeferencing coordinates are described (interoperability considerations may apply if integrating with geospatial systems).
- Scanner and processing limitations include a nominal elevation error of ~±1 mm and a reorientation threshold of 0.5 mm.

## Summary of purpose and utility
- Enables analysis of floodplain evolution and river morphology under controlled discharge variations.
- Provides a reproducible workflow from raw TLS scans to gridded DEMs and derived floodplain metrics (slope, width, depth, conveyance capacity).
- Facilitates comparative studies across multiple DEMs through a consistent sampling grid and defined active floodplain criteria.