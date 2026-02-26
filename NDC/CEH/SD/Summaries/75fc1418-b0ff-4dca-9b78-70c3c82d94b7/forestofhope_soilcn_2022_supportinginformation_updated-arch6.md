# Overview

- The Forest of Hope is a native forest creation project on Highlands Rewilding's Beldorney Estate (coords: 57.409, -2.966).
- Planting details: density of 1600 stems/ha with species mix - birch 40%, sessile oak 20%, hazel 10%, alder 10%, rowan 10%, willow 5%, hawthorn 5%.
- Timeline: planting began in Winter 2022 and is expected to complete in early 2024 after a review of 2023 planting.
- Experimental design: 17 planted plots (40 × 40 m) and 17 natural regeneration plots within the planted area, with natural regeneration plots matched to planted plots; monitoring includes soil and biodiversity metrics alongside tree establishment.
- Baseline data: soil carbon (C) and nitrogen (N) samples collected in Autumn 2022.

## Study design and sampling regime

- 17 soil samples collected on a 100 m grid within the planting area before mounding/planting (Sept 2022); grid extended into surrounding grassland with 8 additional samples for a control site.
- Additional sampling (Nov 2022) in the 40 × 40 m unplanted plots to monitor natural regeneration.
- Plot types:
  - planted: 100 m grid within the area to be planted
  - grassland: 100 m grid extended into surrounding grassland
  - natural regeneration plots: unmounded/unplanted plots

## Collection and laboratory methods

- Sampling tool: 1.9 cm diameter auger; depths 0–10 cm and 10–30 cm (or shallower where not possible).
- One unplanted plot (U8) not sampled due to a pond.
- Lab processing: fresh weight recorded, samples dried at 60°C for at least 48 hours to constant mass, dry weight recorded; samples sieved to <2 mm and >2 mm fractions weighed.
- Subsampling and analysis: 5 g of the <2 mm fraction ball milled; ~10 mg weighed for elemental analysis to determine carbon and nitrogen contents.

## Nature and units of recorded values

- Measurements: fresh weight, dry weight (g); soil bulk density (g/cm3) based on the <2 mm fraction.
- Chemical content: percent carbon (%C) and nitrogen (%N); total carbon (Total_C_gcm3) and total nitrogen (Total_N_gcm3) calculated using bulk density and percent content.

## Quality control

- Pre-sampling numbering system to track samples; experienced lab technicians performed analyses to ensure precision and accuracy; exact sample weights recorded to high precision.

## Data structure

- Single CSV dataset: ForestOfHope_SoilCN_Winter2022.csv
- Key columns and descriptions:
  - Location_ID, Description: unique sample location identifier; Type: category of sampling (planted 100 m grid, grassland 100 m grid, natural regeneration plot)
  - Lat, Long: geographic coordinates; What3words: location reference
  - Date_collected: sampling date
  - Top_core_cm, Bottom_core_cm: depth range of soil core
  - Core_height_cm, Core_diameter_cm, Core_volume_cm3: geometry of soil core
  - Fresh_weight_g, Dry_weight_g: weights of soil samples
  - More_2mm_g, Less_2mm_g: weights of >2 mm and <2 mm fractions after drying
  - Bulk_density_gcm3: bulk density calculated from core and <2 mm fraction
  - N_percent, C_percent: percent nitrogen and carbon
  - Total_N_gcm3, Total_C_gcm3: absolute total nitrogen and carbon per cm3, calculated from bulk density and percentages

## Purpose and potential uses

- Enables assessment of soil carbon and nitrogen stocks under planted forest versus natural regeneration.
- Facilitates cross-depth analyses (0–10 cm vs 10–30 cm) and comparisons between plot types.
- Provides a ready-to-use dataset for ecological monitoring, carbon accounting, and policy-related reporting.