# Canopy height measured by LiDAR during the 2015-16 El Niño Southern Oscillation (ENSO) event in Malaysian Borneo

## Overview
- Repeat LiDAR data collected immediately before (2014) and after (2016) the ENSO event to quantify canopy height changes in human-modified tropical forests within oil palm landscapes.
- Final dataset: 36,655 pixels at 30 × 30 m, covering ~3,301 hectares after rigorous filtering.
- Key outputs: per-pixel TCH in 2014 and 2016, and TCH change (2016 − 2014) across the study area; includes topographic context and distance to oil palm edges.

## Study area
- Location: Sabah, Malaysian Borneo, in a region dominated by logged forests and oil palm plantations.
- Context: Part of the Stability of Altered Forest Ecosystems (SAFE) Project, a fragmentation experiment linking intact forest patches to degraded forest to study biodiversity and ecosystem function under land-use change.
- Landscape characteristics: Varied topography from lowlands to hills (>1,000 m a.s.l.); presence of forest buffers along streams; land-use boundaries defined using high-resolution satellite imagery.

## Data collection and processing workflow
- LiDAR data acquisitions:
  - 2014 November: NERC’s Airborne Research Facility, Leica ALS50-II, 120 kHz, 12° FOV, ~40 cm footprint, ~13.2 points/m².
  - 2016 April: ASU Global Airborne Observatory (GAO), ~200 kHz, ~1.8 m footprint, ~4.1 points/m².
- Processing steps:
  - Create a common 1 m digital terrain model (DTM) from ground returns of both surveys.
  - Generate separate top-of-canopy height models (CHMs) for each survey; compute TCH by subtracting DTM from canopy elevations.
  - Compute TCH change (TCH_2016 − TCH_2014) and coarsen to 30 m resolution to reduce artefacts.
  - Exclude oil palm plantations, salvage-logged areas, and zones within 200 m of clear-cuts; remove roads and adjacent 30 m areas to avoid land-cover biases.
  - Remove pixels with low point density (<10 points/m² in the NERC dataset) to avoid bias; trim extreme values by removing the lowest and highest 1% of TCH change values.
- Data quality notes:
  - GAO data not biased by point density; NERC data showed underestimation of TCH in low-density areas (~62% of dataset removed due to density criteria).
  - Final analysis area: 3,301 ha (36,655 pixels); TCH_2014 ranged from 0 to 64 m.

## Data structure and variables
- Core dataset: RepeatLiDAR_SAFE_Project.csv with 7 columns:
  - TCH_2014: TCH measurements (m) from 2014 LiDAR at 30 m pixel resolution.
  - TCH_2016: TCH measurements (m) from 2016 LiDAR at 30 m pixel resolution.
  - TCH_Change: Change in TCH (m) from 2014 to 2016.
  - coords.x: Longitude (UTM) of each 30 m pixel center.
  - coords.y: Latitude (UTM) of each 30 m pixel center.
  - TPI: Topographic Position Index (unitless), computed from a LiDAR-derived DTM.
  - dist_OP: Distance (m) from the pixel to the nearest oil palm plantation edge (0–4,200 m).
- Additional context:
  - Land-use classification relied on Pléiades imagery (0.5 m panchromatic, 2.8 m res; resampled to 2 m) for edges between forest and plantations.
  - Pixel-level location data provided; no explicit rights metadata included in the dataset description.

## Topography and edge-distance metrics
- Topography: DTM-derived TPI to capture landscape position (ranging from -24 in valleys to 35.1 on hilltops).
- Edge distance: Dist_OP quantified from forest interior to oil palm boundary, enabling analysis of edge effects on canopy change.

## Data provenance and references
- Methodological alignment with established LiDAR approaches for tropical forest structure and carbon monitoring (e.g., Asner et al. 2014, 2018; Jucker et al. 2018; Khosravipour et al. 2014).
- Key references provided for data fusion, canopy height modeling, and topographic influences on microclimate and forest structure.

## Considerations for data stewardship and governance
- Dataset scope centered on a managerially relevant landscape (SAFE) with clear inclusion/exclusion criteria, enabling reproducible analyses of canopy dynamics in fragmented tropical forests.
- Notable governance considerations:
  - Clear documentation of data processing steps, resolution changes, and bias handling (point density, outlier trimming) to support transparency and reproducibility.
  - Explicit exclusion criteria (oil palm areas, salvage logging, proximity to roads) to ensure comparability and reduce confounding effects.
  - Metadata clarity around coordinates, units, and derived metrics (TTC, TPI, Dist_OP) to facilitate data reuse and integration with other datasets.