# Canopy height measured by LiDAR during the 2015-16 El Niño Southern Oscillation (ENSO) event in Malaysian Borneo

## Overview
- Repeat LiDAR surveys before and after the 2015-16 ENSO to quantify canopy height change (TCH) in human-modified tropical forests within oil palm landscapes.
- Provides TCH change data for 36,655 30 x 30 m pixels over ~3,301 ha, plus high-resolution topographic data and distance to oil palm plantations.
- Data enable analysis of forest dynamics, including growth, mortality, leaf shedding, and disturbance in a fragmented landscape.

## Study area
- Sabah, Malaysian Borneo, within a mosaic of logged forests and oil palm plantations.
- Part of the Stability of Altered Forest Ecosystems (SAFE) Project, a forest fragmentation experiment examining biodiversity and ecosystem functioning under land-use change.

## LiDAR data collection
- 2014 (before ENSO): Leica ALS50-II, ~120 kHz, 12° field of view, ~40 cm footprint, ~13.2 points per m².
- 2016 (after ENSO): GAO system, ~200 kHz, 34° field of view, ~1.8 m footprint, ~4.1 points per m².
- Differences in sensor specs and densities addressed in processing to enable data fusion.

## Data processing and fusion
- Created a common 1 m DTM using ground returns from both surveys.
- Generated per-survey:
  - DEM (bare-earth ground elevation) at 2 m.
  - CHM (canopy height model) to estimate top-of-canopy height above ground (TCH).
- Calculated TCH change: TCH_2016 − TCH_2014.
- Coarsened TCH change map to 30 m resolution to reduce artefacts from repeat LiDAR.
- Quality control steps included:
  - Bias correction for point density differences (excluded NERC data with <10 pt/m²; ~62% of dataset removed).
  - Removal of outliers by trimming the bottom and top 1% of TCH change values.

## Study-area filtering and data curation
- Excluded:
  - 9,587 ha of oil palm plantations.
  - 2,500 ha of salvage-logged forest.
  - Pixels within 200 m of clear-cut areas to avoid logging-infrastructure effects.
  - Roads and 30 m surrounding areas due to land-cover differences.
- Resulting analysis area: ~3,301 ha (36,655 pixels); TCH_2014 ranged 0–64 m.

## Data products and variables
- RepeatLiDAR_SAFE_Project.csv (7 columns):
  - TCH_2014: TCH measurements from 2014 (30-m pixels).
  - TCH_2016: TCH measurements from 2016 (30-m pixels).
  - TCH_Change: TCH change (TCH_2016 − TCH_2014) in meters.
  - coords.x: Longitude of pixel center (UTM).
  - coords.y: Latitude of pixel center (UTM).
  - TPI: Topographic Position Index (unitless), 1 ha neighborhood values derived from the DTM.
  - dist_OP: Distance from the pixel to the nearest oil palm edge (m).

## Derived spatial context and variables
- Topographic Position Index (TPI) captures microtopography from the LiDAR-derived DTM, relating to microclimate and nutrient variation in SAFE.
- Dist_OP provides context on proximity to oil palm boundaries, useful for assessing edge effects on canopy change.
- TCH values indicate canopy structure, with 0–64 m observed range in 2014 data.

## Usage notes and limitations
- Data focus on canopy height dynamics within a fragmented, human-modified tropical landscape; not a pristine forest baseline.
- Exclusions (oil palm, salvage logging, buffers, roads) limit scope to regenerating logged forest pixels adjacent to oil palm mosaics.
- Point-density bias corrections were crucial for consistent change estimation; residual artefacts possible in areas with complex terrain or sparse sampling.
- Temporal window spans two LiDAR campaigns separated by ENSO-related drought, enabling analysis of growth and turnover under drought stress.

## References (context)
- Methods and context linked to multi-temporal LiDAR fusion and canopy-height analyses in tropical, human-modified forests.