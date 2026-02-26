# Canopy height measured by LiDAR during the 2015-16 El Niño Southern Oscillation (ENSO) event in Malaysian Borneo

## Overview for monitoring frameworks
- Demonstrates repeat LiDAR as a scalable method to monitor forest dynamics, including canopy growth, mortality, and structural changes, relevant for evaluating policy and management decisions.
- Primary metric: top-of-canopy height (TCH) change over time (TCH_2016 − TCH_2014) across a large mosaic of forest and oil palm landscapes.
- Provides a 36,655-pixel, 30 m resolution dataset over 3,301 ha, enabling landscape-scale assessment of human modification and fragmentation effects.
- Emphasizes data handling practices essential for monitoring frameworks: data fusion across sensors, quality assurance, metadata, and transparent data sharing.

## Study context and policy relevance
- Location: Sabah, Malaysian Borneo within the Stability of Altered Forest Ecosystems (SAFE) project, a landscape-scale fragmentation experiment linked to oil palm expansion.
- Policy relevance: aligns forest conservation and land-use planning with real-world fragmentation gradients, offering evidence on how canopy structure responds to logging, edge effects, and plantation conversion.

## Data collection and processing approach
- LiDAR datasets:
  - 2014 data: NERC ALS50-II sensor, ~13.2 points per m².
  - 2016 data: GAO LiDAR system, ~4.1 points per m², with higher energy and broader footprint for ground detection in dense understory.
- Data fusion and height change estimation:
  - Created a common 1 m digital terrain model (DTM) using ground returns from both surveys.
  - Generated per-survey canopy height models (CHMs) and computed top-of-canopy height above ground (TCH).
  - Calculated TCH_change = TCH_2016 − TCH_2014, then aggregated to 30 m resolution to reduce artefacts.
- Study area and masking:
  - Initial area: 24,120 ha; final analysis area: 3,301 ha after removing oil palm plantations (9,587 ha), salvage-logged forest (2,500 ha), and areas within 200 m of clear-cut sites, as well as roads and adjacent buffers (30 m).
  - Addressed LiDAR point-density biases by removing pixels with density < 10 points/m² (affecting NERC data) and trimming outliers (lower/upper 1%).
- Outputs:
  - Final dataset comprises 36,655 pixels with TCH_2014 (0–64 m) and TCH_2016 values, plus derived TCH_Change.

## Auxiliary data and spatial context
- Topography: Generated Topographic Position Index (TPI) from the LiDAR-derived DTM to capture terrain position (valleys to ridges) and its relation to microclimate and nutrients.
- Land-use and distance to edge:
  - Pléiades satellite imagery (June 2016) used to classify forest vs. oil palm boundaries; high-resolution data (0.5 m panchromatic, resampled to 2 m) enabled edge delineation.
  - Dist_OP: distance from each pixel to the nearest oil palm plantation edge (0–4,200 m; mean ~1,825 m).
- Data structure:
  - Seven columns: TCH_2014, TCH_2016, TCH_Change, coords.x (longitude), coords.y (latitude), TPI, dist_OP.

## Implications for monitoring frameworks
- Demonstrates a robust workflow to produce comparable, landscape-scale canopy-change metrics across heterogeneous datasets (different LiDAR sensors and acquisition dates) suitable for policy evaluation and trend analysis.
- Highlights the importance of:
  - Careful data fusion (common DTM, cross-survey calibration) to ensure consistent change estimates.
  - Strategic masking to isolate relevant forest patches and minimize bias from non-forest land uses and logging infrastructure.
  - Explicit metadata and data structure design to support reproducibility and data governance.
- Provides a concrete example of integrating structural (TCH) metrics with topographic and edge-context variables (TPI, Dist_OP) to interpret canopy dynamics in the context of fragmentation and land-use change.

## Limitations and considerations for practice
- Sensor heterogeneity and variable point densities require careful bias correction and quality control to ensure cross-time comparability.
- Spatial filtering (edge buffers, road masks) may influence representativeness; ongoing governance should document these decisions for transparency.
- Access to and sharing of underlying datasets and metadata are critical considerations for public-facing monitoring frameworks; the study addresses some of these through detailed data description but also illustrates potential barriers.

## Key takeaways for monitoring framework design
- Use repeat LiDAR to quantify canopy structural changes at landscape scales, particularly where policy-relevant land-use changes (e.g., logging, oil palm expansion) occur.
- Derive a standardized change metric (TCH_change) after harmonizing data from multiple sensors and campaigns.
- Apply rigorous pre-processing, masking, and bias corrections to ensure reliable indicators of forest dynamics.
- Integrate structural metrics with topography and edge-distance context to better interpret drivers of change and inform targeted conservation or management interventions.
- Prioritize clear data formats and metadata to support governance, reproducibility, and data-sharing requirements in monitoring programs.