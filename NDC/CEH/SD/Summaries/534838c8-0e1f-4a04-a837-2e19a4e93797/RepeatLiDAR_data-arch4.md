# Canopy height measured by LiDAR during the 2015-16 El Niño Southern Oscillation (ENSO) event in Malaysian Borneo

- Purpose and scope
  - Demonstrates repeat LiDAR surveying as a tool to monitor forest dynamics over large areas.
  - Provides canopy height change data to assess structural responses in human-modified tropical forests within oil palm landscapes.
  - Delivers TCH change data for 36,655 pixels (30 × 30 m) across ~3,301 ha in Sabah, Malaysian Borneo, within a mosaic of logged forests and oil palm plantations.

- Study site
  - Location: Sabah, Malaysian Borneo, within the Stability of Altered Forest Ecosystems (SAFE) Project.
  - Context: region experiencing rapid forest transformation; a gradient from Virgin Jungle Reserve forests to degraded forests and oil palm plantations.
  - Relevance: site mirrors real-world policy issues around fragmentation, biodiversity, and ecosystem functioning.

- Data acquisition (LiDAR campaigns)
  - First survey: November 2014 using Leica ALS50-II (NERC Airborne Research Facility); ~120 kHz pulse frequency, 12° field of view, ~40 cm footprint; mean point density ~13.2 points m-2.
  - Second survey: April 2016 using GAO system (ASU); ~200 kHz pulse frequency, 34° FOV, ~1.8 m footprint; mean point density ~4.1 points m-2.
  - Rationale: different sensor characteristics; higher power and larger footprint in GAO increase ground detection in dense understory.

- Data processing and height change estimation
  - Ground and canopy processing with LAStools; creation of a common 1 m Digital Terrain Model (DTM) from both surveys.
  - Ground point identification and interpolation to produce bare-earth DEMs; generation of separate canopy height models (CHMs) for each survey.
  - Top-of-canopy height above ground (TCH) calculated from CHMs; TCH_2014 and TCH_2016 derived for each 30 m pixel.
  - TCH_change = TCH_2016 − TCH_2014; final mapping resampled to 30 m to reduce repeat LiDAR artefacts.
  - Area covered by repeated flights: 24,120 ha; final analysis area after filtering: 3,301 ha (36,655 pixels); TCH_2014 range: 0–64 m.

- Data cleaning and filtering
  - Excluded: 9,587 ha of oil palm plantations and 2,500 ha of salvage-logged forest between surveys.
  - Excluded pixels within 200 m of clear-cut areas to avoid edge effects from interim logging infrastructure.
  - Roads and adjacent 30 m buffers removed due to land-cover differences.
  - Addressed LiDAR biases: removed pixels with point density < 10 m-2 (approx. 62% of dataset); found no density bias in GAO data.
  - Outliers: trimmed lower and upper 1% of TCH_change values to remove unrealistic values.

- Topography and distance metrics
  - Topographic Position Index (TPI) computed from a 1 m DTM, using 10 m coarsening and 1 ha neighborhood means; TPI ranges from -24 (valleys) to 35.1 (ridgelines).
  - Distance to oil palm edge (Dist_OP) calculated from Pléiades satellite imagery (June 2016) at ~2 m resolution; Dist_OP ranges 0–4,200 m (mean ~1,825 m).
  - Land-use boundaries defined visually from high-resolution satellite imagery to distinguish forest vs. oil palm.

- Data structure and file content
  - File: RepeatLiDAR_SAFE_Project.csv with 7 columns:
    - TCH_2014: 30 m pixel TCH from Nov 2014.
    - TCH_2016: 30 m pixel TCH from Apr 2016.
    - TCH_Change: 30 m pixel change (2016 − 2014) in meters.
    - coords.x: longitude of pixel center (UTM).
    - coords.y: latitude of pixel center (UTM).
    - TPI: Topographic Position Index value.
    - dist_OP: distance to nearest oil palm boundary in meters.

- Software and methodological references
  - LAStools used for LiDAR processing.
  - Methodological basis and prior applications cited (e.g., ground interpolation, CHM derivation, and the use of TCH for biophysical inference).

- Implications and usage
  - Demonstrates integration of multi-sensor LiDAR data to quantify canopy dynamics in a highly transformed tropical landscape.
  - Provides a scalable, reproducible data product (pixel-level TCH and change) relevant for policy-focused analysis of fragmentation, restoration prioritization, and monitoring of forest structure under land-use change.