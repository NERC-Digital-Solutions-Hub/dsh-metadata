# Digital elevation model of the Evoflood experiments, elevation data of the experimental river: supporting information

## Overview
- Data repository documenting digital elevation models (DEMs) and related experimental parameters from Evoflood flume experiments studying river morphology under varying discharges.
- Setup: 10 m long, 2.5 m wide flume (Total Environment Simulator, University of Hull, UK) simulating an alluvial river.
- Data types: XYZ point-cloud files (elevations) and an experimental_parameters.csv table.
- Purpose: track morphological evolution of the experimental river and derive floodplain characteristics to evaluate conveyance under flood conditions.
- Workflow: scans obtained, reoriented, processed, and converted to TIFF DEMs for analysis with Python.

## Data types and collection
- XYZ_i.csv: elevation data for scan i (i = 0 to 137). Z value of 999999 indicates no data for that pixel.
- Scan details: overhead 3D terrestrial laser scanner (Faro Focus X330); seven fixed targets used for reorientation; reorientation error must be < 0.5 mm.
- Scanning cadence: base flow every 1 hour; medium flow every 45 minutes; high flow every 30 minutes (exact intervals documented in experimental_parameters.csv).
- Practical constraints: surface must be dry for scanning; wet surfaces produce -999999 values.
- Pre-processing: CloudCompare used to isolate the experimental area, remove walls/instruments, and export to TIFF for analysis.
- Point cloud: initially with vertical/horizontal errors ~±1 mm; subsampled to a regular grid (0.5 cm grid cells) to enable DEM comparison.
- DEM grid: 2100 rows × 477 columns; consistent grid across scans for tracking morphological change.

## Processing and analysis
- DEM generation: from the reoriented scans, converted into regularly spaced raster grids for comparison.
- Morphological extraction (via Python): analyze DEMs to derive channel and floodplain characteristics.
- Slope and detrending: average channel slope computed and used to detrend DEMs.
- Active floodplain definition: areas with elevation below zero after detrending; areas above zero are inundated only when floodplain conveyance capacity is exceeded.
- Floodplain metrics:
  - Average floodplain depth: mean elevation of the below-zero area.
  - Floodplain width: average number of below-zero pixels per row along the channel length.
  - Conveyance capacity: CC = W × D (width × depth) averaged along the river length (expressed in pixel.m).
- DEM-derived metrics are stored alongside supplementary fields for each time point (see table below).

## Experimental parameters and derived metrics
- Table experimental_parameters.csv provides:
  - Time (seconds) and water discharge at the inlet (Qw in L/min) corresponding to each scan.
  - DEM file name associated with each time point.
  - Morphological metrics extracted from the DEM: slope (S), slope error (dS), width (Width_pixel) and its error (D_w), depth (Depth_m) and its error (D_d), conveyance capacity (Conveyance_pixel.m) and its error (D_cc).
- Derived values are computed from the DEMs (e.g., width, depth, conveyance) and aggregated across the study channel.

## Data quality, accessibility, and governance
- Quality controls: scans reoriented with stringent error threshold (< 0.5 mm); only accepted scans used for DEM construction.
- Data gaps: presence of -999999 values indicates unobserved or invalid data (e.g., surface not dry during scan).
- Metadata and reproducibility: experimental parameters accompany DEMs to enable replication of morphological calculations (slope detrending, active floodplain delineation, and CC computation).
- Data handling considerations: raw and processed data require explicit data processing steps (CloudCompare, TIFF conversion, Python analysis) to reproduce results.

## Relevance for monitoring frameworks
- Demonstrates a end-to-end workflow for generating high-resolution environmental monitoring data (from acquisition to derived metrics) suitable for evaluating flood response and floodplain capacity.
- Highlights practical monitoring challenges: data gaps, data standardization, data governance, and transparent reporting of methods and uncertainties.
- Provides a structured set of metrics (slope, width, depth, conveyance, and derived conveyance capacity) that can inform policy decisions on flood risk management and river health monitoring.
- Emphasizes the importance of metadata, data sharing, and methodological transparency to support data-driven decision making in environmental health monitoring.