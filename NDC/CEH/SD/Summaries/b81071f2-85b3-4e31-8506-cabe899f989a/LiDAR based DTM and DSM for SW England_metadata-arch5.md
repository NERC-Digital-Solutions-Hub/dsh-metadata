# LiDAR based digital terrain and surface model for SW England [TELLUS SW-Project]

## Purpose and scope
- High-resolution LiDAR dataset over Cornwall and Devon (July–August 2013) for the Tellus South West project.
- Deliverables: Digital Terrain Model (DTM) and Digital Surface Model (DSM) representing bare earth and features on it.
- Spatial extent: 9424 km² west of Exmouth; coordinate system OSGB 1936 / British National Grid (EPSG:27700).

## Data products and attributes
- Two height layers at 1 m resolution:
  - DTM: terrain/bare earth.
  - DSM: surface features (buildings, vegetation) above bare earth.
  - Vertical accuracy: ~25 cm.
  - Data attribute: Elevation (Height) in metres.
- Deliverables format:
  - DSM/DTM as ESRI grid tiles (e.g., SX37ne, SX37nw, SX37se, SX37sw).
  - Calibrated LAS point cloud data delivered as individual flight lines.

## Data collection and processing
- Acquisition: 26 survey flights; 14817 line km of new LiDAR data.
- Coverage strategy: ca. 300 m overlap between data swaths; ~1 point per m² data density.
- Equipment: Optech ALTM 3100 EA LiDAR system with integrated GPS/INS; mounted on BAS Twin Otter aircraft.
- Processing and QA:
  - Processing performed by Environment Agency using Terrascan to generate DSM and DTM from calibrated point cloud.
  - Calibration and supporting inputs used: raw range files, SBET post-processed files, SMRSMG accuracy files, calibration files, flight logs, and ground truth details.
  - Quality control included comparison of DSM/DTM with existing LiDAR data and GPS ground truth; QA documented in EA QC report.

## Metadata, provenance, and supporting materials
- Documentation and supporting reports:
  - BASS survey report.
  - EA QC report detailing accuracy and limitations.
- Supporting data included with the dataset:
  - Flight logs and calibration files.
  - Ground truth survey details.

## Data accessibility and governance considerations
- Data access format: individual Esri grid tiles; LAS point cloud available per flight line.
- Source and project context: Tellus South West project; project overview available at the Tellus GB website.
- Data stewardship notes:
  - Clear indication of data provenance (airborne LiDAR collection, processing steps, and QA).
  - Metadata reflects dataset’s accuracy, resolution, coverage, and processing chain to support discoverability and reuse.
- Limitations and caveats:
  - Vertical accuracy ~25 cm; limitations documented in the EA QC report.
  - Handling of data in the context of large file sizes and potential interoperability considerations due to multiple formats and processing steps.