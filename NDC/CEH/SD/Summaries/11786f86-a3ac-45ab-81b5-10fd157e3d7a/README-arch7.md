# Bank strength measurements in the Amazon River, September to October 2022

- This repository holds pre- and postprocessed data collected in the field and from satellite imagery of the Solimões River (Amazon River), published with the DOI provided. It integrates multiple data types to support bank strength and river morphology analyses.

## Data types and formats

- 1) Measurements
  - Data: shear vane and cohesion strength meter measurements.
  - Time/Location: Sep 25–Oct 8, 2022; 100 km river reach around Tefé (approx. 64°42'30"W, 3°21'S).
  - Files:
    - Measurement_locations.csv: location IDs, bank type, sediment type, GIS-estimated river kilometer.
    - CSM_measurements_test3.csv: location ID, bank type, sediment type, test setting, mean critical shear stress, mean shear strength (kPa).
  - Per-location data: shear vane measurements stored in folders per location ID; includes converted values.
  - Analysis/Visualization: Figure2_LSV_CSM_violin.py to plot violin plots.

- 2) Satellite imagery (Landsat)
  - Data: binary maps of channel-land area (water vs land) for 1984–1988 and 2019–2023; three reaches along the Solimões River.
  - Format: SHP (Esri shapefiles) in WGS84; 20 m grid cell size TIFFs created for MATLAB workflows.
  - Geodata details: segments created for 10-km (reach 3) and 20-km (reaches 1–2); attributes include Shape_leng (m). RiverKM records river kilometer from Manaus with Depth (m) and Width (m); Qrockbank and QrockBed distances to hard layers, derived from visual/digital elevation model analyses (FABDEM).

- 3) Corona imagery (1967)
  - Data: Corona imagery from USGS for a 100 km reach around Tefé; RGB TIFF bands.
  - Vector: SHP of digitized bank and bar lines as polylines (FID IDs).

- 4) GIS_analysis (GWSE-derived statistics)
  - Data: two CSVs containing large-scale GWSE-based calculations for ~1,600 km upstream of Manaus.
  - Analysis: 5-km reaches split by bank (left/right); polygon areas summed over ~10-km reaches, mean annual erosion/deposition distance computed by reach length and 37 years of imagery.
  - Visualization: Python scripts (.py) to plot histograms.

- 5) Multibeam echosounder data (MBES)
  - Data: cleaned/postprocessed for a 2 km reach at river kilometer 688 (Manaus).
  - Outputs: adjusted trajectory files and corrected bathymetric LAS/LAZ point clouds; processed with GGMatch (trajectory alignment, error correction) and BathyQC.
  - Resolution: xyz data gridded to 50 cm and 25 cm; RGB bands included.

- Reference and related work
  - Boothroyd et al., 2020: methods for detecting and quantifying morphological change in tropical rivers (context for GWSE and image analysis approaches).

## Geospatial and work-flow notes for GIS specialists

- Spatial reference and projections
  - Landsat outputs: transformed to Equal Earth for postprocessing.
  - Shapefiles: provided in WGS 84 coordinates; coordinate handling and reprojecting may be needed for integration with other layers.
- Data integration across resolutions and times
  - Combines field measurements (bank strength) with historical/remote-sensing data (Landsat, Corona) and modern bathymetry (MBES) for multi-temporal analyses.
- Documentation and reproducibility
  - Included Python scripts for visualization (violin plots, histograms) and processing steps.
  - Cross-referencing between field locations, bank type, and sediment type supports spatially stratified analyses.
- Data packaging and accessibility
  - Datasets are spread across CSV, SHP, TIFF/LAZ/LAS formats; expect multi-source harmonization during GIS workflows.
  - Key identifiers: location IDs, FID/OBJECTID, RiverKM, reach delineations, and bank-specific attributes.

## How this supports GIS-based data products

- Enables map-based visualization of bank strength across a 100 km reach and broader morphodynamic context upstream
- Facilitates overlay of field measurements with land-water classifications and historical imagery for change detection
- Supports reproducible GIS analyses combining in-situ measurements with satellite-derived and bathymetric data
- Provides a structured dataset for policy-relevant riverbank integrity assessments, hazard mapping, and river management planning

## Access and citation

- DOI reference: https://doi.org/10.1130/G51862.1
- Source material includes field measurements, Landsat-derived land-water masks, Corona imagery, GWSE-derived analyses, and MBES data, with supporting plotting and processing scripts.