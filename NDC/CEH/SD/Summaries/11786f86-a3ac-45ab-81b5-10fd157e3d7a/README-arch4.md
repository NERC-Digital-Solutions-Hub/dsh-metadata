# Bank strength measurements in the Amazon River, September to October 2022

## Overview
- Public repository of pre- and postprocessed data collected in the field and from satellite imagery for the Solimões (Amazon) River, published at the provided DOI.
- Focuses on bank strength, channel-land extent, historical imagery, and hydrographic surveys around the city of Tefé (approximately 100 km river reach).
- Five data domains are included, with supporting metadata, processing scripts, and derived analyses.

## Data types and content

- 1) Measurements
  - Bank strength measurements using a shear vane and a cohesion strength meter, collected Sep 25–Oct 8, 2022 for a 100 km reach around Tefé (coordinates near 64°42′30″W, 3°21′S).
  - Key files: Measurement_locations.csv (location IDs, bank type, sediment type, GIS river kilometer), CSM_measurements_test3.csv (location ID, bank type, sediment type, test setting, mean critical shear stress, mean shear strength in kPa).
  - Per-location folders contain shear vane data; accompanying Figure2_LSV_CSM_violin.py for violin plots.

- 2) Satellite imagery
  - Postprocessed Landsat-derived binary maps (water vs. land) for 1984–1988 and 2019–2023, for three river reaches (30–65 km) along the Solimões.
  - Data provided as SHP files in WGS84 with 20 m grid cells; segments defined at 10-km or 20-km scales.
  - Segment metadata includes RiverKM (river kilometers from Manaus), Depth (m), Width (m), Qrockbank, QrockBed (hard layer distances).
  - Derived from Landsat classification and FABDEM-based distance measurements; files are organized with geometric attributes (FID, Id, Shape_leng, etc.).

- 3) Corona_images
  - Corona satellite image from 1967 for a 100 km reach around Tefé, provided as a stitched .TIF with RGB bands.
  - Digitized bank and bar lines provided as polylines in an accompanying SHP file (FID-based IDs).

- 4) GIS_analysis
  - Large-scale analysis derived from the Global Water Surface Explorer (GWSE) for ~1,600 km upstream of Manaus (around 65°W, 3°06′S).
  - Calculations cover 5-km reaches; results aggregated to mean annual erosion/deposition distance over ~37 years, plus per-reach statistics.
  - Outputs include two CSV files and Python scripts to plot histograms.

- 5) Multibeam echosounder data (MBES)
  - Cleaned and postprocessed data for a 2 km reach at river kilometer 688 near Manaus.
  - Outputs: adjusted trajectory files and corrected bathymetric point clouds (LAZ/XYZ), suitable for comparison with source data.
  - Processing chain includes GGMatch (trajectory alignment) and BathyQC; data gridded to 50 cm and 25 cm resolution with RGB bands.

## Data processing and provenance
- Data spans field measurements, satellite-derived classifications, historical imagery, and hydroacoustic surveys.
- Key methods and sources cited: Boothroyd et al. 2020 for Landsat-based river classification and analysis techniques; data openly linked via the DOI of the underlying publication.
- Coordinate systems and spatial details:
  - Landsat-derived SHP files in WGS 84; Corona imagery provided in TIFF with RGB bands; river kilometer and geospatial attributes derived from navigational maps and FABDEM DEM analyses.
  - MBES outputs gridded to high-resolution spatial scales (50 cm and 25 cm) for detailed bathymetry.

## Access, reuse and governance
- All data are organized into clearly labeled folders by data type, with accompanying metadata in CSV files (e.g., Measurement_locations.csv) and scripts (e.g., Figure2_LSV_CSM_violin.py).
- Primary access via the DOI-linked publication; data files include both raw and postprocessed versions to support verification and reuse.
- Clear provenance enables cross-domain reuse (hydrology, geomorphology, remote sensing, ocean/bank stability studies) and supports reproducibility of analyses.

## Implications for Data Leaders
- Demonstrates end-to-end data integration across field measurements, remote sensing, and hydrographic processing, aligned to a single river system.
- Highlights the importance of:
  - Rich metadata and standardized formats (CSV, SHP, TIFF, LAZ) to support discoverability and reuse.
  - Documentation of processing steps and software tools (Python scripts, GGMatch, BathyQC) to enable replication.
  - Cross-referencing datasets with published methodologies to ensure consistency and transparency.
- Reflects potential for co-ownership and collaboration across data sources (measurement campaigns, satellite archives, GWSE-derived analyses, MBES surveys) to support comprehensive data systems for river health and erosion monitoring.