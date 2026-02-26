# Bank strength measurements in the Amazon River, September to October 2022

- Overview
  - A repository of pre- and postprocessed data collected in the field and from satellite imagery for the Solimões (Amazon) River around Tefé.
  - Five data types are included: measurements of bank strength, Landsat-derived binary maps, Corona imagery with channel outlines, postprocessed GIS data from GWSE, and multibeam echosounder data.
  - Data are organized to support data exploration, cross-dataset analysis, and the creation of data products for end users.

- Data types and key contents
  - 1) Measurements
    - Timeframe: Sep 25–Oct 8, 2022, covering a ~100 km reach around Tefé.
    - Files: Measurement_locations.csv (location IDs, bank type, sediment type, GIS river kilometer); CSM_measurements_test3.csv (location ID, bank type, sediment, test setting, mean critical shear stress, mean shear strength in kPa).
    - Per-location shear vane data stored in folders by location ID; accompanying Figure2_LSV_CSM_violin.py script to generate violin plots.
  - 2) Satellite imagery (Landsat)
    - Binary water/land classifications for 1984–1988 and 2019–2023 across three 30–65 km reaches along the Solimões.
    - Deliverables: SHP files (water/land shapes) with 20 m grid TIFF outputs for postprocessing in MATLAB.
    - Segment and riverkm data: 10 km (reach 3) and 20 km (reaches 1–2) segment lengths; SHP structure includes FID/Id fields, with river kilometer (RiverKM), depth (m), width (m), Qrockbank, and QrockBed metrics derived from visual observations and FABDEM.
  - 3) Corona imagery
    - 1967 Corona image for a 100 km reach around Tefé, stitched into TIFF with RGB bands.
    - Digitized bank and bar lines provided as polylines in SHP (FID identifiers).
  - 4) GIS_analysis (GWSE-based analyses)
    - Calculations for 1,600 km upstream from Manaus (1 of 2 GWSE analyses) across 5 km reaches, separated by river bank.
    - Outputs: two CSV files with mean annual erosion/deposition distance (derived from 37 years of imagery) and per-reach statistics; Python scripts to plot histograms.
  - 5) Multibeam echosounder (MBES)
    - Cleaned and postprocessed MBES data for a 2 km reach at river kilometer 688 from Manaus.
    - Outputs: adjusted trajectory files and corrected bathymetric point clouds (LAZ) for comparison against source data, using GGMatch for strip alignment and BathyQC for final processing.
    - Final gridded xyz data at 50 cm and 25 cm resolutions; bands are RGB.
    - Data processed with reference methods (GGMatch, BathyQC) to reduce geometric errors; documentation cites Boothroyd et al. (2020) for methodology.

- Data formats, provenance, and access notes
  - Formats include CSV, SHP (Shapefiles), TIFF, and LAZ, with RGB TIFFs for imagery.
  - Coordinate references: Landsat-derived SHP data provided in WGS84; postprocessed imagery and segment data are aligned for GIS and MATLAB analyses.
  - Provenance: Data linked to a published study with the DOI 10.1130/G51862.1 and the methodological framework described by Boothroyd et al. (2020).

- Processing and usage considerations for data support
  - The dataset is designed to enable self-serve analyses and cross-dataset comparisons (e.g., bank strength measurements with geomorphology from Landsat and Corona imagery, and MBES bathymetry).
  - The MBES workflow includes trajectory correction and bathymetric postprocessing, ensuring higher accuracy for riverbed analyses.
  - Users should be aware of dataset-specific structures (e.g., per-location measurement folders, FID/Id fields in SHP files, and river kilometer references) to correctly join and interpret data.
  - The repository provides scripts (e.g., violin plot generator) to facilitate quick visualization and interpretation of results.

- References
  - Boothroyd, R. J., Williams, R. D., Barrett, B., Hoey, T. B., Tolentino, P. L. M., Perez, J. E., ... & Yang, X. (2020). Detecting and quantifying morphological change in tropical rivers using Google Earth Engine and image analysis techniques. River Flow, 2020, 1013-1021.
  - Data described as published in the repository DOI: 10.1130/G51862.1.