# Bank strength measurements in the Amazon River, September to October 2022

- The repository contains pre- and postprocessed data collected in the field and from satellite imagery for the Solimões River (Amazon River), published with the DOI https://doi.org/10.1130/G51862.1. Five data types are included, spanning in-situ measurements, satellite-derived land-water classifications, historic imagery, GIS-derived statistics, and high-resolution bathymetry.

## Data types and key contents

- 1) Bank strength measurements
  - Measurements performed Sep 25–Oct 8, 2022 on a 100 km river reach around Tefé (approximately 64°42′30″W, 3°21′S).
  - Files:
    - Measurement_locations.csv: location IDs, bank type, sediment type, GIS river kilometer.
    - CSM_measurements_test3.csv: per-location test settings, mean critical shear stress, mean shear strength (kPa).
    - Per-location folders containing shear vane measurements; converted values are provided, with a MATLAB/Python script (Figure2_LSV_CSM_violin.py) to plot violin plots.
  - Purpose: assess bank strength using shear vane and cohesion strength meter data.

- 2) Satellite imagery – Landsat-based binary maps
  - Postprocessed Landsat data classifying water vs. land for 1984–1988 and 2019–2023 along three 30–65 km reaches of the Solimões.
  - Files:
    - SHP-format binary images (water/land) with 20 m grid cell size, coordinates in Equal Earth.
    - Segmentations and reach delineations (10 km for reach 3; 20 km for reaches 1–2).
    - RiverKM fields containing River kilometer from Manaus, with Depth (m), Width (m), Qrockbank, QrockBed (distances to hard layers) derived from manual measurements in FABDEM.
  - Metadata fields include FID, Id, Shape_leng, and reach-related attributes.

- 3) Corona imagery (1967)
  - USGS-provided Corona imagery for a 100 km reach around Tefé, stitched into TIFF with RGB bands.
  - Files:
    - 1967 Corona TIFF imagery.
    - Digitized bank and bar lines provided as polylines (SHP) with FID IDs.
  - Use: historical channel morphology context for change analyses.

- 4) GIS_analysis – Global Water Surface Explorer (GWSE) based statistics
  - Large-scale analysis covering roughly 1,600 km upstream of Manaus ( Manaus area coordinates).
  - Files:
    - Two CSVs with GWSE-derived calculations for 5 km reaches, separated by left/right banks.
    - Aggregated area per polygon summed over ~10 km reaches; erosion/deposition distance mean calculated per length and year (37 years).
    - Python scripts to plot histograms of the results.

- 5) Multibeam echosounder (MBES) data
  - Cleaned and postprocessed data for a 2 km reach at river kilometer 688 from Manaus.
  - Files and processing:
    - Adjusted trajectory files and corrected bathymetric point clouds (LAZ and XYZ formats).
    - GGMatch: automatic strip alignment to correct relative/absolute geometric errors using sensor trajectory and overlapping swath data.
    - BathyQC: postprocessing to generate final data products.
    - Gridded outputs at 50 cm and 25 cm resolutions; RGB bands available.
  - Purpose: high-resolution bathymetric mapping to quantify bed morphology and compare with source data.

## Reference context

- The data and methodology align with the work described by Boothroyd et al. (2020) on detecting and quantifying morphological change in tropical rivers.