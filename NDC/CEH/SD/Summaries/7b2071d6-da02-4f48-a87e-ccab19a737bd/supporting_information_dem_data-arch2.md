# Digital elevation model of the Evoflood experiments, elevation data of the experimental river: supporting information

## Data types and structure
- Two data types are provided: XYZ files (elevation data) and an experimental parameters file.
- Experimental setup: a 10 m long and 2.5 m wide flume (Total Environment Simulator, University of Hull, UK) to study a generic alluvial river under varying discharges.
- DEMs are stored as XYZ_i.csv files with i ranging from 0 to 137 (138 scans in total).
- XYZ values: X and Y are pixel coordinates; Z is elevation in meters. A Z value of 999999 indicates no data for that pixel.
- The experimental parameters table complements the DEMs with time, discharge, and morphological metrics.

## Data collection and processing workflow
- Acquisition: elevation data collected Sep–Dec 2021 using a fixed-position overhead 3D terrestrial laser scanner (Faro Focus X330) at intervals chosen by flow condition (base ~1 h, medium ~45 min, high ~30 min).
- Orientation and quality control: scans reoriented using seven known targets; only scans with re-orientation error < 0.5 mm are kept.
- Scan duration and cadence: each scan ~10 minutes; interval timing is specified in the experimental parameters file.
- Pre-processing: CloudCompare used to isolate the experimental area (removing wall/instrument) and to convert scans to TIFFs for Python analysis.
- Dryness requirement: area must be dry for scanning; wet surfaces yield -999999 values.
- Data formatting: point clouds are sub-sampled to create a regular raster grid (0.5 x 0.5 cm cells) with 2100 rows and 477 columns, enabling cross-DEM comparison and morphological evolution assessment.
- Output production: DEMs are generated from Python-based analyses of the regularly spaced grid.

## Data quality, constraints, and handling
- Accuracy: laser-derived point cloud has vertical and horizontal errors ~±1 mm.
- Dry condition requirement: submerged areas cannot be scanned; such pixels are marked -999999.
- Re-orientation checks: strict threshold; otherwise scans are redone to ensure alignment reliability.

## Derived metrics and analysis methodology
- DEM analysis process:
  - Detrend DEMs using the average channel slope.
  - Define active floodplain as the area with elevation below zero; areas above zero are considered inundated only when floodplain conveyance capacity is exceeded.
  - Compute average floodplain depth as the mean elevation of the area below zero.
  - Determine floodplain width by averaging the count of below-zero pixels per row along the channel length.
  - Conveyance capacity (CC) is defined as CC = W × D, where W is width and D is depth, averaged across the river length.
- Morphological characteristics (from experimental_parameters.csv) include:
  - Time (seconds)
  - Water discharge at inlet (Qw, L/min)
  - DEM name
  - Slope (m/m) and slope error (dS)
  - Width (pixels) and width error (D_w)
  - Depth (m) and depth error (D_d)
  - Conveyance capacity (pixel·meter) and its error (D_cc)

## Experimental parameters and metadata
- The experimental_parameters.csv table documents:
  - Time since beginning (in minutes)
  - Inlet water discharge (Qw in L/min)
  - Associated DEM file name
  - Slope and slope error
  - Width, width error
  - Depth, depth error
  - Conveyance capacity and its error
- These fields underpin the linkage between each DEM and its measured morphodynamic state.

## How to use and interpret
- Use DEM_i.csv files to analyze temporal evolution of the river’s morphodynamics under different discharge scenarios.
- Compare DEMs via the consistently spaced 0.5 cm grid to quantify changes in floodplain depth, width, and overall conveyance capacity.
- Leverage the experimental_parameters.csv to contextualize each DEM with the corresponding discharge, time, and derived morphology.
- Follow the described processing workflow (reorientation quality control, area extraction, 2D rasterization, and Python-based analysis) to reproduce results or perform new analyses.