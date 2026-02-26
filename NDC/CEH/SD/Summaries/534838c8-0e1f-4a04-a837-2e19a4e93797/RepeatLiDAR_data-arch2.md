# Canopy height measured by LiDAR during the 2015-16 El Niño Southern Oscillation (ENSO) event in Malaysian Borneo

## Overview
- Repeat airborne LiDAR surveys before (Nov 2014) and after (Apr 2016) the 2015-16 ENSO drought were used to quantify canopy height change in human-modified tropical forests within oil palm landscapes in Sabah, Malaysian Borneo.
- Focuses on 36,655 pixels at 30 x 30 m resolution over ~3,301 ha in a mosaic of logged forests and oil palm plantations as part of the SAFE Project.
- TCH change (TCH_2016 - TCH_2014) serves as a key metric for canopy dynamics and structural change under drought and logging influences.

## Study area and context
- Located in Sabah, Malaysian Borneo, within the Stability of Altered Forest Ecosystems (SAFE) Project area, a gradient from Virgin Jungle Reserve to degraded, selectively logged forests transitioning toward oil palm.
- The landscape represents rapid transformation with logging history, road access, and plantation edge effects; the study area excludes oil palm plantations and salvage-logged forests to focus on regenerating logged forest pixels.
- Topography is varied (lowlands to >1,000 m), with forest buffers around oil palm edges and a distance measure (Dist_OP) to the nearest oil palm boundary.

## Data acquisition and processing
- LiDAR data sources:
  - 2014: NERC ALS50-II sensor (November 2014) with ~120 kHz pulse rate, 12° FOV, ~40 cm footprint, ~13.2 points m^-2.
  - 2016: GAO LiDAR system (April 2016) with 200 kHz, 34° FOV, ~1.8 m footprint, ~4.1 points m^-2.
- Processing workflow:
  - Create a common 1 m DTM from ground returns; interpolate ground and upper canopy returns to 2 m resolution for each flight.
  - Generate separate canopy height models (CHM) per survey and derive top-of-canopy height above ground (TCH).
  - Compute TCH_change per 30 x 30 m pixel as TCH_2016 - TCH_2014.
  - Downsample to 30 m to reduce lidar artefacts and within-canopy variability.
- Quality control and filtering:
  - Exclude 9,587 ha of oil palm and 2,500 ha of salvage-logged forest; remove pixels within 200 m of clear-cut areas; remove roads and 30 m buffers around roads.
  - Correct for LiDAR point density biases; remove pixels with NERC density < 10 points m^-2 (about 62% of dataset); assess GAO data and find no density bias.
  - Trim extreme values by removing the lower and upper 1% of TCH_change values.
- Final dataset scope:
  - Area: 3,301 ha (36,655 30 m pixels).
  - TCH_2014 range: 0–64 m.

## Additional spatial indicators
- Topographic Position Index (TPI) derived from the DTM to capture landscape position from valleys to ridges; computed on a 10 m coarsened DTM with 1 ha neighborhoods.
- Distance to oil palm edge (Dist_OP) calculated from Pléiades imagery (June 2016) to quantify proximity to plantation boundaries (0–4,200 m; mean ~1,825 m).

## Data structure and content
- Data file: RepeatLiDAR_SAFE_Project.csv
- 7 columns:
  - TCH_2014: TCH values for 2014 (m) at 30 m pixels.
  - TCH_2016: TCH values for 2016 (m) at 30 m pixels.
  - TCH_Change: TCH_change (m) = TCH_2016 - TCH_2014.
  - coords.x: Longitude of pixel center (UTM).
  - coords.y: Latitude of pixel center (UTM).
  - TPI: Topographic Position Index (unitless).
  - dist_OP: Distance to nearest oil palm edge (m).

## Implications for environmental monitoring and policy
- Demonstrates how repeat LiDAR over a large, human-modified tropical landscape can reveal canopy dynamics linked to drought and fragmentation.
- Produces standardized, QA’d height-change data suitable for monitoring forest health, carbon dynamics, and ecosystem responses to landscape change.
- The dataset facilitates cross-study synthesis by providing accessible, georeferenced, pixel-level measurements of canopy structure and its relation to topography and plantation proximity.
- Real-world relevance to policy: helps quantify effects of logging history and plantation expansion on forest structure, informing conservation priorities and landscape-scale management.
- Accessibility and reuse: aligns with aims to increase dataset value and enable access to underlying data for broader analysis and policy scrutiny.

## References (context)
- Foundational methods and related work on LiDAR fusion, canopy height modelling, and tropical forest structure, including SAFE Project context, canopy height modelling techniques, and forest fragmentation studies.