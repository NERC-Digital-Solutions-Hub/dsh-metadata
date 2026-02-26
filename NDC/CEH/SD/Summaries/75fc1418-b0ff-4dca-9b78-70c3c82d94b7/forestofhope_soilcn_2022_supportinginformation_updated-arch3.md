# Overview

- Purpose and setting: The Forest of Hope is a native forest creation project on Highlands Rewilding's Beldorney Estate (coords 57.409, -2.966). The aim is to monitor soil carbon (C) and nitrogen (N) and track establishment of planted trees and natural regeneration.

- Planting details: 1600 stems/ha mixed native species (birch 40%, sessile oak 20%, hazel 10%, alder 10%, rowan 10%, willow 5%, hawthorn 5%). Planting began Winter 2022 and completion planned for early 2024 after a 2023 planting review.

- Experimental design: 
  - 17 planted plots and 17 unplanted natural regeneration plots, each 40 × 40 m, distributed with a gradient from seed sources and near a nearby semi-natural woodland.
  - Natural regeneration plots are matched to planted plots for comparative monitoring.
  - Baseline soil sampling for carbon and nitrogen collected autumn 2022.

- Sampling regime and plot layout:
  - A 100 m grid within the planting area plus extension into adjacent grassland, with 8 additional control-site samples.
  - Natural regeneration plots sampled at their centers; planted plots monitored to compare with regeneration plots.
  - One unplanted plot (U8) omitted from sampling due to a pond.

- Soil sampling methods:
  - Depths: 0–10 cm and 10–30 cm (where possible); core diameter 1.9 cm; two sampling depths documented where feasible.
  - Equipment and process: auger samples collected, fresh weight measured, soils dried at 60°C for at least 48 hours, dry weight measured, soils sieved to <2 mm and >2 mm fractions weighed.
  - Subsampling for analysis: ~5 g of <2 mm fraction ball milled; ~10 mg used for elemental analysis.
  - Analytical method: elemental analyzer to determine % C and % N; calculations convert to absolute C and N using bulk density estimates.

- Data collection and units:
  - Measurements recorded include fresh/dry weights, bulk density (g/cm3), % C, % N, total C (g/cm3), and total N (g/cm3).
  - Data tied to sample metadata (location, coordinates, date, depth, core dimensions, sample weights, fraction masses).

- Quality control and data integrity:
  - A unique sampling-location numbering system used to track samples.
  - Experienced lab technicians perform analyses; precise subsample weights ensure accuracy.

- Data structure and availability:
  - Single dataset: ForestOfHope_SoilCN_Winter2022.csv.
  - Key fields include Location_ID, Type (planted grassland, planted plot, natural regeneration plot), lat/long/What3words, date_collected, top/bottom core depths, core_height/diameter/volume, fresh/dry weights, fraction masses, bulk density, N%, C%, Total_N_gcm3, Total_C_gcm3, and related descriptive fields for each sample.

- Implications for monitoring and data governance:
  - Demonstrates a structured approach to linking physical plots with soil health metrics to evaluate restoration progress.
  - Highlights the importance of robust metadata, standardized sampling, and clear data processing steps for transparency and reproducibility.
  - Exposes practical challenges relevant to data sharing and governance, such as ensuring metadata completeness, managing data from multiple plot types, and documenting any deviations (e.g., pond area affecting sampling).