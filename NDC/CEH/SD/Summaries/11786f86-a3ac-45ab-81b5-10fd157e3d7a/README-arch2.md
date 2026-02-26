# Bank strength measurements in the Amazon River, September to October 2022

## Overview
- A data repository of pre- and postprocessed field and satellite data for the Solimões (Amazon) River, accompanying the publication at DOI 10.1130/G51862.1.
- Five data types are provided, encompassing field measurements, satellite-derived land-water classifications, historical imagery, postprocessed GIS data, and multibeam echosounder data.
- Aimed at enabling standardized analysis of bank strength, channel morphology, and related environmental conditions over time.

## Data types and key contents

- 1) Measurements (shear vane and cohesion strength meter)
  - Collected Sep 25–Oct 8, 2022 over a 100 km reach near Tefé (coordinates around 64°42'30" W, 3°21' S).
  - Files include:
    - Measurement_locations.csv: location IDs, bank type, sediment type, GIS-based river kilometer.
    - CSM_measurements_test3.csv: location ID, bank type, sediment type, test setting, mean critical shear stress, mean shear strength (kPa).
  - Per-location folders contain shear vane data; data supplied in converted and raw forms; a Python script (Figure2_LSV_CSM_violin.py) generates violin plots from the data.

- 2) Satellite imagery (Landsat-based binary maps)
  - Postprocessed Landsat data (SHP format) for land-water classification.
  - Covers 1984–1988 and 2019–2023 for three 30–65 km reaches along the Solimões River.
  - Outputs transformed to 20 m grid cells (TIFF for processing; SHP files in WGS84 with FID/Id).
  - Segment definitions: 10-km (reach 3) and 20-km (reaches 1 and 2); includes river kilometer data (RiverKM), depth, width, and distances to hard layers (Qrockbank, QrockBed) derived from visual/DIG elevations (FABDEM).

- 3) Corona imagery (1967)
  - Corona image for a 100 km reach around Tefé (same coordinates) stitched into TIFF with RGB bands.
  - SHP file of digitized bank and bar lines as polylines (FID for each polyline).

- 4) GIS_analysis (Global Water Surface Explorer)
  - Calculations for 1,600 km upstream of Manaus (upstream reach area).
  - CSV outputs calculating changes for 5-km reaches, with area-derived metrics to mean annual erosion and deposition distance; means aggregated across ~10-km reaches; Python scripts generate histograms.

- 5) Multibeam echosounder data (MBES)
  - Cleaned and postprocessed data for a 2-km reach at river kilometer 688 (Manaus area).
  - Outputs include adjusted trajectory files and corrected bathymetric point clouds (LAZ and XYZ), processed with GGMatch (trajectory alignment and error correction) and BathyQC for final gridding at 50 cm and 25 cm resolutions; RGB imagery included.

- Cited methodology reference: Boothroyd et al. (2020) on detecting and quantifying morphological change in tropical rivers.

## Data processing and quality
- Data include both raw field/satellite inputs and postprocessed outputs, enabling reproducibility and cross-time comparisons.
- Measurements and imagery are organized with explicit metadata (locations, bank type, sediment type, river kilometers, segment lengths, and derived metrics).
- Postprocessing steps involve standard GIS and remote-sensing workflows (Landsat classification, CORONA stitching, FABDEM-based measurements, GWSE-based erosion/deposition calculations, and MBES trajectory/bathymetry corrections).

## Access, formats, and reproducibility
- Storage in widely used formats: CSV (measurements and analyses), SHP (vector land-water/classification and bank lines), TIFF (image data and bathymetry), and LAZ/XYZ (bathed point clouds).
- Scripted outputs and visualizations are supported by Python files for figure generation and data plotting.
- Data are organized to enable straightforward integration with standard environmental monitoring workflows and portals.

## Relevance for environmental monitoring
- Provides a consistent, multi-temporal dataset to assess bank strength, channel morphology, and erosion/deposition dynamics in a key tropical river system.
- Combines field measurements with historical and contemporary remote sensing data for integrated analysis.
- Supports standardised reporting and performance assessment of environmental health and river-management policies over time.

## Challenges and opportunities highlighted
- Increasing the value of datasets by integrating these data with other relevant environmental datasets for broader analyses.
- Ensuring broader access to underlying data to facilitate reuse by researchers, policymakers, and practitioners.