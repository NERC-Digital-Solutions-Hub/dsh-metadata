# Canopy height measured by LiDAR during the 2015-16 El Niño Southern Oscillation (ENSO) event in Malaysian Borneo

## Overview
- Repeat LiDAR captures used to monitor forest canopy dynamics across large landscapes within oil palm–modified systems.
- Provides canopy height change data for 36,655 30 × 30 m pixels over ~3,301 ha, focusing on human-modified tropical forests in Sabah, Malaysian Borneo.
- Combines pre- and post-ENSO LiDAR measurements to derive TCH change as a key indicator of structural dynamics and potential mortality, regrowth, or shedding events.

## Study site
- Location: Sabah, Malaysian Borneo, SAFE Project area (Stability of Altered Forest Ecosystems) characterized by a mosaic of logged forest and oil palm plantations.
- Context: Region with rapid, extensive transformation and fragmentation; study area reflects real-world habitat conversion relevant to policy.
- Landscape features: Varied topography from lowlands to hills >1,000 m a.s.l.; presence of forest buffers around plantations; distance-to-edge metrics capture edge effects.

## Airborne LiDAR data acquisition, fusion, and height-change estimation
- Data collection:
  - 2014 November: NERC ALS50-II LiDAR, 120 kHz, ~40 cm footprint, ~13.2 points/m².
  - 2016 April: GAO LiDAR, ~200 kHz, ~1.8 m footprint, ~4.1 points/m².
- Data fusion and processing:
  - Create a common 1 m digital terrain model (DTM) using ground returns from both surveys.
  - Generate per-survey canopy height models (CHM) and derive top-of-canopy height above ground (TCH).
  - Compute TCH_change = TCH_2016 − TCH_2014; coarsen to 30 m to reduce LiDAR artefacts and uncertainties.
- Data filtering and quality control:
  - Excluded 9,587 ha of oil palm and 2,500 ha salvage-logged forest between surveys.
  - Removed areas within 200 m of clear-cuts and 30 m roads/adjacent zones to reduce land-use confounds.
  - Corrected for point-density biases (particularly removing ~62% of the dataset where density < 10 points/m² in the NERC data) and trimmed extreme values by removing the bottom and top 1% of TCH_change.
- Final dataset extent:
  - Area analyzed: 3,301 ha (36,655 pixels).
  - TCH_2014 range: 0–64 m.

## Topography and distance-from-edge measures
- Topographic position index (TPI) computed from a 1 m DTM, resampled to 10 m and aggregated to 1 ha neighborhoods; TPI ranges from -24 (valleys) to 35.1 (hilltops).
- Edge distance (Dist_OP):
  - Derived from Pléiades imagery (June 2016) to delineate forest vs. oil palm boundaries (resampled to 2 m).
  - Dist_OP computed as the distance from each pixel’s center to the nearest oil palm edge; values 0–4,200 m (mean ~1,825 m).

## Data structure and production notes
- File: RepeatLiDAR_SAFE_Project.csv
- 7 columns:
  - TCH_2014: 30 m pixel-level TCH from 2014 LiDAR
  - TCH_2016: 30 m pixel-level TCH from 2016 LiDAR
  - TCH_Change: 30 m pixel-level TCH_change (2016 − 2014)
  - coords.x: Longitude of pixel center (UTM)
  - coords.y: Latitude of pixel center (UTM)
  - TPI: Topographic position index value
  - dist_OP: Distance to nearest oil palm edge (m)

## GIS implications and applications
- Enables mapping and analysis of canopy growth, decline, or turnover across a human-modified tropical landscape.
- Facilitates assessment of how canopy structure changes relate to:
  - Proximity to oil palm edges (Dist_OP)
  - Topographic context (TPI)
  - Landscape fragmentation gradients (SAFE project region)
- Data products are suitable for integration into GIS workflows to support policy-relevant analyses of forest degradation, edge effects, and microclimatic influences on forest structure.

## Methods and reproducibility considerations for GIS work
- Tools and approaches:
  - LAStools for LiDAR processing; lasground for ground point classification.
  - DTM and DEM/CHM construction, then TCH computation and change detection.
  - R packages (e.g., rgeos, gDistance) for distance calculations and spatial analysis.
- Considerations:
  - Harmonization of data from two different LiDAR systems with differing densities.
  - Substantial masking of oil palm and salvage-logged areas to focus on regenerating forest pixels.
  - Coarsening from 2 m to 30 m to reduce LiDAR artefacts and ensure robust change estimates.
  - Explicit quality controls to mitigate density biases and extreme values.

## Notes on limitations and interpretation
- significant exclusion of pixels due to point-density constraints (~62% removal in the NERC dataset), which can influence spatial coverage and statistical power.
- Differences in sensor characteristics necessitate careful interpretation when combining TCH metrics across time.
- The final dataset focuses on forest pixels with reduced confounding land-use types, potentially limiting generalizability to broader landscape categories without reprocessing.