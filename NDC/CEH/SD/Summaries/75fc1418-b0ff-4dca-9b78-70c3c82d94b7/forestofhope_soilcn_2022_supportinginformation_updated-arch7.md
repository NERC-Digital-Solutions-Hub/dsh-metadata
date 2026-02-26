# Overview

- Purpose: Establish baseline soil carbon (C) and nitrogen (N) across The Forest of Hope, compare planted area with natural regeneration, and monitor soil properties over time.
- Timing: Baseline soil sampling autumn 2022; planting began winter 2022 and to be completed by early 2024 after a 2023 planting review.
- Site context: Highlands Rewilding's Beldorney Estate (lat 57.409, lon -2.966). Native forest creation with a mix of species (birch 40%, sessile oak 20%, hazel 10%, alder 10%, rowan 10%, willow 5%, hawthorn 5%), planted at ~1600 stems/ha.
- Plots and design:
  - Planted area: 17 plots, each 40 × 40 m.
  - Natural regeneration: 17 plots, 40 × 40 m, unmounded/unplanted; centroids used for sampling.
  - Grassland control: 8 samples extending the 100 m soil sampling grid beyond planting area to serve as a control that will not be planted.
  - One unplanted plot (U8) not sampled due to a pond.
  - 100 m soil sampling grid established within the planting area prior to mounding and planting (Sept 2022); grid extended into adjacent grassland.
- Objectives for GIS relevance: Produce georeferenced soil CN data and plot-level context suitable for map-based analyses and stakeholder visuals.

## Experimental design and sampling regime

- Sampling framework:
  - 17 soil samples on a 100 m grid within the planting area (Sept 2022, pre-mounding/planting).
  - 8 additional samples in grassland control extending the 100 m grid.
  - November 2022 sampling in 40 × 40 m natural regeneration plots for ongoing monitoring.
- Depths:
  - 0–10 cm and 10–30 cm (sampling depth for some locations may have been unavailable beyond 30 cm; depth recorded).
- Core and plots:
  - Soil cores: 1.9 cm diameter.
  - Planted plots vs natural regeneration plots: paired approach for monitoring; centroids used for natural regeneration plots.
  - Field note: U8 pond prevented sampling at that location.

## Collection and laboratory processing methods

- Field collection:
  - Use 1.9 cm diameter auger.
  - Record core depth range and core dimensions; collect two depth ranges per sampling point where possible.
- Laboratory processing:
  - Fresh weight recorded; samples dried at 60°C for at least 48 hours to constant mass; dry weight recorded.
  - Samples sieved to 2 mm; fractions weighed (<2 mm and >2 mm).
  - <2 mm fraction ball milled; ~10 mg weighed into tin capsule with exact mass recorded.
  - Carbon and nitrogen measured with an elemental analyzer.
- Measurements reported:
  - Fresh weight (g) and dry weight (g).
  - Bulk density (g/cm^3) based on <2 mm fraction.
  - %C and %N; total C and total N calculated as g/cm^3 using bulk density and %C/%N.

## Data structure and recording

- Data file: ForestOfHope_SoilCN_Winter2022.csv
- Key columns and descriptors:
  - Location_ID, Description: unique sampling location type (100m grid planted, 100m grid grassland, natural regeneration plot).
  - Lat, Long: geographic coordinates.
  - What3words: precise location reference.
  - Date_collected: sampling date.
  - Top_core_cm, Bottom_core_cm: depth range of the sampled core.
  - Core_height_cm, Core_diameter_cm, Core_volume_cm3: physical dimensions and calculated core volume.
  - Fresh_weight_g, Dry_weight_g: mass before and after drying.
  - More_2mm_g, Less_2mm_g: weight of fractions >2 mm and <2 mm after drying.
  - Bulk_density_gcm3: calculated from core volume and <2 mm fraction.
  - N_percent, C_percent: % nitrogen and % carbon.
  - Total_N_gcm3, Total_C_gcm3: absolute total N and C per cm^3 derived from bulk density and %N/%C.
- Location metadata:
  - 17 planted plots, 17 natural regeneration plots, 8 grassland control points, plus overall study boundary and grid legend.

## Quality control and data integrity

- Pre-sampling numbering system established to track samples.
- Experienced lab technicians performed processing; precise weighing to ensure accuracy for elemental analysis.
- Consistent documentation of sampling depths, core dimensions, and sample mass to support reproducibility and GIS integration.

## GIS-relevant insights and accessibility

- Georeferenced dataset with lat/long and What3words enables spatial mapping of soil CN across planting vs. regeneration vs. control zones.
- Uniform 40 × 40 m plot grid in combination with the 100 m sampling grid supports multi-scale spatial analyses.
- Data can be integrated with map-based visualizations for stakeholders, policy colleagues, and public audiences to illustrate soil carbon and nitrogen distribution and changes over time.