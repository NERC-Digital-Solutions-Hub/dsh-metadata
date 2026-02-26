# Bank strength measurements in the Amazon River, September to October 2022

## Overview
- A data repository containing pre- and postprocessed field and satellite data collected around the Solimões (Amazon) River from Sep 25 to Oct 8, 2022, published alongside a DOI reference.
- Five data types are provided: bank strength measurements, Landsat-based channel-land maps, Corona imagery, postprocessed GIS data from GWSE, and cleaned multibeam echosounder (MBES) data.
- Data are organized to support discovery, reuse, and reproducibility, with accompanying processing scripts and documentation where relevant.

## Data types and contents

- Measurements
  - Bank strength measurements using a shear vane and a cohesion strength meter (CSV format).
  - Location and context files:
    - Measurement_locations.csv: location IDs, bank type, sediment type, GIS-estimated river kilometer.
    - CSM_measurements_test3.csv: location ID, bank type, sediment type, test setting, mean critical shear stress, mean shear strength (kPa).
  - Per-location measurement files: shear vane data stored in location-specific folders (with converted values based on vane geometry).
  - Supporting script: Figure2_LSV_CSM_violin.py to plot violin plots of results.

- Satellite imagery (Landsat)
  - Postprocessed Landsat data in SHP format with water/land classification for 1984–1988 and 2019–2023 across three river reaches (30–65 km each).
  - Data processing: binary images cleaned and reprojected to Equal Earth; exported as TIFF (20 m grid) for MATLAB postprocessing.
  - Spatial structure: SHP files with FID/Id representing land and water features; segment shapes correspond to 10-km and 20-km reach delineations along river kilometers.
  - Attributes include RiverKM (river kilometer from Manaus), Depth, Width, Qrockbank, QrockBed, derived from visual observations via DEM (FABDEM).

- Corona imagery
  - Corona image from 1967 for a 100 km reach around Tefé; RGB TIFF bands.
  - Digitized bank and bar lines provided as polyline SHP with FID IDs.

- GIS_analysis (GWSE-derived data)
  - Two CSVs containing large-scale GWSE-based calculations for ~1,600 km upstream of Manaus.
  - Analyses for 5-km reaches split by bank (left/right); mean annual erosion and deposition distance calculated per ~10-km reach.
  - Python code available to plot data histograms.

- Multibeam echosounder (MBES) data
  - Cleaned and postprocessed data for a 2-km reach at river kilometer 688 from Manaus.
  - Outputs: adjusted trajectory files, corrected bathymetric point clouds (LAZ format) for cross-data comparison.
  - Processing workflow: GGMatch (automatic strip alignment using trajectory and overlapping swath data) to correct geometric errors, followed by BathyQC postprocessing; final xyz data gridded at 50 cm and 25 cm resolutions.
  - Visualization: RGB bands provided.

## Data formats, structure, and provenance
- Formats used: CSV, SHP, TIFF, LAZ, and Python scripts.
- Coordinate systems: most GIS components use WGS84; Landsat-derived segments reprojected to Equal Earth for processing.
- Traceability: datasets reference methods from Boothroyd et al. 2020 for river morphology analysis; MBES workflow documented with GGMatch and BathyQC tools.
- Documentation and code: supporting Python scripts provided for plotting and analysis (e.g., violin plots, histograms).

## Data processing and quality assurance
- Field and satellite data undergo:
  - Standardization of units and formats (e.g., conversion of shear strength values, alignment of measurement locations).
  - Spatial alignment and coordinate transformation to consistent CRS.
  - Postprocessing steps for Landsat data and GWSE-derived metrics to enable comparability across time.
  - MBES data quality controls via trajectory correction, grid generation, and cross-checks using GGMatch and BathyQC.
- Metadata elements include location IDs, bank type, sediment type, river kilometer estimates, and segment/line identifiers for traceability.

## Access, reuse, and licensing considerations
- Data are published with a DOI, enabling citation and formal reuse.
- Datasets are broken down by type to support targeted discovery (measurements, imagery, GWSE analyses, MBES data).
- Reuse notes:
  - Some analyses rely on manual distance measurements and model-derived attributes (e.g., Qrock distances, channel depths) and may require understanding of underlying methods (FABDEM, GWSE, etc.).
  - Associated scripts are provided to reproduce visualizations and some analyses.
- Users should reference Boothroyd et al. (2020) for GWSE methodology when interpreting large-scale river changes.

## Governance considerations and challenges for Data Stewards
- Data heterogeneity: five distinct data types across various formats (CSV, SHP, TIFF, LAZ) requiring careful metadata harmonization and interoperability strategies.
- Large datasets and transfer: MBES and Landsat-derived products involve substantial data volumes; plan for storage, access, and transfer efficiencies.
- Metadata completeness: ensure consistent documentation across all files (units, coordinate systems, reach definitions, IDs, and provenance).
- Versioning and updates: coordinate with data creators to manage updates or corrections to measurements, imagery, or GWSE-derived metrics.
- Interoperability: align with common standards to facilitate cross-dataset integration (e.g., consistent river reach definitions, CRS, and naming conventions).
- Accessibility: maintain clear paths to data and scripts, including any embargoed or sensitive components, and ensure proper citation and attribution.